---
title: Aspose.PSD für .NET 21.9 - Versionshinweise
type: docs
weight: 40
url: /de/net/aspose-psd-fuer-net-21-9-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-574|Stellen Sie die RLE-Komprimierung standardmäßig für das Speichern von PSDs ein, um die Ausgabedateigröße zu vermeiden|Funktion|
|PSDNET-747|Unterstützung des Überlagerungsmuster-Layer-Effekts mit dem Mehrkanalfarbmodus in der PSD-Datei|Funktion|
|PSDNET-951|Nach dem Erstellen der neuen Ebene ist ihre Ressourceneigenschaft null, was Manipulationen verhindert (zum Beispiel Ändern der Größe)|Fehler|
|PSDNET-955|Nicht unterstützte Komprimierungsmethoden ZipWithPrediction für 8-Bit|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

## **Beispiele für die Verwendung:**

**PSDNET-574. Stellen Sie die RLE-Komprimierung standardmäßig für das Speichern von PSDs ein, um die Ausgabedateigröße zu vermeiden**

{{< highlight csharp >}}
            string inputFilePath = "file.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Unterstützung des Überlagerungsmuster-Layer-Effekts mit dem Mehrkanalfarbmodus in der PSD-Datei**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Soll keine Ausnahme auslösen
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Soll keine Ausnahme auslösen
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Nach dem Erstellen der neuen Ebene ist ihre Ressourceneigenschaft null, was Manipulationen verhindert (zum Beispiel Ändern der Größe)**

{{< highlight csharp >}}
            string PSDFile = "Layer1.psd";
            string layer1File = "Layer2.png";
            string layer2File = "Layer3.png";
            string outFileName = "finaloutput.psd";

            void ReplaceColor(RasterImage image, Color oldColor, int diff, Color newColor)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var length = pixels.Length;

                var oldR = oldColor.R;
                var oldG = oldColor.G;
                var oldB = oldColor.B;
                var newColorValue = newColor.ToArgb();

                for (int i = 0; i < length; i++)
                {
                    // Rot
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Grün
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Blau
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Layer2 = null;
            Layer Layer3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Hinzufügen von Ebene 1

                using (var stream = new FileStream(layer1File, FileMode.Open))
                {
                    Layer2 = new Layer(stream);

                    Layer2.Resize(image.Width, image.Height);
                    var width = Layer2.Width;
                    var height = Layer2.Height;

                    Layer2.Left = 675;
                    Layer2.Top = 0;

                    Layer2.Right = Layer2.Left + width;
                    Layer2.Bottom = Layer2.Top + height;

                    image.AddLayer(Layer2);
                }

                #endregion

                using (var stream = new FileStream(layer2File, FileMode.Open))
                {
                    Layer3 = new Layer(stream);
                    // Ersetzen der weißen Farbe durch Transparent
                    ReplaceColor(Layer3, Color.White, 256, Color.Transparent);
                    Layer2.DrawImage(new Point(0, 0), Layer3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Nicht unterstützte Komprimierungsmethoden ZipWithPrediction für 8-Bit**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "out_Zip8bit.psd";
            string outputZip16 = "out_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}

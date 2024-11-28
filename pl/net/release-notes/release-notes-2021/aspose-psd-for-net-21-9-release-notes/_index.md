---
title: Notatki dotyczące wydania Aspose.PSD dla .NET 21.9
type: docs
weight: 40
url: /pl/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-574|Ustawienie kompresji RLE jako domyślnej dla zapisywania plików PSD w celu uniknięcia ogromnego rozmiaru pliku wynikowego PSD|Funkcja|
|PSDNET-747|Wsparcie efektów warstw wzorca nakładki z trybem kolorów wielokanałowych w pliku PSD|Funkcja|
|PSDNET-951|Po utworzeniu nowej warstwy jej właściwość Resources jest zerowa, co uniemożliwia manipulacje (np. zmianę rozmiaru)|Błąd|
|PSDNET-955|Niewspierane metody kompresji ZipWithPrediction dla 8-bitowych plików|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- Brak

# **Usunięte API:**
- Brak

## **Przykłady użycia:**

**PSDNET-574. Ustawienie kompresji RLE jako domyślnej dla zapisywania plików PSD w celu uniknięcia ogromnego rozmiaru pliku PSD**

{{< highlight csharp >}}
            string inputFilePath = "plik.psd";
            string output1 = "output_original.psd";
            string output2 = "output_psdOptions.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Wsparcie efektów warstw wzorca nakładki z trybem kolorów wielokanałowych w pliku PSD**

{{< highlight csharp >}}
            var fileName = "AllEffects.psd";
            var outputFile = "AllEffects_out.psd";
            var loadOptions = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Nie powinno wywoływać wyjątku
            using (var im = Image.Load(fileName, loadOptions))
            {
                // Nie powinno wywoływać wyjątku
                im.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-951. Po utworzeniu nowej warstwy jej właściwość Resources jest zerowa, co uniemożliwia manipulacje (np. zmianę rozmiaru)**

{{< highlight csharp >}}
            string PSDFile = "Warstwa1.psd";
            string warstwa1Plik = "Warstwa2.png";
            string warstwa2Plik = "Warstwa3.png";
            string outFileName = "wyjsciekoncowe.psd";

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
                    // Czerwony
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Zielony
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Niebieski
                    var b = (byte)(pixels[i] & 0xff);

                    int actualDiff = Math.Abs(r - oldR) + Math.Abs(g - oldG) + Math.Abs(b - oldB);

                    if (actualDiff <= diff)
                    {
                        pixels[i] = newColorValue;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Warstwa2 = null;
            Layer Warstwa3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDFile))
            {
                #region Dodawanie Warstwy 1

                using (var stream = new FileStream(warstwa1Plik, FileMode.Open))
                {
                    Warstwa2 = new Layer(stream);

                    Warstwa2.Resize(image.Width, image.Height);
                    var width = Warstwa2.Width;
                    var height = Warstwa2.Height;

                    Warstwa2.Left = 675;
                    Warstwa2.Top = 0;

                    Warstwa2.Right = Warstwa2.Left + width;
                    Warstwa2.Bottom = Warstwa2.Top + height;

                    image.AddLayer(Warstwa2);
                }

                #endregion

                using (var stream = new FileStream(warstwa2Plik, FileMode.Open))
                {
                    Warstwa3 = new Layer(stream);
                    // Zamiana białego koloru na przezroczysty
                    ReplaceColor(Warstwa3, Color.White, 256, Color.Transparent);
                    Warstwa2.DrawImage(new Point(0, 0), Warstwa3);
                }

                image.Save(outFileName, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Niewspierane metody kompresji ZipWithPrediction dla 8-bitowych plików**

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

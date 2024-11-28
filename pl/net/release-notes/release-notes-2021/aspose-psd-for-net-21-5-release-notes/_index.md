---
title: Notatki wydania Aspose.PSD dla .NET 21.5
type: docs
weight: 80
url: /pl/net/aspose-psd-dla-net-21-5-notatki-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-758|Wsparcie dla zmiany rozmiaru warstw kształtów z ścieżkami wektorowymi|Nowa funkcjonalność|
|PSDNET-862|Wsparcie dla zmiany rozmiaru warstw kształtów z ścieżkami wektorowymi, gdy zmieniana jest tylko jedna warstwa|Nowa funkcjonalność|
|PSDNET-578|Ucinany łańcuch tekstowy|Błąd|

## **Zmiany w publicznym API**
# **Dodane interfejsy API:**
- Brak

# **Usunięte interfejsy API:**
- Brak

## **Przykłady użycia:**

**PSDNET-578. Ucinany łańcuch tekstowy**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // Ustawienie ścieżki czcionek
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. Wsparcie dla zmiany rozmiaru warstw kształtów z ścieżkami wektorowymi**

{{< highlight csharp >}}
            string sourceFileName = "vectorShapes.psd";
            string outputFileName = "out_vectorShapes.psd";
            string dataDir = "PSDNET758_1";
            string sourcePath = Path.Combine(dataDir, sourceFileName);
            string outputPath = Path.Combine(dataDir, outputFileName);
            using (var psdImage = (PsdImage)Image.Load(sourcePath))
            {
                foreach (var layer in psdImage.Layers)
                {
                    layer.Resize(layer.Width * 5 / 4, layer.Height / 2);
                }

                psdImage.Save(outputPath);
                psdImage.Save(Path.ChangeExtension(outputPath, ".png"), new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-862. Wsparcie dla zmiany rozmiaru warstw kształtów z ścieżkami wektorowymi, gdy zmieniana jest tylko jedna warstwa**

{{< highlight csharp >}}
            // Ten przykład pokazuje, jak zmienić rozmiar warstw z obrazem Vogk i ścieżką wektorową w obrazie PSD
            float scaleX = 0.45f;
            float scaleY = 1.60f;
            string dataDir = "PSDNET862_1";
            string sourceFileName = Path.Combine(dataDir, "vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                for (int layerIndex = 1; layerIndex < image.Layers.Length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f)
                {
                    var layer = image.Layers[layerIndex];
                    var newWidth = (int)Math.Round(layer.Width * scaleX);
                    var newHeight = (int)Math.Round(layer.Height * scaleY);
                    layer.Resize(newWidth, newHeight);

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("en-GB");
                    string outputName = string.Format("resized_{0}_{1}_{2}", layerIndex, scaleX, scaleY);
                    string outputPath = Path.Combine(dataDir, outputName + ".psd");
                    string outputPngPath = Path.Combine(dataDir, outputName + ".png");
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

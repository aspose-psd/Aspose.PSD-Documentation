---
title: Aspose.PSD voor .NET 21.5 - Release-opmerkingen
type: docs
weight: 80
url: /nl/net/aspose-psd-voor-net-21-5-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-758|Ondersteuning voor het wijzigen van vormlagen met vectorpaden|Functie|
|PSDNET-862|Ondersteuning voor het wijzigen van vormlagen met vectorpaden wanneer alleen een laag wordt gewijzigd|Functie|
|PSDNET-578|Afgekapte tekstreeks|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-578. Afgekapte tekstreeks**

{{< highlight csharp >}}
            string srcFile = "grinched-regular-font.psd";
            string output = "output_grinched-regular-font.psd.png";

            // Set lettertypen pad
            System.Collections.Generic.List<string> fonts = new System.Collections.Generic.List<string>();
            fonts.AddRange(FontSettings.GetDefaultFontsFolders());
            fonts.Add(@"Fonts\");
            FontSettings.SetFontsFolders(fonts.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. Ondersteuning voor het wijzigen van vormlagen met vectorpaden**

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

**PSDNET-862. Ondersteuning voor het wijzigen van vormlagen met vectorpaden wanneer alleen een laag wordt gewijzigd**

{{< highlight csharp >}}
            // Dit voorbeeld toont hoe lagen met een Vogk en vectorpadresource in de PSD-afbeelding worden gewijzigd
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

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("nl-NL");
                    string outputName = string.Format("resized_{0}_{1}_{2}", layerIndex, scaleX, scaleY);
                    string outputPath = Path.Combine(dataDir, outputName + ".psd");
                    string outputPngPath = Path.Combine(dataDir, outputName + ".png");
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}

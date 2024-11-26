---
title: Aspose.PSD voor .NET 21.1 - Uitgaveopmerkingen
type: docs
weight: 120
url: /nl/net/aspose-psd-voor-net-21-1-uitgaveopmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat uitgaveopmerkingen voor [Aspose.PSD voor .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Belangrijkste** | **Samenvatting** | **Categorie** |
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Uitzondering bij het proberen om een bepaald Psd-bestand naar png te converteren|Bug|
|PSDNET-792|Uitzondering bij het opslaan van PSD met slim object naar PNG|Bug|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-766. Aspose.PSD 20.10: Uitzondering bij het proberen om een bepaald Psd-bestand naar png te converteren**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Uitzondering bij het opslaan van PSD met slim object naar PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder + "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Op zoek naar Slim Object
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // We laden Slim Object Layer vanuit Memory Stream,
                        // Maar we kunnen smart.ExportContents(somePath) gebruiken om het slimme object naar een bestand te exporteren
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Op zoek naar Tekstlaag
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // We kunnen eenvoudig UpdateText gebruiken, maar op deze manier kunnen we tekst bewerken per gedeelte
                                        // Maak meerregelige tekstlagen en andere tekst- en alinea-opmaakfuncties
                                        // Wees voorzichtig. Als de inhoud van het slimme object geen PSD is, kun je deze manier van tekstbewerking niet gebruiken
                                        // In dat geval moet je de Grafische API gebruiken: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Best";

                                        // Je moet de grootte van de tekst aanpassen als je wilt dat de afbeelding er goed uitziet.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Het is beter om ReplaceContents te gebruiken. Het zal het Slim Object automatisch opnieuw renderen
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Op deze manier slaan we het gewijzigde PSD-bestand op
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

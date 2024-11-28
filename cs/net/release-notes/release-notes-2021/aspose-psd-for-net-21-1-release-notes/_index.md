---
title: Aspose.PSD pro .NET 21.1 - Poznámky k vydání
type: docs
weight: 120
url: /cs/net/aspose-psd-pro-net-21-1-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Výjimka při pokusu o konverzi konkrétního souboru Psd na png|Chyba|
|PSDNET-792|Výjimka při ukládání PSD s chytrým objektem do PNG|Chyba|

## **Změny ve veřejném rozhraní API**
# **Přidaná rozhraní:**
- Žádné

# **Odebraná rozhraní:**
- Žádné

## **Příklady použití:**
**PSDNET-766. Aspose.PSD 20.10: Výjimka při pokusu o konverzi konkrétního souboru Psd na png**
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

**PSDNET-792. Výjimka při ukládání PSD s chytrým objektem do PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Hledání chytrého objektu
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Načítáme vrstvu chytrého objektu ze streamu paměti,
                        // Ale můžeme použít smart smart.ExportContents(somePath) k exportu chytrého objektu do souboru
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Hledání textové vrstvy
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Můžeme použít jednoduché UpdateText, ale tímto způsobem získáme schopnost editovat text částmi
                                        // Vytvořit víceřádkové textové vrstvy a jiné funkce formátování textu a odstavce
                                        // Buďte opatrní. Pokud Obsah chytrého objektu není PSD, nemůžete používat tento způsob editace textu
                                        // V takovém případě byste měli použít Grafické API: https://docs.aspose.com/psd/net/kresleni-obrazku-pomoci-grafiky/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Nejlepší";

                                        // Pokud chcete, aby obrázek vypadal pěkně, měli byste změnit velikost textu.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Lepší je použít ReplaceContents. Automaticky znovu vykreslí chytrý objekt
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Tímto způsobem ukládáme změněný soubor PSD
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

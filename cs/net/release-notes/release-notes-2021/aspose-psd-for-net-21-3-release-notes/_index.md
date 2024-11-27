---
title: Aspose.PSD pro .NET 21.3 - Poznámky k vydání
type: docs
weight: 100
url: /cs/net/aspose-psd-pro-net-21-3-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-823|Přidání SectionDividerLayer pro zlepšení zážitku se skupinami vrstev|Vylepšení|
|PSDNET-694|Při čtení PattResource byly zaměněny šířka a výška|Chyba|
|PSDNET-789|Nesprávné míchání více než jednoho efektu vrstvy|Chyba|
|PSDNET-805|Nesprávné pořadí a logika míchání při více než jednom efektu vrstvy|Chyba|
|PSDNET-842|Vlastnosti efektu tažení se neukládají do souboru PSD|Chyba|

## **Změny ve veřejném rozhraní API**
# **Přidané API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Odstraněné API:**
- Žádné

## **Příklady použití:**

**PSDNET-694. Při čtení PattResource byly zaměněny šířka a výška**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // zavolat renderování vzoru

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Nesprávné míchání více než jednoho efektu vrstvy**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
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
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Nejlepší";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Tímto způsobem ukládáme změněný soubor PSD
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Nesprávné pořadí a logika míchání při více než jednom efektu vrstvy**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // Tímto způsobem ukládáme změněný soubor PSD
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Přidání SectionDividerLayer pro zlepšení zážitku se skupinami vrstev**

{{< highlight csharp >}}
            // Následující kód ukazuje vrstvy SectionDividerLayer a jak získat s nimi související vrstvu LayerGroup.

            // Hierarchie vrstev
            //    [0]: '</Layer group>' SectionDividerLayer pro skupinu 1
            //    [1]: 'Vrstva 1' Běžná vrstva
            //    [2]: '</Layer group>' SectionDividerLayer pro skupinu 2
            //    [3]: '</Layer group>' SectionDividerLayer pro skupinu 3
            //    [4]: 'Skupina 3' GroupLayer
            //    [5]: 'Skupina 2' GroupLayer
            //    [6]: 'Skupina 1' GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekty nejsou stejné.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Vytvoření hierarchie vrstev
                // Přidejte skupinu vrstev 'Skupina 1'
                LayerGroup group1 = image.AddLayerGroup("Skupina 1", 0, true);
                // Přidejte běžnou vrstvu
                Layer layer1 = new Layer();
                layer1.DisplayName = "Vrstva 1";
                group1.AddLayer(layer1);
                // Přidejte skupinu vrstev 'Skupina 2'
                LayerGroup group2 = group1.AddLayerGroup("Skupina 2", 1);
                // Přidejte skupinu vrstev 'Skupina 3'
                LayerGroup group3 = group2.AddLayerGroup("Skupina 3", 0);

                // Získá SectionDividerLayer's
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // pomocí metody SectionDividerLayer.GetRelatedLayerGroup(), získáme související instanci LayerGroup.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // stejná LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // stejná LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // stejná LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Skupina 1' obsahuje 5 vrstev
            }
{{< /highlight >}}

**PSDNET-842. Vlastnosti efektu tažení se neukládají do souboru PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekty nejsou stejné.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Nebude vyvoláno ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Kontrola uložených hodnot
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

---
title: Aspose.PSD für .NET 21.3 - Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-psd-für-net-21-3-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-823|Fügen Sie die SectionDividerLayer hinzu, um die Erfahrung mit Ebenengruppen zu verbessern|Verbesserung|
|PSDNET-694|Beim Lesen von PattResource wurden Breite und Höhe vertauscht|Fehlerbehebung|
|PSDNET-789|Fehlerhaftes Mischen von mehr als einem Ebeneneffekt|Fehlerbehebung|
|PSDNET-805|Fehlerhafte Mischreihenfolge und Logik bei mehreren Ebeneneffekten|Fehlerbehebung|
|PSDNET-842|Eigenschaften des Strich-Effekts werden nicht in die PSD-Datei gespeichert|Fehlerbehebung|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Entfernte APIs:**
- Keine

## **Beispiele:**
**PSDNET-694. Beim Lesen von PattResource wurden Breite und Höhe vertauscht**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // Musterrendering aufrufen

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Fehlerhaftes Mischen von mehr als einem Ebeneneffekt**

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
                                    // Nach der Textebene suchen
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Auf diese Weise wird die geänderte PSD-Datei gespeichert
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Fehlerhafte Mischreihenfolge und Logik bei mehreren Ebeneneffekten**

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

                // Auf diese Weise wird die geänderte PSD-Datei gespeichert
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Fügen Sie die SectionDividerLayer hinzu, um die Erfahrung mit Ebenengruppen zu verbessern**

{{< highlight csharp >}}
            // Der folgende Code zeigt SectionDividerLayer-Ebenen und wie Sie die zugehörige LayerGroup erhalten.

            // Ebenenhierarchie
            //    [0]: '</Layer group>' SectionDividerLayer für Gruppe 1
            //    [1]: 'Ebene 1' Reguläre Ebene
            //    [2]: '</Layer group>' SectionDividerLayer für Gruppe 2
            //    [3]: '</Layer group>' SectionDividerLayer für Gruppe 3
            //    [4]: 'Gruppe 3' GruppenEbene
            //    [5]: 'Gruppe 2' GruppenEbene
            //    [6]: 'Gruppe 1' GruppenEbene

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekte sind nicht gleich.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Ebenenhierarchie erstellen
                // Fügen Sie die LayerGroup 'Gruppe 1' hinzu
                LayerGroup group1 = image.AddLayerGroup("Gruppe 1", 0, true);
                // Normale Ebene hinzufügen
                Layer layer1 = new Layer();
                layer1.DisplayName = "Ebene 1";
                group1.AddLayer(layer1);
                // Fügen Sie die LayerGroup 'Gruppe 2' hinzu
                LayerGroup group2 = group1.AddLayerGroup("Gruppe 2", 1);
                // Fügen Sie die LayerGroup 'Gruppe 3' hinzu
                LayerGroup group3 = group2.AddLayerGroup("Gruppe 3", 0);

                // Erhält die SectionDividerLayer
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // Mit der Methode SectionDividerLayer.GetRelatedLayerGroup() wird die zugehörige LayerGroup-Instanz abgerufen.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // die gleiche LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // die gleiche LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // die gleiche LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Gruppe 1' enthält 5 Ebenen
            }
{{< /highlight >}}

**PSDNET-842. Eigenschaften des Strich-Effekts werden nicht in die PSD-Datei gespeichert**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objekte sind nicht gleich.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Wirft keine ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Überprüft gespeicherte Werte
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

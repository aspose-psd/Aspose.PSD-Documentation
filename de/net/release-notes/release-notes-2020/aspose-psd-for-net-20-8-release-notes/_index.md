---
title: Aspose.PSD für .NET 20.8 - Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-psd-für-net-20-8-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-390|Unterstützung von PlLdResource (Platzierte Ressource für Smart Object Layer)|Feature|
|PSDNET-400|Unterstützung von SoLdResource (Smart Object Layer Data-Ressource)|Feature|
|PSDNET-693|Hinzufügen von Unterstützung für Objekt- und Einheits-Array-Strukturen: ObAr / UnFl-Signaturen|Feature|
|PSDNET-600|Problembehebung beim Speichern von modifizierten PSD-Bildern mit CMYK-Farbraum 16 Bit pro Kanal|Fehler|
|PSDNET-664|Unterstreichung und Durchstreichung gehen nach dem Fokussieren auf den Text in der Datei, die mit Aspose.PSD gespeichert wurde, verloren|Fehler|
|PSDNET-710|Regression: Aspose.PSD 20.7.0 verändert Schriftgrößen für ältere Dateien|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])

## **Beispiele**

**PSDNET-693. Hinzufügen von Unterstützung für Objekt- und Einheits-Array-Strukturen: ObAr / UnFl-Signaturen**
{{< highlight csharp >}}
            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
                }
            }

            string dataDir = "PSDNET693_1\\";
            var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";

{{< /highlight >}}

**PSDNET-600. Problembehebung beim Speichern von modifizierten PSD-Bildern mit CMYK-Farbraum 16 Bit pro Kanal**
{{< highlight csharp >}}
            using (PsdImage image = (PsdImage)Image.Load("cub16bit_cmyk.psd"))
            {
                RasterCachedImage raster = image.Layers[0];
                Aspose.PSD.Graphics graphics = new Graphics(raster);
                int width = raster.Width;
                int height = raster.Height;
                Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);
                graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1),  rect);
                image.Save("output.png", new PngOptions());
            }
{{< /highlight >}}

**PSDNET-664. Unterstreichung und Durchstreichung gehen nach dem Fokussieren auf den Text in der Datei, die mit Aspose.PSD gespeichert wurde, verloren**
{{< highlight csharp >}}
            string sourceFile = "source.psd";
            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var layers = image.Layers;
                var textLayer = (TextLayer)layers[1];

                textLayer.TextData.Items[0].Style.Underline = true;
                textLayer.TextData.Items[1].Style.Strikethrough = true;

                textLayer.TextData.UpdateLayerData();

                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-710. Regression: Aspose.PSD 20.7.0 verändert Schriftgrößen für ältere Dateien**
{{< highlight csharp >}}
            string srcFile = "font_size_lost.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[0];
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFilePng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-693. Hinzufügen von Unterstützung für Objekt- und Einheits-Array-Strukturen: ObAr / UnFl-Signaturen**
{{< highlight csharp >}}
            void AssertAreEqual(object actual, object expected)
            {
                if (!object.Equals(actual, expected))
                {
                    throw new FormatException(string.Format("Actual value {0} are not equal to expected {1}.", actual, expected));
                }
            }

            string dataDir = "PSDNET693_1\\";
            var sourceFilePath = dataDir + "LayeredSmartObjects8bit2.psd";
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                UnitArrayStructure verticalStructure = null;
                foreach (Layer imageLayer in image.Layers)
                {
                    foreach (var imageResource in imageLayer.Resources)
                    {
                        var resource = imageResource as PlLdResource;
                        if (resource != null && resource.IsCustom)
                        {
                            foreach (OSTypeStructure structure in resource.Items)
                            {
                                if (structure.KeyName.ClassName == "customEnvelopeWarp")
                                {
                                    AssertAreEqual(typeof(DescriptorStructure), structure.GetType());
                                    var custom = (DescriptorStructure)structure;
                                    AssertAreEqual(custom.Structures.Length, 1);
                                    var mesh = custom.Structures[0];
                                    AssertAreEqual(typeof(ObjectArrayStructure), mesh.GetType());
                                    var meshObjectArray = (ObjectArrayStructure)mesh;
                                    AssertAreEqual(meshObjectArray.Structures.Length, 2);
                                    var vertical = meshObjectArray.Structures[1];
                                    AssertAreEqual(typeof(UnitArrayStructure), vertical.GetType());
                                    verticalStructure = (UnitArrayStructure)vertical;
                                    AssertAreEqual(verticalStructure.UnitType, UnitTypes.Pixels);
                                    AssertAreEqual(verticalStructure.ValueCount, 16);

                                    break;
                                }
                            }
                        }
                    }
                }

                AssertAreEqual(true, verticalStructure != null);
            }
{{< /highlight >}}

**PSDNET-600. Problembehebung beim Speichern von modifizierten PSD-Bildern mit CMYK-Farbraum 16 Bit pro Kanal**
{{< highlight csharp >}}
            using (PsdImage image = (PsdImage)Image.Load("cub16bit_cmyk.psd"))
            {
                RasterCachedImage raster = image.Layers[0];
                Aspose.PSD.Graphics graphics = new Graphics(raster);
                int width = raster.Width;
                int height = raster.Height;
                Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);
                graphics.DrawRectangle(new Aspose.PSD.Pen(Color.DarkGray, 1),  rect);
                image.Save("output.png", new PngOptions());
            }
{{< /highlight >}}

**PSDNET-664. Unterstreichung und Durchstreichung gehen nach dem Fokussieren auf den Text in der Datei, die mit Aspose.PSD gespeichert wurde, verloren**
{{< highlight csharp >}}
            string sourceFile = "source.psd";
            string outputFile = "output.psd";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var layers = image.Layers;
                var textLayer = (TextLayer)layers[1];

                textLayer.TextData.Items[0].Style.Underline = true;
                textLayer.TextData.Items[1].Style.Strikethrough = true;

                textLayer.TextData.UpdateLayerData();

                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-710. Regression: Aspose.PSD 20.7.0 verändert Schriftgrößen für ältere Dateien**
{{< highlight csharp >}}
            string srcFile = "font_size_lost.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                var textLayer = (TextLayer)psdImage.Layers[0];
                textLayer.TextData.UpdateLayerData();

                psdImage.Save(outputFilePng, new PngOptions());
            }
{{< /highlight >}}
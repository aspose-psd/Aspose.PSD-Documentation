---
title: Aspose.PSD für .NET 20.10 - Versionshinweise
type: docs
weight: 30
url: /de/net/aspose-psd-fur-net-20-10-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-565|Ausnahme beim Speichern der spezifischen PSD-Datei mit Textebenen|Fehler|
|PSDNET-680|Schriftarten gehen nach Rundgängen mit Aspose.PSD verloren|Fehler|
|PSDNET-704|Rendern der Smart Object-Layer|Feature|
|PSDNET-707|Unterstützung der Smart Object nicht-destruktive Transformationen|Feature|
|PSDNET-711|Textebene wird nach dem Speichern ohne Änderungen verschoben|Fehler|
|PSDNET-720|Aspose.PSD 20.8: Ausnahme bei der Psd-zu-Tiff-Konvertierung|Fehler|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Keine
# **Entfernte APIs:**
- Keine

## **Verwendungsbeispiele:**
**PSDNET-565. Ausnahme beim Speichern der spezifischen PSD-Datei mit Textebenen**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Schriftarten gehen nach Rundgängen mit Aspose.PSD verloren**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("Die Werte sind nicht gleich.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Rendern der Smart Object-Layer**
{{< highlight csharp >}}
            // Dieses Beispiel zeigt, wie der Inhalt der Adobe® Photoshop® Smart Object-Layer ersetzt und korrekt gerendert wird.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Dieses Beispiel zeigt, wie der Bildcache der Adobe® Photoshop® Smart Object-Layer aktualisiert und korrekt gerendert wird.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. Unterstützung der Smart Object nicht-destruktiven Transformationen**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Diese Beispiele zeigen nicht-destruktive Transformationen der PSD-Datei mit SmartObjectLayer.
            // Wir können eine Ebene skalieren, drehen, neigen, verzerren, perspektivisch transformieren oder verzerren,
            // ohne Originale Bilddaten oder Qualität zu verlieren, da die Transformationen die Originaldaten nicht beeinflussen.

            // Dieses Beispiel zeigt, wie das Adobe® Photoshop® Bild mit Smart Object-Layern skaliert wird:
            BeispielFürSmartObjectBildSkalierung("new_panama-papers-8-trans4-linked");
            BeispielFürSmartObjectBildSkalierung("picture-frame-4-linked3");
            BeispielFürSmartObjectBildSkalierung("gorilla");

            // Dieses Beispiel zeigt, wie die PSD-Datei mit Smart Object-Layern skaliert wird.
            void BeispielFürSmartObjectBildSkalierung(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie die Adobe® Photoshop® Smart Object-Layer skaliert wird.
            BeispielFürSmartObjectLayerSkalierung("new_panama-papers-8-trans4-linked");
            BeispielFürSmartObjectLayerSkalierung("gorilla");

            // Dieses Beispiel zeigt, wie eine Smart Object-Layer in der PSD-Datei skaliert wird.
            void BeispielFürSmartObjectLayerSkalierung(string fileName)
            {
                const double scale = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int newWidth = (int)(smartObjectLayer.Width * scale);
                    int newHeight = (int)(smartObjectLayer.Height * scale);
                    smartObjectLayer.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie die Adobe® Photoshop® Smart Object-Layer zugeschnitten wird.
            BeispielFürSmartObjectLayerZuschneiden("new_panama-papers-8-trans4-linked");
            BeispielFürSmartObjectLayerZuschneiden("gorilla");

            // Dieses Beispiel zeigt, wie eine Smart Object-Layer in der PSD-Datei zugeschnitten wird.
            void BeispielFürSmartObjectLayerZuschneiden(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CropLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "CropLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie das Adobe® Photoshop® Bild mit Smart Object-Layern rotiert und gespiegelt wird:
            BeispielFürSmartObjectBildRotationSpiegelung("gorilla", RotateFlipType.Rotate90FlipNone);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            BeispielFürSmartObjectBildRotationSpiegelung("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Dieses Beispiel zeigt, wie die PSD-Datei mit Smart Object-Layern rotiert und gespiegelt wird.
            void BeispielFürSmartObjectBildRotationSpiegelung(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie die Adobe® Photoshop® Smart Object-Layer rotiert und gespiegelt wird.
            BeispielFürSmartObjectLayerRotationSpiegelung("gorilla", RotateFlipType.Rotate90FlipNone);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            BeispielFürSmartObjectLayerRotationSpiegelung("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Dieses Beispiel zeigt, wie die Smart Object-Layer in der PSD-Datei rotiert und gespiegelt wird.
            void BeispielFürSmartObjectLayerRotationSpiegelung(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "Last_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "Last_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie die Adobe® Photoshop® Smart Object-Layer um einen beliebigen Winkel rotiert wird:
            const string AngleFormat = "+#;-#;+0";
            BeispielFürSmartObjectLayerRotation("gorilla", 45, false);
            BeispielFürSmartObjectLayerRotation("gorilla", 45, true);
            BeispielFürSmartObjectLayerRotation("r3-embedded-transform2", -30, true);
            BeispielFürSmartObjectLayerRotation("r3-embedded-transform2", -30, false);
            BeispielFürSmartObjectLayerRotation("new_panama-papers-8-trans4-linked", 190, false);
            BeispielFürSmartObjectLayerRotation("new_panama-papers-8-trans4-linked", 190, true);

            // Dieses Beispiel zeigt, wie eine Smart Object-Layer in der PSD-Datei um einen beliebigen Winkel rotiert wird.
            void BeispielFürSmartObjectLayerRotation(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "RotateLast" +  angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefix + fileName + ".psd";
                string outputPngPath = outputDir + prefix + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Rotate(angle, resizeProportionally, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Dieses Beispiel zeigt, wie das Adobe® Photoshop® Bild mit Smart Object-Layer um einen beliebigen Winkel rotiert wird
            BeispielFürSmartObjectBildRotation("gorilla", 45, false);
            BeispielFürSmartObjectBildRotation("new_panama-papers-8-trans4-linked", -30, false);

            // Dieses Beispiel zeigt, wie die PSD-Datei mit Smart Object-Layern um einen beliebigen Winkel rotiert wird.
            void BeispielFürSmartObjectBildRotation(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "Rotate" +  angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefix + fileName + ".psd";
                string outputPngPath = outputDir + prefix + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Rotate(angle, resizeProportionally, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-711. Textebene wird nach dem Speichern ohne Änderungen verschoben**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("Die Werte sind gleich.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual(txtLayer.Top, txtLayer.TransformMatrix[5]);
            }
{{< /highlight >}}
**PSDNET-720. Aspose.PSD 20.8: Psd-zu-Tiff Konvertierungsausnahme**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}
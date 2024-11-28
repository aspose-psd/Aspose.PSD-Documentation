---
title: Aspose.PSD for .NET 20.10 - リリースノート
type: docs
weight: 30
url: /ja/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

このページは [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートを含んでいます。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-565|特定のテキストレイヤーを持つPSDファイルの保存時に例外が発生する|バグ|
|PSDNET-680|Aspose.PSDを介したラウンドトリップ後にフォントが失われる|バグ|
|PSDNET-704|Smart Object レイヤーのレンダリング|機能|
|PSDNET-707|Smart Object 非破壊変換のサポート|機能|
|PSDNET-711|変更なしで保存した後、テキストレイヤーがシフトする|バグ|
|PSDNET-720|Aspose.PSD 20.8: Psd を Tiff に変換する際の例外|バグ|

## **公開 API 変更**
# **追加された API:**
- なし
# **削除された API:**
- なし

## **使用例:**
**PSDNET-565. 特定のテキストレイヤーを持つPSDファイルの保存時に例外が発生する**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Aspose.PSDを介したラウンドトリップ後にフォントが失われる**
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
                    throw new Exception("Values are not equal.");
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
**PSDNET-704. Smart Object レイヤーのレンダリング**
{{< highlight csharp >}}
            // この例は、Adobe® Photoshop® のスマートオブジェクトレイヤーの内容を置き換えて正しくレンダリングする方法を示しています。
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

            // この例は、Adobe® Photoshop® のスマートオブジェクトレイヤーの画像キャッシュを更新して正しくレンダリングする方法を示します。
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
**PSDNET-707. Smart Object 非破壊変換のサポート**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // これらの例では、SmartObjectLayer を持つ PSD ファイルの非破壊変換を示しています。
            // オリジナルのイメージデータや品質が変化しないため、変換は元のデータに影響を与えません。

            // この例は、Adobe® Photoshop® イメージのスマートオブジェクトレイヤーのリサイズ方法を示しています:
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // この例は、スマートオブジェクトレイヤーを持つ PSD ファイルのリサイズ方法を示しています。
            void ExampleOfSmartObjectImageResizeSupport(string fileName)
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

            // この例は、Adobe® Photoshop® スマートオブジェクトレイヤーのリサイズ方法を示しています:
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // この例は、PSD ファイル内のスマートオブジェクトレイヤーのリサイズ方法を示しています。
            void ExampleOfSmartObjectLayerResizeSupport(string fileName)
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

            // この例は、Adobe® Photoshop® スマートオブジェクトレイヤーの切り取り方法を示しています。
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // この例は、PSD ファイル内のスマートオブジェクトレイヤーの切り取り方法を示しています。
            void ExampleOfSmartObjectLayerCropSupport(string fileName)
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

            // この例は、Adobe® Photoshop® スマートオブジェクトレイヤーの切り取り方法を示しています:
            ExampleOfSmartObjectImageCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageCropSupport("gorilla");

            // この例は、スマートオブジェクトレイヤーを持つ PSD ファイルの切り取り方法を示しています。
            void ExampleOfSmartObjectImageCropSupport(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Crop_" + fileName + ".psd";
                string outputPngPath = outputDir + "Crop_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // この例は、Adobe® Photoshop® イメージのスマートオブジェクトレイヤーを回転および反転する方法を示しています:
            ExampleOfSmartObjectImageRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // この例は、PSD ファイル内のスマートオブジェクトレイヤーを回転および反転する方法を示しています。
            void ExampleOfSmartObjectImageRotateFlipSupport(string fileName, RotateFlipType rotateFlipType)
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

            // この例は、Adobe® Photoshop® スマートオブジェクトレイヤーを回転および反転する方法を示しています：
            ExampleOfSmartObjectLayerRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // この例は、PSD ファイル内のスマートオブジェクトレイヤーを回転および反転する方法を示しています。
            void ExampleOfSmartObjectLayerRotateFlipSupport(string fileName, RotateFlipType rotateFlipType)
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

            // この例は、Adobe® Photoshop® スマートオブジェクトレイヤーを任意の角度で回転する方法を示しています：
            const string AngleFormat = "+#;-#;+0";
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, true);

            // この例は、PSD ファイル内のスマートオブジェクトレイヤーを任意の角度で回転する方法を示します。
            void ExampleOfSmartObjectLayerRotateSupport(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "RotateLast" + angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportionally" : "") + "_";
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

            // この例は、Adobe® Photoshop® イメージのスマートオブジェクトレイヤーを任意の角度で回転する方法を示しています:
            ExampleOfSmartObjectImageRotateSupport("gorilla", 45, false
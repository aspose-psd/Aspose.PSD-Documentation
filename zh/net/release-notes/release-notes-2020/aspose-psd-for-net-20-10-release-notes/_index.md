---
title: Aspose.PSD for .NET 20.10 - 发行说明
type: docs
weight: 30
url: /zh/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

本页包含了 [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-565|保存具有文本层的特定PSD文件时出现异常|Bug|
|PSDNET-680|使用 Aspose.PSD 后字体丢失|Bug|
|PSDNET-704|智能对象图层的渲染|功能|
|PSDNET-707|智能对象非破坏性变换的支持|功能|
|PSDNET-711|在没有任何更改的情况下保存后文本图层位置发生偏移|Bug|
|PSDNET-720|Aspose.PSD 20.8: Psd 转 Tiff 转换异常|Bug|

## **公共API更改**
# **已添加的API:**
- 无
# **已删除的API:**
- 无

## **用法示例:**
**PSDNET-565. 保存具有文本层的特定PSD文件时出现异常**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. 使用 Aspose.PSD 后字体丢失**
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
                    throw new Exception("数值不相等。");
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
**PSDNET-704. 智能对象图层的渲染**
{{< highlight csharp >}}
            // 此示例演示如何替换 Adobe® Photoshop® 智能对象图层的内容并正确渲染。
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

            // 此示例演示如何更新 Adobe® Photoshop® 智能对象图层的图像缓存并正确渲染。
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
**PSDNET-707. 智能对象非破坏性变换的支持**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // 这些示例演示了具有 SmartObjectLayer 的 PSD 文件的非破坏性变换。
            // 我们可以对图层进行缩放、旋转、扭曲、透视变换或形变，而不会丢失原始图像数据
            // 或质量，因为这些变换不会影响原始数据。

            // 此示例演示如何调整 Adobe 
            // Photoshop® 图像以及智能对象图层的大小：
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // 此示例演示如何调整具有智能对象图层的 PSD 文件的大小。
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

            // 此示例演示如何调整 Adobe® Photoshop® 智能对象图层的大小。
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // 此示例演示如何调整 PSD 文件中智能对象图层的大小。
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

            // 此示例演示如何裁剪 Adobe® Photoshop® 智能对象图层。
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // 此示例演示如何裁剪 PSD 文件中的智能对象图层。
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

            // 此示例演示如何裁剪 Adobe® Photoshop® 智能对象图层。
            ExampleOfSmartObjectImageCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageCropSupport("gorilla");

            // 此示例演示如何裁剪具有智能对象图层的 PSD 文件。
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

            // 此示例演示如何旋转和翻转 Adobe® Photoshop® 图像与智能对象图层：
            ExampleOfSmartObjectImageRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // 此示例演示如何旋转和翻转具有智能对象图层的 PSD 文件。
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

            // 此示例演示如何旋转和翻转 Adobe® Photoshop® 智能对象图层。
            ExampleOfSmartObjectLayerRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // 此示例演示如何在 PSD 文件中旋转和翻转智能对象图层。
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

            // 此示例演示如何以任意角度旋转 Adobe® Photoshop® 智能对象图层：
            const string AngleFormat = "+#;-#;+0";
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, true);

            // 此示例演示如何以任意角度旋转 PSD 文件中的智能对象图层。
            void ExampleOfSmartObjectLayerRotateSupport(string fileName, float angle, bool resizeProportionally)
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

            // 此示例演示如何以任意角度旋转 Adobe® Photoshop® 图像与智能对象图层：
            ExampleOfSmartObjectImageRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectImageRotateSupport("new_panama-papers-8-trans4-linked", -30, false);

            // 此示例演示如何以任意角度旋转具有智能对象图层的 PSD 文件。
            void ExampleOfSmartObjectImageRotateSupport(string fileName, float angle, bool resizeProportionally)
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
**PSDNET-711. 在没有任何更改的情况下保存后文本图层位置发生偏移**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object
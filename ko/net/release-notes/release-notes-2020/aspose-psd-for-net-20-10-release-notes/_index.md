---
title: Aspose.PSD for .NET 20.10 - 릴리스 노트
type: docs
weight: 30
url: /ko/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-565|텍스트 레이어가 포함된 특정 PSD 파일을 저장할 때 예외 발생|버그|
|PSDNET-680|Aspose.PSD와의 라운드 트립 후에 글꼴이 손실됨|버그|
|PSDNET-704|Smart Object 레이어 렌더링|기능|
|PSDNET-707|Smart Object 비파괴적 트랜스폼 지원|기능|
|PSDNET-711|변경 사항 없이 저장한 후 텍스트 레이어가 이동됨|버그|
|PSDNET-720|Aspose.PSD 20.8: Psd에서 Tiff로 변환할 때 예외 발생|버그|

## **공개 API 변경**
# **추가된 API:**
- 없음
# **제거된 API:**
- 없음

## **사용 예시:**
**PSDNET-565. 텍스트 레이어가 포함된 특정 PSD 파일을 저장할 때 예외 발생**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Asposed.PSD와의 라운드 트립 후에 글꼴이 손실됨**
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
                    throw new Exception("값이 같지 않습니다.");
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
**PSDNET-704. Smart Object 레이어 렌더링**
{{< highlight csharp >}}
            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어의 내용을 교체하고 올바른 렌더링을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어의 이미지 캐시를 업데이트하고 올바른 렌더링을 보여줍니다.
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
**PSDNET-707. Smart Object 비파괴적 트랜스폼 지원**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // 이 예는 SmartObjectLayer를 포함한 PSD 파일의 비파괴적 트랜스폼을 보여줍니다.
            // 스케일링, 회전, 기울이기, 왜곡, 원근 변형 또는 그림자를 생성하지 않는 변형을 통해
            // 원본 이미지 데이터나 품질을 손상시키지 않고 레이어를 조정할 수 있습니다.

            // 이 예는 Adobe® Photoshop® 이미지의 Smart Object Layer를 조정하는 방법을 보여줍니다.
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // 이 예는 Smart Object Layer를 포함한 PSD 파일을 조정하는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어를 조정하는 방법을 보여줍니다.
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // 이 예는 PSD 파일의 스마트 오브젝트 레이어를 조정하는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어를 자르는 방법을 보여줍니다.
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // 이 예는 PSD 파일에서 스마트 오브젝트 레이어를 자르는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어를 자르는 방법을 보여줍니다:
            ExampleOfSmartObjectImageCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageCropSupport("gorilla");

            // 이 예는 스마트 오브젝트 레이어가 포함된 PSD 파일을 자르는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 이미지의 스마트 오브젝트 레이어를 회전하고 뒤집는 방법을 보여줍니다:
            ExampleOfSmartObjectImageRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // 이 예는 PSD 파일의 스마트 오브젝트 레이어를 회전하고 뒤집는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어를 회전하고 뒤집는 방법을 보여줍니다.
            ExampleOfSmartObjectLayerRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // 이 예는 PSD 파일의 스마트 오브젝트 레이어를 회전하고 뒤집는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 스마트 오브젝트 레이어를 원하는 각도로 회전하는 방법을 보여줍니다:
            const string AngleFormat = "+#;-#;+0";
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, true);

            // 이 예는 PSD 파일의 스마트 오브젝트 레이어를 원하는 각도로 회전하는 방법을 보여줍니다.
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

            // 이 예는 Adobe® Photoshop® 이미지의 스마트 오브젝트 레이어를 원하는 각도로 회전하는 방법을
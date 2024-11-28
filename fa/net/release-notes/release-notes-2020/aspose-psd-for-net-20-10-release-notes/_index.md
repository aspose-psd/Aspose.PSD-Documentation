---
title: یادداشت‌های انتشار Aspose.PSD برای .NET 20.10
type: docs
weight: 30
url: /fa/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/) است.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-565|استثنا در ذخیره فایل PSD خاص با لایه‌های متنی|باگ|
|PSDNET-680|فونت‌ها پس از سیکل‌های تغییر Aspose.PSD از دست داده می‌شوند|باگ|
|PSDNET-704|رندرینگ لایه شیوه‌ی هوشمند|ویژگی|
|PSDNET-707|پشتیبانی از تبدیل‌های غیرازیبی لایه شیوه‌هوشمند|ویژگی|
|PSDNET-711|لایه متنی پس از ذخیره بدون هیچ تغییری منزوی می‌شود|باگ|
|PSDNET-720|استثنای تبدیل Psd به Tiff Aspose.PSD 20.8|باگ|

## **تغییرات API عمومی**
# **API‌های اضافه‌شده:**
- هیچکدام
# **API‌های حذف‌شده:**
- هیچکدام

## **مثال‌های استفاده:**
**PSDNET-565. استثنا در ذخیره فایل PSD خاص با لایه‌های متنی**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. فونت‌ها پس از سیکل‌های تغییر Aspose.PSD از دست داده می‌شوند**
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
                    throw new Exception("مقادیر برابر نیستند.");
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
**PSDNET-704. رندرینگ لایه شیوه‌هوشمند**
{{< highlight csharp >}}
            // این مثال نشان می‌دهد چگونه محتوای لایه شیوه‌هوشمند فتوشاپ را جایگزین کنید و رندر صحیح آن را ارائه دهید.
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

            // این مثال نشان می‌دهد چگونه کش تصویر لایه‌های شیوه هوشمند فتوشاپ را به روز کنید و رندر صحیح آن‌ها را انجام دهید.
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
**PSDNET-707. پشتیبانی از تبدیل‌‌های غیرازیبی لایه شیوه‌‌هوشمند**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // این مثال‌ها تبدیل‌های غیرازیبی فایل PSD با SmartObjectLayer را نمایش می‌دهند.
            // ما می‌توانیم یک لایه‌ی تصویر را بدون کوچک‌کردن، چرخاندن، خمیدن، تغییر چشم‌انداز، یا انحراف بدهیم
            // بدون از دست دادن داده یا کیفیت تصویر اصلی زیرا تبدیلات تصاویر اصلی تغییر نمی‌ده.

            // این مثال نشان می‌دهد چگونه تصویر فتوشاپ را با لایه‌های SmartObject تغییر اندازه دهید:
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // این مثال نشان می‌دهد چگونه فایل PSD را با لایه‌های SmartObject تغییر اندازه دهید.
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

            // این مثال نشان می‌دهد چگونه لایه‌ی SmartObject فتوشاپ را تغییر اندازه دهید.
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // این مثال نشان می‌دهد چگونه لایه‌ی SmartObject یک لایه در فایل PSD را تغییر اندازه دهید.
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

            // این مثال نشان می‌دهد چگونه لایه‌ی SmartObject فتوشاپ را قطع کنید.
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // این مثال نشان می‌دهد چگونه یک لایه‌ی SmartObject در فایل PSD را قطع کنید.
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

            // این مثال نشان می‌دهد چگونه تصویر فتوشاپ را با لایه‌های SmartObject چرخانید و وارونه کنید:
            ExampleOfSmartObjectImageRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectImageRotateFlipSupport("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // این مثال نشان می‌دهد چگونه یک فایل PSD با لایه‌های SmartObject چرخیده و وارونه شده را ذخیره کنید.
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

            // این مثال نشان می‌دهد چگونه لایه‌ی SmartObject فتوشاپ را چرخانید و وارونه کنید.
            ExampleOfSmartObjectLayerRotateFlipSupport("gorilla", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExampleOfSmartObjectLayerRotateFlipSupport("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // این مثال نشان می‌دهد چگونه یک لایه‌ی SmartObject در فایل PSD را چرخانید و وارونه کنید.
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

            // این مثال نشان می‌دهد چگونه یک لایه‌ی SmartObject فتوشاپ را به هر زاویه‌ای چرخانید:
            const string AngleFormat = "+#;-#;+0";
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, false);
            ExampleOfSmartObjectLayerRotateSupport("gorilla", 45, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, true);
            ExampleOfSmartObjectLayerRotateSupport("r3-embedded-transform2", -30, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, false);
            ExampleOfSmartObjectLayerRotateSupport("new_panama-papers-8-trans4-linked", 190, true);

            // این مثال نشان می‌دهد چگونه یک لایه‌ی SmartObject در فایل PSD را به هر زاویه‌ای چرخانید.
            void ExampleOfSmartObjectLayerRotateSupport(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "RotateLast" +  angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportion
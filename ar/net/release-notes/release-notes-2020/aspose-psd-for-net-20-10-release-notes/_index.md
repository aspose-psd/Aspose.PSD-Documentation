---
title: ملاحظات الإصدار Aspose.PSD for .NET 20.10
type: docs
weight: 30
url: /ar/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-565|استثناء عند حفظ ملف PSD مع طبقات نص معينة|خلل|
|PSDNET-680|تفقد الخطوط بعد جولات متعددة مع Aspose.PSD|خلل|
|PSDNET-704|عرض طبقة الكائن الذكي|ميزة|
|PSDNET-707|دعم التحويلات غير المدمرة للكائن الذكي|ميزة|
|PSDNET-711|تحريك طبقة النص بعد الحفظ دون أي تغييرات|خلل|
|PSDNET-720|استثناء تحويل PSD إلى Tiff في Aspose.PSD 20.8|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المُضافة:**
- لا شيء
# **APIs المُحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**
**PSDNET-565. استثناء عند حفظ ملف PSD مع طبقات نص محددة**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. تفقد الخطوط بعد جولات متعددة مع Aspose.PSD**
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
                    throw new Exception("ليست القيم متساوية.");
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
**PSDNET-704. عرض طبقة الكائن الذكي**
{{< highlight csharp >}}
            // في هذا المثال نقدم كيفية استبدال محتوى طبقة الكائن الذكي في Adobe® Photoshop® وعمله بشكل صحيح.
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

            // في هذا المثال نقدم كيفية تحديث ذاكرة التخزين المؤقت لطبقات الكائن الذكي في Adobe® Photoshop® وعملها بشكل صحيح.
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
**PSDNET-707. دعم التحويلات غير المدمرة للكائن الذكي**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // هذه الأمثلة توضح التحويلات غير المدمرة لملف PSD مع طبقة SmartObjectLayer.
            // يمكننا تغيير مقياس، وتدوير، وميل، وتشويه، وتحويل الوجهة، أو تشويه الطبقة من دون فقدان البيانات أو الجودة الأصلية للصورة لأن التحويلات لا تؤثر على البيانات الأصلية.

            // يوضح هذا الأمثلة كيفية تغيير حجم الصورة Adobe® Photoshop® مع طبقات SmartObject.
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // يوضح هذا المثال كيفية تغيير حجم ملف PSD مع طبقات SmartObject.
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

            // يوضح هذا المثال كيفية تغيير حجم طبقة الكائن الذكي في ملف PSD.
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // يوضح هذا المثال كيفية تغيير حجم طبقة SmartObject في ملف PSD.
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

            // يوضح هذا المثال كيفية قص طبقة الكائن الذكي في ملف PSD.
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // يوضح هذا المثال كيفية قص طبقة SmartObject في ملف PSD.
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
{{< /highlight >}}
**PSDNET-711. تحريك طبقة النص بعد الحفظ دون أي تغييرات**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("القيم متساوية.");
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
**PSDNET-720. استثناء تحويل PSD إلى Tiff في Aspose.PSD 20.8**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}
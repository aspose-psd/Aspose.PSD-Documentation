---
title: دفترچه یادداشت نسخه Aspose.PSD برای .NET 21.3
type: docs
weight: 100
url: /fa/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار [Aspose.PSD برای .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/​) می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته بندی**|
|:-|:-|:-|
|PSDNET-823|افزودن SectionDividerLayer برای بهبود تجربه با گروه‌های لایه|بهبود|
|PSDNET-694|هنگام خواندن PattResource، عرض و ارتفاع اشتباه تعویض شد|اشکال|
|PSDNET-789|ترکیب نادرست از بیش از یک اثر لایه|اشکال|
|PSDNET-805|ترتیب و منطق ترکیب نادرست وقتی بیش از یک اثر لایه وجود دارد|اشکال|
|PSDNET-842|خواص اثر Stroke در فایل PSD ذخیره نمی‌شوند|اشکال|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDNET-694. هنگام خواندن PattResource، عرض و ارتفاع اشتباه تعویض شد**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // فراخوانی پترن رندر

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. ترکیب نادرست از بیش از یک اثر لایه**

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
                                    // در حال جستجو برای لایه متن
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "بهترین";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // به این روش ما فایل PSD تغییر‌یافته را ذخیره می‌کنیم
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. ترتیب و منطق ترکیب نادرست وقتی بیش از یک اثر لایه وجود دارد**

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

                //به این روش ما فایل PSD تغییر‌یافته را ذخیره می‌کنیم
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. اضافه کردن SectionDividerLayer برای بهبود تجربه با گروه‌های لایه**

{{< highlight csharp >}}
            // کد زیر لایه‌های SectionDividerLayer و چگونگی دریافت مربوط به آن LayerGroup را نشان می‌دهد.

            // سلسله‌مراتب لایه‌ها
            //    [0]: '</Layer group>' لایه SectionDividerLayer برای گروه 1
            //    [1]: 'Layer 1' لایه معمولی
            //    [2]: '</Layer group>' لایه SectionDividerLayer برای گروه 2
            //    [3]: '</Layer group>' لایه SectionDividerLayer برای گروه 3
            //    [4]: 'گروه 3' لایه GroupLayer
            //    [5]: 'گروه 2' لایه GroupLayer
            //    [6]: 'گروه 1' لایه GroupLayer

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "اشیاء برابر نیستند.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // ایجاد سلسله‌مراتب لایه‌ها
                // اضافه کردن لایه‌گروه 'گروه 1'
                LayerGroup group1 = image.AddLayerGroup("گروه 1", 0, true);
                // اضافه کردن لایه معمولی
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // اضافه کردن لایه‌گروه 'گروه 2'
                LayerGroup group2 = group1.AddLayerGroup("گروه 2", 1);
                // اضافه کردن لایه‌گروه 'گروه 3'
                LayerGroup group3 = group2.AddLayerGroup("گروه 3", 0);

                // گرفتن SectionDividerLayer ها
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // با استفاده از متد SectionDividerLayer.GetRelatedLayerGroup()، نمونه آگاه منظوری LayerGroup را به دست می‌آورد.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // همان LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // همان LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // همان LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'گروه 1' شامل 5 لایه است
            }
{{< /highlight >}}

**PSDNET-842. خواص اثر Stroke در فایل PSD ذخیره نمی‌شوند**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "اشیاء برابر نیستند.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // خطای NullArgumentException را پرت نمی‌کند

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // بررسی مقادیر ذخیره شده
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

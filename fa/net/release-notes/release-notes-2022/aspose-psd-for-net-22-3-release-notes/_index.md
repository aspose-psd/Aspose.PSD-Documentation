---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 22.3
type: docs
weight: 100
url: /fa/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-210|افزودن خصوصیت IsOpen برای گروه لایه|ویژگی|
|PSDNET-643|تصویر PSD با ماسک لایه‌ی raster ماسک‌ها را در هنگام ذخیره کردن به تصویر 16 بیتی PSD از دست می‌دهد|باگ|
|PSDNET-899|حالت ترکیبی Dissolve بر روی پوشه با ماسک اعمال نمی‌شود|باگ|
|PSDNET-1047|فایل خاصی نمی‌تواند پس از ذخیره شدن در Aspose.PSD 21.11 توسط فتوشاپ باز شود|باگ|
|PSDNET-1068|رندر نادرست لایه با حالت ترکیبی Linear Dodge (Add)|باگ|
|PSDNET-1069|لایه پر کردن الگو بعد از بارگذاری استثناء می‌اندازد|باگ|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **API‌های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDNET-210. افزودن خصوصیت IsOpen برای گروه لایه**

{{< highlight csharp >}}
// مثال خواندن و نوشتن خصوصیت IsOpen در زمان اجرا.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. تصویر PSD با ماسک لایه‌ی raster ماسک‌ها را در هنگام ذخیره کردن به تصویر 16 بیتی PSD از دست می‌دهد**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. حالت ترکیبی Dissolve بر روی پوشه با ماسک اعمال نمی‌شود**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. فایل خاصی نمی‌تواند پس از ذخیره شدن در Aspose.PSD 21.11 توسط فتوشاپ باز شود**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // نیاز به باز کردن دستی فایل PSD خروجی توسط فتوشاپ.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // بدون استثناء.
            }
{{< /highlight >}}

**PSDNET-1068. رندر نادرست لایه با حالت ترکیبی Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. لایه پر کردن الگو باعث پرتاب استثناء در زمان به‌روزرسانی پس از بارگذاری می‌شود**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}

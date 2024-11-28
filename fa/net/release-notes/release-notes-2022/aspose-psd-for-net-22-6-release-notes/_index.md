---
title: اسپوز.پی‌اس‌دی برای .نت 22.6 - یادداشت‌های انتشار
type: مستندات
weight: 70
url: /fa/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای .نت 22.6](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-940|‌ایجاد API برای دریافت هش منحصر به فرد برای لایه‌های مشابه در فایل‌های مختلف|بهبود|
|PSDNET-678|نمایش نادرست لایه پرکننده با الگو در صورتی که الگوها بیش از یکی باشند و ترتیب لایه‌ها تغییر کرده باشد|باگ|
|PSDNET-1125|استثنا در بارگذاری فایل خاص PSD با حالت رنگ CMYK|باگ|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **API‌های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDNET-678. نمایش نادرست لایه پرکننده با الگو در صورتی که الگوها بیش از یکی باشند و ترتیب لایه‌ها تغییر کرده باشد**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. ایجاد API برای دریافت هش منحصر به فرد برای لایه‌های مشابه در فایل‌های مختلف**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        // کدهای اجرایی
    }
}
{{< /highlight >}}

**PSDNET-1125. استثنا در بارگذاری فایل خاص PSD با حالت رنگ CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
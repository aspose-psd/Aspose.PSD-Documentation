---
title: اصلاحیه های Aspose.PSD برای .NET 24.3
type: docs
weight: 100
url: /fa/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل اصلاحیه ها برای [Aspose.PSD برای .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد

{{% /alert %}}

| **کلید**    | **خلاصه**                                                        | **دسته‌بندی** |
|:-----------|:-------------------------------------------------------------------|:------------|
| PSDNET-1914 | [فرمت AI] کاهش زمان بارگذاری تصاویر AI چند صفحه بزرگ       | ارتقاء     |
| PSDNET-1905 | فایل PSD پس از تبدیل از 8 بیت به 16 بیت غیر قابل خواندن شد   | باگ        |
| PSDNET-1906 | فایل PSD پس از تبدیل از 8 بیت به 32 بیت غیر قابل خواندن شد   | باگ        |
| PSDNET-1921 | [فرمت AI] اصلاح نحوه رندرینگ منحنی کوتاه در فایل AI           | باگ        |

## تغییرات API عمومی
# **API های اضافه‌شده:**
- هیچ‌کدام

# **API های حذف شده:**
- هیچ‌کدام

## **مثال‌های استفاده:**

**PSDNET-1905. فایل PSD پس از تبدیل از 8 بیت به 16 بیت غیر قابل خواندن شد**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("منبع جهانی اشتباه است، اولین منبع باید Lr16Resource باشد");
    }
}
{{< /highlight >}}

**PSDNET-1906. فایل PSD پس از تبدیل از 8 بیت به 32 بیت غیر قابل خواندن شد**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("منبع جهانی اشتباه است، اولین منبع باید Lr32Resource باشد");
    }
}
{{< /highlight >}}

**PSDNET-1921. [فرمت AI] اصلاح نحوه رندرینگ منحنی کوتاه در فایل AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

---
title: اصلاحات نسخه Aspose.PSD برای Python via .NET 24.3 - یادداشت‌های انتشار
type: مستندات
weight: 10
url: /fa/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای Python via .NET 24.3](https://pypi.org/project/aspose-psd/) می‌باشد.

{{% /alert %}}

| **کلید**      | **خلاصه**                                                          | **دسته‌بندی**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [فرمت AI] کاهش زمان بارگذاری تصاویر AI چند صفحه بزرگ         | بهبود |
| PSDPYTHON-45 | فایل PSD پس از تبدیل از 8 بیت به 16 بیت غیرقابل‌خواندن شد |     باگ     |
| PSDPYTHON-46 | فایل PSD پس از تبدیل از 8 بیت به 32 بیت غیرقابل‌خواندن شد |     باگ     |
| PSDPYTHON-47 | [فرمت AI] اصلاح نمایش منحنی کوتاه در فایل AI                 |     باگ     |



## **تغییرات API عمومی**
# **API‌های افزوده شده:**
- هیچ یک

# **API‌های حذف شده:**
- هیچ یک


## **مثال‌های استفاده:**

**PSDPYTHON-42. [فرمت AI] کاهش زمان بارگذاری تصاویر AI چند صفحه بزرگ**

{{< highlight python >}}
   # بدون نمونه
{{< /highlight >}}

**PSDPYTHON-45. فایل PSD پس از تبدیل از 8 بیت به 16 بیت غیرقابل‌خواندن شد**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # درست است
                pass
            else:
                raise Exception("منبع جهانی اشتباه است، منبع اول باید منبع Lr16Resource باشد")
{{< /highlight >}}

**PSDPYTHON-46. فایل PSD پس از تبدیل از 8 بیت به 32 بیت غیرقابل‌خواندن شد**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # درست است
                pass
            else:
                raise Exception("منبع جهانی اشتباه است، منبع اول باید منبع Lr32Resource باشد")
{{< /highlight >}}

**PSDPYTHON-47. [فرمت AI] اصلاح نمایش منحنی کوتاه در فایل AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

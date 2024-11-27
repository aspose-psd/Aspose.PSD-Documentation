---
title: دفاتر انتشار Aspose.PSD برای .NET 21.6
type: مستندات
weight: 70
url: /fa/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD برای .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**رده**|
| :- | :- | :- |
|PSDNET-546|پوش عایق برای یک گروه به درستی رندر نمی‌شود|اشکال|
|PSDNET-547|عایق منظم یا بردار برای یک گروه لایه در هنگام رندر نادیده گرفته می‌شود|اشکال|
|PSDNET-647|تصویر PSD با غیرفعال کردن ماسک‌های لایه برداری برای ذخیره‌سازی ماسک‌های برداری فعال می‌شود|اشکال|
|PSDNET-786|استثناء در هنگام ایجاد یک TextLayer با متن بیش از 255 کاراکتر|اشکال|
|PSDNET-900|متن لایه متن روی لینوکس نمی‌تواند رندر شود|بهبود|

## **تغییرات در API عمومی**
# **API‌های اضافه شده:**
- هیچکدام

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDNET-546. پوش عایق برای یک گروه به درستی رندر نمی‌شود**

{{< highlight csharp >}}


            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }


{{< /highlight >}}

**PSDNET-547. عایق منظم یا بردار برای یک گروه لایه در هنگام رندر نادیده گرفته می‌شود**

{{< highlight csharp >}}


        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }


{{< /highlight >}}

**PSDNET-647. تصویر PSD با غیرفعال کردن ماسک‌های لایه برداری برای ذخیره‌سازی ماسک‌های برداری فعال می‌شود**

{{< highlight csharp >}}

            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }


{{< /highlight >}}

**PSDNET-786. استثناء در هنگام ایجاد یک TextLayer با متن بیش از 255 کاراکتر**

{{< highlight csharp >}}

            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }


{{< /highlight >}}

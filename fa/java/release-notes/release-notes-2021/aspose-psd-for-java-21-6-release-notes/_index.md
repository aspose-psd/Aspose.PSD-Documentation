---
title: فراپی کیش‌های Aspose.PSD برای جاوا 21.6 - یادداشت‌های انتشار
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای جاوا 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) می‌باشد {{% /alert %}}

|**کلید**|**خلاصه**|**رده**|
| :- | :- | :- |
|PSDJAVA-351|ماسک گروه برشی به درستی رندر نمی‌شود|اشکال|
|PSDJAVA-352|ماسک منظم یا برداری برای گروه لایه در هنگام رندر کردن نادیده گرفته می‌شود|اشکال|
|PSDJAVA-353|تصویر PSD با غیرفعال کردن ماسک‌های برداری لایه در هنگام ذخیره کردن، ماسک‌های برداری را فعال می‌کند|اشکال|
|PSDJAVA-354|استثناء هنگام ایجاد لایه متن با متنی بیش از 255 کاراکتر|اشکال|

# **تغییرات عمومی API**
# **API‌های افزوده شده:**
- هیچکدام

# **API‌های حذف شده:**
- هیچکدام

# **نمونه‌های استفاده:**

**PSDJAVA-351. ماسک گروه برشی به درستی رندر نمی‌شود**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. ماسک منظم یا برداری برای گروه لایه در هنگام رندر کردن نادیده گرفته می‌شود**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. تصویر PSD با غیرفعال کردن ماسک‌های برداری لایه در هنگام ذخیره کردن، ماسک‌های برداری را فعال می‌کند**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. استثناء هنگام ایجاد لایه متن با متنی بیش از 255 کاراکتر**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

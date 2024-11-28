---
title: یادداشت های نسخه Aspose.PSD برای Java 23.8
type: docs
weight: 40
url: /fa/aspose-psd-for-java-23-8-release-notes/
---

{{% alert color="primary" %}} این صفحه شامل یادداشت های نسخه برای [Aspose.PSD برای Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) می باشد. {{% /alert %}}

| **کلید**      | **خلاصه**                                                                                   | **دسته‌بندی** |
|:-------------|:-------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-518 | افزودن نوع جدید از انحنا (پرچم)                                                        |    قابلیت     |
| PSDJAVA-519 | افزودن انواع جدیدی از انحنا: قوس بالا، قوس پایین، کره                                   |    قابلیت     |
| PSDJAVA-520 | پیاده سازی متد جدید PsdImage.AddPosterizeAdjustmentLayer برای اضافه کردن لایه جدید پوسترایز    |    قابلیت     |
| PSDJAVA-521 | اطلاعات PSD در حالت فقط باز کردن و ذخیره کردن از دست رفته است                             |      باگ      |
| PSDJAVA-522 | خطا در بارگذاری تصویر                                                                       |      باگ      |
| PSDJAVA-523 | خطا در بارگذاری تصویر: قادر به تبدیل آبجکت از نوع UnknownStructure به نوع DescriptorStructure   |      باگ      |
| PSDJAVA-524 | تغییر در فایل در کتابخانه شخص سوم، فایل PSD را خراب می کند اما قابل باز کردن در فتوشاپ می باشد |      باگ      |

## **تغییرات در API عمومی**
# **API‌های اضافه شده:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **API‌های حذف شده:**

- هیچکدام

## **مثال‌های استفاده:**

**PSDJAVA-518. افزودن نوع جدید از انحنا (پرچم)**

{{< highlight java >}}
    String sourceFile = "src/main/resources/flag_warp.psd";
    String outputFile = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. افزودن انواع جدیدی از انحنا: قوس بالا، قوس پایین، کره**

{{< highlight java >}}
    String sourceFileArcUpper = "src/main/resources/arc_upper_warp.psd";
    String sourceFileArcLower = "src/main/resources/arc_lower_warp.psd";
    String sourceFileBulge = "src/main/resources/bulge_warp.psd";

    String outputFileArcUpper = "src/main/resources/ArcUpper_export.png";
    String outputFileArcLower = "src/main/resources/ArcLower_export.png";
    String outputFileBulge = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcUpper, psdLoadOptions)) {
        psdImage.save(outputFileArcUpper, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcLower, psdLoadOptions)) {
        psdImage.save(outputFileArcLower, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileBulge, psdLoadOptions)) {
        psdImage.save(outputFileBulge, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. پیاده سازی متد جدید PsdImage.AddPosterizeAdjustmentLayer برای اضافه کردن لایه جدید پوسترایز**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya.psd";
    String outFile = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // بررسی تغییرات ذخیره شده
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "اشکال در تطابق اشیاء.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-521. اطلاعات PSD در حالت فقط باز کردن و ذخیره کردن از دست رفته است**

{{< highlight java >}}
    String src = "src/main/resources/Original file.psd";
    String outputPsd = "src/main/resources/out_Original file.psd";
    String outputPng = "src/main/resources/out_Original file.png";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. خطا در بارگذاری تصویر**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. خطا در بارگذاری تصویر: قادر به تبدیل آبجکت از نوع UnknownStructure به نوع DescriptorStructure**

{{< highlight java >}}
   try (PsdImage newPsd = new PsdImage(10, 10)) {
        newPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            newPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // باید به درستی بارگذاری شود
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. تغییر در فایل در کتابخانه شخص سوم، فایل PSD را خراب می کند اما قابل باز کردن در فتوشاپ می باشد**

{{< highlight java >}}
    String sourceFile = "src/main/resources/output.psd";
    String outputFile = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(outputFile, pngOptions);
    }
{{< /highlight >}}

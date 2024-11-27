---
title: Aspose.PSD برای جاوا 24.7 - یادداشت های انتشار
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} این صفحه حاوی یادداشت های انتشار برای [Aspose.PSD برای جاوا 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) می‌باشد. {{% /alert %}}

| **کلید**        | **خلاصه**                                                                                      | **دسته بندی** |
|:---------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635   | "استثناء بارگذاری تصویر" زمان باز کردن سند AI                                           | اشکال        |
| PSDJAVA-636   | متن به طرز نادرستی در فایل‌های PDF خروجی نمایش داده می‌شود                               | اشکال        |
| PSDJAVA-637   | رفع استثناء ImageSaveException: خطای صادر کردن تصویر برای فایل داده شده در لینوکس    | اشکال        |
| PSDJAVA-638   | رفع مشکلات بارگذاری فونت هنگام استفاده از Aspose.Drawing                               | اشکال        |
| PSDJAVA-639   | 'عملیات حسابی منجر به سرریز شدن' هنگام ایجاد لایه smart object با استفاده از JPEG بزرگ | اشکال        |
| PSDJAVA-640   | فایل AI نمی‌تواند به یک فایل JPG تبدیل شود                                               | اشکال        |

## **تغییرات API عمومی**
# **API های اضافه شده:**

- هیچکدام

# **API های حذف شده:**

- هیچکدام

## **مثال های استفاده:**

**PSDJAVA-635. "استثناء بارگذاری تصویر" زمان باز کردن سند AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. متن به طرز نادرستی در فایل‌های PDF خروجی نمایش داده می‌شود**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. رفع استثناء ImageSave: خطای صادر کردن تصویر برای فایل داده شده در لینوکس**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. رفع مشکل بارگذاری فونت‌ها هنگام استفاده از Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- قبل از به‌روزرسانی. تعداد فونت‌های نصب شده: " + installedFonts.getFamilies().length);
        System.out.println("- پلتفورم: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- به‌روزرسانی کش فونت با تلاش برای گرفتن نام فونت Adobe برای 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- پس از به‌روزرسانی. تعداد فونت‌های نصب شده: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'عملیات حسابی منجر به سرریز شدن' هنگام ایجاد لایه smart object با استفاده از JPEG بزرگ**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. فایل AI نمی‌تواند به یک فایل JPG تبدیل شود**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

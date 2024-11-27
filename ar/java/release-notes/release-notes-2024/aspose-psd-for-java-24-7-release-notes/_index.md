---
title: أزبزس.بي.إس.دي لجافا 24.7 - ملاحظات الإصدار
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أزبزس.بي.إس.دي لجافا 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **المفتاح**     | **الملخص**                                                                                      | **الفئة**   |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | استثناء "فشل تحميل الصورة" عند فتح مستند AI                                                  | خلل          |
| PSDJAVA-636 | تقديم النص بشكل غير صحيح في ملفات PDF الناتجة                                                 | خلل          |
| PSDJAVA-637 | إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux             | خلل          |
| PSDJAVA-638 | إصلاح تحميل الخطوط عند استخدام Aspose.Drawing                                                 | خلل          |
| PSDJAVA-639 | 'العملية الحسابية أسفرت عن تجاوز' عند إنشاء طبقة كائن ذكي باستخدام ملف JPEG كبير        | خلل          |
| PSDJAVA-640 | لا يمكن تحويل ملف AI إلى ملف JPG                                                              | خلل          |

## **تغييرات الواجهة العامة للتطبيقات**
# **APIs المضافة:**

- لا شيء

# **APIs المحذوفة:**

- لا شيء

## **أمثلة الاستخدام:**

**PSDJAVA-635. "فشل تحميل الصورة" استثناء عند فتح مستند AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. تقديم النص بشكل غير صحيح في ملفات PDF الناتجة**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux**

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

**PSDJAVA-638. إصلاح تحميل الخطوط عند استخدام Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- قبل التحديث. عدد الخطوط المثبتة: " + installedFonts.getFamilies().length);
        System.out.println("- النظام الأساسي: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- تحديث ذاكرة التخزين المؤقت للخطوط عبر محاولة الحصول على اسم الخط من Adobe لـ 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- بعد التحديث. عدد الخطوط المثبتة: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'العملية الحسابية أسفرت عن تجاوز' عند إنشاء طبقة كائن ذكي باستخدام ملف JPEG كبير**

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

**PSDJAVA-640. لا يمكن تحويل ملف AI إلى ملف JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
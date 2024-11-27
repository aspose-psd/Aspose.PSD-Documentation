---
title: Aspose.PSD עבור Java 24.7 - הערות גרסה
type: docs
weight: 40
url: /he/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל הערות גרסה עבור [Aspose.PSD עבור Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **מפתח**   | **סיכום**                                                                                            | **קטגוריה** |
|:------------|:-----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך AI                                                  | באג          |
| PSDJAVA-636 | הטקסט מוצג באופן שגוי בקבצי PDF המוצאים                                                      | באג          |
| PSDJAVA-637 | תיקון ImageSaveException: ייצוא התמונה נכשל עבור הקובץ הנתון בלינוקס                        | באג          |
| PSDJAVA-638 | תיקון טעינת גופנים בעת שימוש ב-Aspose.Drawing                                                 | באג          |
| PSDJAVA-639 | 'הפעולה החשבונית תוצאה בתוחלת' ביצירת שכבת אובייקט חכם בשימוש ב-JPEG גדול               | באג          |
| PSDJAVA-640 | לא ניתן להמיר את הקובץ AI לקובץ JPG                                                         | באג          |

## **שינויים ב- API הציבוריים**
# **APIs שנוספו:**

- אין

# **APIs שהוסרו:**

- אין

## **דוגמאות שימוש:**

**PSDJAVA-635. חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. הטקסט מוצג באופן שגוי בקבצי PDF המוצאים**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. תיקון ImageSaveException: ייצוא התמונה נכשל עבור הקובץ הנתון בלינוקס**

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

**PSDJAVA-638. תיקון טעינת גופנים בעת שימוש ב-Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- לפני העדכון. ספירת הפונטים המותקנים: " + installedFonts.getFamilies().length);
        System.out.println("- פלטפורמה: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- רענון מטמון הפונטים על ידי ניסיון לקבל את שם הפונט של אדובי עבור 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- לאחר העדכון. ספירת הפונטים המותקנים: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'הפעולה החשבונית תוצאה בתוחלת' ביצירת שכבת אובייקט חכם בשימוש ב-JPEG גדול**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("שכבת בדיקה");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. לא ניתן להמיר את הקובץ AI לקובץ JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

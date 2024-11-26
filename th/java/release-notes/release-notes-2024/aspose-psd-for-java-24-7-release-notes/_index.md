---
title: Aspose.PSD for Java 24.7 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Key**     | **สรุป**                                                                                      | **ประเภท** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | ข้อผิดพลาด "Image loading failed." เมื่อเปิดเอกสาร AI                                            | ข้อผิดพลาด          |
| PSDJAVA-636 | การแสดงข้อความไม่ถูกต้องในไฟล์ PDF ผลลัพธ์                                            | ข้อผิดพลาด          |
| PSDJAVA-637 | แก้ปัญหา ImageSaveException: การส่งออกภาพล้มเหลวสำหรับไฟล์ที่กำหนดบน Linux                          | ข้อผิดพลาด          |
| PSDJAVA-638 | แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.วาด                                                      | ข้อผิดพลาด          |
| PSDJAVA-639 | 'การดำเนินการทางคณิตศาสตร์ส่งผลให้เกิน' เมื่อสร้างเลเยอร์วัตถุอัจฉริยะโดยใช้ JPEG ขนาดใหญ่ | ข้อผิดพลาด          |
| PSDJAVA-640 | ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้                                                 | ข้อผิดพลาด          |

## **การเปลี่ยนแปลงใน Public API**
# **API ที่เพิ่มเติม:**

- ไม่มี

# **API ที่ถูกลบ:**

- ไม่มี 

## **ตัวอย่างการใช้:**

**PSDJAVA-635. ข้อผิดพลาด "Image loading failed." เมื่อเปิดเอกสาร AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. การแสดงข้อความไม่ถูกต้องในไฟล์ PDF ผลลัพธ์**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. แก้ปัญหา ImageSaveException: การส่งออกภาพล้มเหลวสำหรับไฟล์ที่กำหนดบน Linux**

{{< highlight java >}}}

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

**PSDJAVA-638. แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.วาด**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- ก่อนการอัปเดต. จำนวนฟอนต์ที่ติดตั้ง: " + installedFonts.getFamilies().length);
        System.out.println("- แพลตฟอร์ม: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- รีเฟรชแคชฟอนต์โดยการพยายามให้ชื่อฟอนต์ Adobe สำหรับ 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- หลังการอัปเดต. จำนวนฟอนต์ที่ติดตั้ง: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'การดำเนินการทางคณิตศาสตร์ส่งผลให้เกิน' เมื่อสร้างเลเยอร์วัตถุอัจฉริยะโดยใช้ JPEG ขนาดใหญ่**

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

**PSDJAVA-640. ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

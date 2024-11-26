---
title: Aspose.PSD สำหรับ Java 23.8 - บันทึกการปล่อย
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-23-8-release-notes/
---

{{% alert color="primary" %}} หน้านี้ประกอบด้วยบันทึกการปล่อยสำหรับ [Aspose.PSD สำหรับ Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **คีย์**    | **สรุป**                                                                                                                                          | **หมวดหมู่** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-518 | เพิ่มประเภทใหม่ของการผิดรูป (Flag)                                                                                                           |    คุณลักษณะ    |
| PSDJAVA-519 | เพิ่มประเภทใหม่ของการผิดรูป: โค้งขึ้น, โค้งลง, ทรงกลม                                                                                  |    คุณลักษณะ    |
| PSDJAVA-520 | ดำเนินการเพิ่มเมธอดใหม่ PsdImage.AddPosterizeAdjustmentLayer เพื่อเพิ่มเลเยอร์ Posterize ใหม่                                         |    คุณลักษณะ    |
| PSDJAVA-521 | ข้อมูล PSD สูญเสียเมื่อเปิดและบันทึกเท่านั้น                                                                                               |      ข้อบกพร่อง     |
| PSDJAVA-522 | การโหลดภาพล้มเหลว                                                                                                                            |      ข้อบกพร่อง     |
| PSDJAVA-523 | การโหลดภาพล้มเหลว: ไม่สามารถแปลงออบเจกต์ชนิด UnknownStructure เป็นออบเจกต์ชนิด DescriptorStructure                    |      ข้อบกพร่อง     |
| PSDJAVA-524 | ไฟล์ถูกเปลี่ยนแปลงในไลบรารีภายนอกทำให้ไฟล์ PSD เสียหาย แต่ยังสามารถเปิดใน Photoshop ได้                                      |      ข้อบกพร่อง     |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **API ที่ถูกลบออก:**

- ไม่มี

## **ตัวอย่างการใช้:**

**PSDJAVA-518. เพิ่มประเภทใหม่ของการผิดรูป (Flag)**

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

**PSDJAVA-519. เพิ่มประเภทใหม่ของการผิดรูป: โค้งขึ้น, โค้งลง, ทรงกลม**

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

**PSDJAVA-520. ดำเนินการเพิ่มเมธอดใหม่ PsdImage.AddPosterizeAdjustmentLayer เพื่อเพิ่มเลเยอร์ Posterize ใหม่**

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

    // Check saved changes
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objects are not equal.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-521. ข้อมูล PSD สูญเสียเมื่อเปิดและบันทึกเท่านั้น**

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

**PSDJAVA-522. การโหลดภาพล้มเหลว**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. การโหลดภาพล้มเหลว: ไม่สามารถแปลงออบเจกต์ชนิด UnknownStructure เป็นออบเจกต์ชนิด DescriptorStructure**

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
                // ควรโหลดถูกต้อง
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. ไฟล์ถูกเปลี่ยนแปลงในไลบรารีภายนอกทำให้ไฟล์ PSD เสียหาย แต่ยังสามารถเปิดใน Photoshop ได้**

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

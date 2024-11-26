---
title: Aspose.PSD สำหรับ Java 23.9 - บันทึกการออกจำหน่าย
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการออกจำหน่ายสำหรับ [Aspose.PSD สำหรับ Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **หมายเลข** | **สรุป**                                                                                                                                      | **หมวดหมู่** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | การนำมาใช้งานการสร้างมาสก์สำหรับเลเยอร์ปรับปรุงใหม่                                                                                             |    คุณลักษณะ   |
| PSDJAVA-528 | เพิ่มการสนับสนุนการผสมเลเยอร์ดึกดาบแบบกลุ่มเป็นตัวเลือกการผสม                                                                                     |    คุณลักษณะ   |
| PSDJAVA-529 | ไฟล์ PSD ที่มีโหมดสี 16 บิตไม่ใช้มาสก์สำหรับเลเยอร์ปรับปรุง                                                                              |      ข้อบกพร่อง     |
| PSDJAVA-530 | การแสดงผลไม่ถูกต้องของเครื่องหมายวงเล็บในเลเยอร์ข้อความ                                                                                                 |      ข้อบกพร่อง     |
| PSDJAVA-531 | ไม่สามารถอัปเดตสไตล์ในเลเยอร์ข้อความ                                                                                                          |      ข้อบกพร่อง     |
| PSDJAVA-532 | หลังจากส่งออกไฟล์ PSD ด้วย CMYK สีพังสีในไฟล์ PSD ที่ส่งออก                                                                          |      ข้อบกพร่อง     |
| PSDJAVA-533 | ไฟล์ PSB ที่เฉพาะเจาะจงโยงออกข้อยกเว้น "ของสี่เหลี่ยมไม่มีพื้นที่ประมวลผลร่วม"                                                                 |      ข้อบกพร่อง     |
| PSDJAVA-534 | การโหลดภาพล้มเหลว OverflowException: ปฏิบัติการคำนวณที่เกิดความผิดพลาด                                                            |      ข้อบกพร่อง     |

## **การเปลี่ยนแปลงใน Public API**
# **API ที่เพิ่มเข้ามา:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **API ที่ถูกนำออก:**

- ไม่มี

## **ตัวอย่างการใช้งาน:**

** PSDJAVA-527. การนำมาใช้งานการสร้างมาส์สำหรับเลเยอร์ปรับปรุงใหม่**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "ไม่เท่ากัน.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. เพิ่มการสนับสนุนการผสมเลเยอร์ดึกดาบแบบกลุ่มเป็นตัวเลือกการผสม**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

ต่อไปมี...

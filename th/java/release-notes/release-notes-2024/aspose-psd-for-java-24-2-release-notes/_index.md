---
title: Aspose.PSD for Java 24.2 - บันทึกการปล่อย
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-24-2-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการปล่อยสำหรับ [Aspose.PSD for Java 24.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.2/) {{% /alert %}}

| **คีย์**    | **สรุป**                                                                                  | **หมวดหมู่** |
|:------------|:---------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-584 | จัดการคุณสมบัติมุมสำหรับ PatternFillSettings                                        | คุณลักษณะ     |
| PSDJAVA-585 | รองรับการยืดและย่อแบนานแนวตั้งและนอนสำหรับ TextLayer                                | คุณลักษณะ    |
| PSDJAVA-589 | [รูปแบบ AI] นำการแสดงผลพื้นหลังที่ถูกต้องในรูปแบบ AI ที่ใช้ PDF เข้าไป                | คุณลักษณะ    |
| PSDJAVA-590 | เปลี่ยนกลไกทำลายในการบิด                                                   | การปรับปรุง    |
| PSDJAVA-591 | เพิ่มความรวดเร็วในการบิด                                                        | การปรับปรุง    |
| PSDJAVA-592 | ข้อแก้ไข "การโหลดรูปภาพล้มเหลว" เมื่อเปิดเอกสาร                               | ข้อบกพร่อง     |
| PSDJAVA-593 | แก้ไขการบันทึกไฟล์ psd ที่มีรูปแบบ Stroke                                          | ข้อบกพร่อง     |
| PSDJAVA-594 | สไตล์ข้อความไม่ถูกต้องในอ็อบเจ็กต์ฉลากเฉดสเพรสเราห์เมื่อเราใช้ ReplaceContents | ข้อบกพร่อง     |
| PSDJAVA-595 | [รูปแบบ AI] แก้ไขการเรนเดอร์ Cubic Bezier ในไฟล์ AI                       | ข้อบกพร่อง    |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- T:com.aspose.psd.fileformats.psd.layers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.update
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.getAngle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.setAngle(double)

# **API ที่ถูกลบ:**

- T:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.update

## **ตัวอย่างการใช้:**

** PSDJAVA-584. จัดการกับคุณสมบัติของมุมสำหรับ PatternFillSettings**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/PatternFillLayerWide_0.psd";
        String outputFile = "src/main/resources/PatternFillLayerWide_0_output.psd";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage image = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();
            fillSettings.setAngle(70.0);
            fillLayer.update();
            image.save(outputFile, new PsdOptions());
        }

        try (PsdImage image = (PsdImage) Image.load(outputFile, psdLoadOptions)) {
            FillLayer fillLayer = (FillLayer) image.getLayers()[1];
            PatternFillSettings fillSettings = (PatternFillSettings) fillLayer.getFillSettings();

            assertAreEqual(70.0, fillSettings.getAngle());
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

... (ต่อไป)
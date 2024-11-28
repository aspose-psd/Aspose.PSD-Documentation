---
title: Aspose.PSD for Java 24.1 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-24-1-release-notes/
---

{{% alert color="primary" %}} หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 24.1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) {{% /alert %}}

| **คีย์**     | **สรุป**                                                                                    | **หมวดหมู่** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับภาพ AI หลายหน้า | คุณลักษณะ      |
| PSDJAVA-579 | ไม่สามารถใช้เอฟเฟคเอฟเฟกต์บนข้อความ                                        | ข้อบกพร่อง          |
| PSDJAVA-580 | การเรนเดอร์ไม่ถูกต้องของมาสก์ในไฟล์ที่ระบุ                                        | ข้อบกพร่อง          |
| PSDJAVA-581 | NullReferenceException ที่ Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor | ข้อบกพร่อง          |
| PSDJAVA-582 | [รูปแบบ AI] การแก้ไขการใช้หน่วยความจำใน AiExporterUtils | ข้อบกพร่อง          |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- ...

# **API ที่ถูกลบ:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- ...

## **ตัวอย่างการใช้:**

** PSDJAVA-576. [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับภาพ AI หลายหน้า**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        String firstPageOutputPng = "src/main/resources/firstPageOutput.png";
        ...

{{< /highlight >}}

** PSDJAVA-579. ไม่สามารถใช้เอฟเฟคเอฟเฟกต์บนข้อความ**

{{< highlight java >}}

        String sourceFile = "src/main/resources/text_warp.psd";
        ...

{{< /highlight >}}

** PSDJAVA-580. การเรนเดอร์ไม่ถูกต้องของมาส์คในไฟล์ที่ระบุ**

{{< highlight java >}}

        String sourceFile1 = "src/main/resources/mask_problem.psd";
        ...

{{< /highlight >}}

** PSDJAVA-581. NullReferenceException ที่ Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor**

{{< highlight java >}}

        String fontsFolder = "src/main/resources/Fonts";
        ...

{{< /highlight >}}

** PSDJAVA-582. [รูปแบบ AI] การแก้ไขการใช้หน่วยความจำใน AiExporterUtils**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        ...

{{< /highlight >}}
---
title: Aspose.PSD สำหรับ Python via .NET 24.3 - บันทึกรายละเอียดการปล่อย
type: docs
weight: 10
url: /th/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกรายละเอียดการปล่อยสำหรับ [Aspose.PSD สำหรับ Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**      | **สรุป**                                                          | **ประเภท**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [รูปแบบ AI] ลดเวลาโหลดของรูปภาพ AI หน้าหลายหน้าขนาดใหญ่        | การปรับปรุง |
| PSDPYTHON-45 | หลังจากที่ไฟล์ PSD หลังจากที่แปลงจาก 8 บิตเป็น 16 บิต กลายเป็นอ่านไม่ได้ |     ข้อบกพร่อง     |
| PSDPYTHON-46 | หลังจากที่ไฟล์ PSD หลังจากที่แปลงจาก 8 บิตเป็น 32 บิต กลายเป็นอ่านไม่ได้ |     ข้อบกพร่อง     |
| PSDPYTHON-47 | [รูปแบบ AI] แก้ไขการแสดงผลเส้น Curve ที่ไฟล์ AI                  |     ข้อบกพร่อง     |



## **การเปลี่ยนแปลงของ API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- ไม่มี

# **API ที่ถูกลบออก:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDPYTHON-42. [รูปแบบ AI] ลดเวลาโหลดของรูปภาพ AI หน้าหลายหน้าขนาดใหญ่**

{{< highlight python >}}
   # ไม่มีตัวอย่าง
{{< /highlight >}}

**PSDPYTHON-45. หลังจากที่ไฟล์ PSD หลังจากที่แปลงจาก 8 บิตเป็น 16 บิต กลายเป็นอ่านไม่ได้**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # ถูกต้อง
                pass
            else:
                raise Exception("การทราบทรวงเกิดโลก่าง, ทรรงที่ต้องการ ดตรรทราเอลทรูฟ ชูทรีทเฉล จากรี่แล รีซูส อเดลน ละ 16 เรซูรเซสตรัยก")
{{< /highlight >}}

**PSDPYTHON-46. หลังจากที่ไฟล์ PSD หลังจากที่แปลงจาก 8 บิตเป็น 32 บิต กลายเป็นอ่านไม่ได้**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # ถูกต้อง
                pass
            else:
                raise Exception("การทราบทรุคลเอลดวองกล รีซูสเซ เอลวทร้อง รีทรรีมทรางกล, ทรรง ท็อตรู ยว๊ก อนจุ้ก็เรเชอ ทราเบล จาแเฉล ลรรลเอเฮลนเอน เคลล ธรวส ชุหลเม ตรกร คดยล จรูรเซ)
{{< /highlight >}}

**PSDPYTHON-47. [รูปแบบ AI] แก้ไขการแสดงเส้น Curve ที่ไฟล์ AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

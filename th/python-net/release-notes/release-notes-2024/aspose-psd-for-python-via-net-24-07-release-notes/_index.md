---
title: บันทึกการอัปเดต Aspose.PSD สำหรับ Python via .NET 24.7
type: docs
weight: 10
url: /th/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD สำหรับ Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**      | **รายละเอียด**                                                                                                  | **หมวดหมู่** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | มีข้อผิดพลาด "การโหลดรูปภาพไม่สำเร็จ" เมื่อเปิดเอกสาร AI                             | บั๊ก      |
| PSDPYTHON-87 | ข้อความถูกเรนเดอร์ไม่ถูกต้องในไฟล์ PDF ผลลัพธ์                           | บั๊ก      |
| PSDPYTHON-88 | แก้ไขข้อยกเว้น ImageSaveException: การส่งออกรูปภาพล้มเหลวสำหรับไฟล์ที่กำหนดบน Linux  | บั๊ก      |
| PSDPYTHON-89 | แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.Drawing                                                      | บั๊ก      |
| PSDPYTHON-90 | 'การดำเนินการเลขคณิตเกิดอุดม' เมื่อสร้างเลเยอร์ออบเจกต์สมาร์ทโดยใช้ JPEG ขนาดใหญ่ | บั๊ก      |
| PSDPYTHON-91 | ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้                                                | บั๊ก      |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDPYTHON-86. มีข้อผิดพลาด "การโหลดรูปภาพไม่สำเร็จ" เมื่อเปิดเอกสาร AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. ข้อความถูกเรนเดอร์ไม่ถูกต้องในไฟล์ PDF ผลลัพธ์**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. แก้ไขข้อยกเว้น ImageSaveException: การส่งออกรูปภาพล้มเหลวสำหรับไฟล์ที่กำหนดบน Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- ก่อนการอัปเดต จำนวนฟอนต์ที่ติดตั้ง: " + str(len(installedFonts.families)))
            print("- รีเฟรชแคชฟอนต์โดยพยายามรับชื่อฟอนต์ของ Adobe สำหรับ 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- หลังการอัปเดต จำนวนฟอนต์ที่ติดตั้ง: " + str(len(installedFonts.families))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'การดำเนินการเลขคณิตเกิดอุดม' เมื่อสร้างเลเยอร์ออบเจกต์สมาร์ทโดยใช้ JPEG ขนาดใหญ่**
{{< highlight python >}}
        # แก้ไขแล้ว แต่ยังมีปัญหาเพิ่มเติมใน Aspose.PSD สำหรับ Python ที่จำกัดการทดสอบนี้
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Test Layer"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

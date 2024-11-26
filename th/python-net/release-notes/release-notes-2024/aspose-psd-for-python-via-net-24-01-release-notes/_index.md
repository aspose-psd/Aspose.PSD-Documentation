---
title: บันทึกการออก Aspose.PSD สำหรับ Python ผ่าน . NET 24.1
type: ศูนย์ความรู้
weight: 10
url: /th/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกสำหรับ [Aspose.PSD สำหรับ Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                                | **ประเภท** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับรูปภาพ AI หลายหน้า                                                 |   คุณลักษณะ   |
|  PSDPYTHON-22 | พลิกเอฟเฟกต์ข้อความไม่ได้รับการประยุกต์ใช้กับข้อความ                                                                     |     ข้อบกพร่อง     |
|  PSDPYTHON-23 | การเรนเดอร์ไม่ถูกต้องของมาสก์ในไฟล์ที่เฉพาะเจาะจง                                                                 |     ข้อบกพร่อง     |
|  PSDPYTHON-24 | NullReferenceException ที่ Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor           |     ข้อบกพร่อง     |
|  PSDPYTHON-25 | [รูปแบบ AI] การแก้ไขการใช้งานหน่วยความจำใน AiExporterUtils                                       |     ข้อบกพร่อง     |



## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API ที่ถูกนำออก:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDPYTHON-19. [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับรูปภาพ AI หลายหน้า**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # โหลดรูปภาพ AI
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # โดยค่าเริ่มต้น, ActivePageIndex คือ 0
            # ดังนั้นหากคุณบันทึกรูปภาพ AI โดยไม่เปลี่ยนแปลงสมบัตินี้, รูปภาพหน้าแรกจะถูกเรนเดอร์และบันทึก
            image.save(firstPageOutputPng, PngOptions())

            # เปลี่ยน ActivePageIndex เป็นหน้าที่สอง
            image.active_page_index = 1

            # บันทึกหน้าที่สองของรูปภาพ AI เป็นรูปภาพ PNG
            image.save(secondPageOutputPng, PngOptions())

            # เปลี่ยน ActivePageIndex เป็นหน้าที่สาม
            image.active_page_index = 2

            # บันทึกหน้าที่สามของรูปภาพ AI เป็นรูปภาพ PNG
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. พลิกเอฟเฟกต์ข้อความไม่ได้รับการประยุกต์ใช้กับข้อความ**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. การเรนเดอร์ไม่ถูกต้องของมาสก์ในไฟล์ที่เฉพาะเจาะจง**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException ที่ Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [รูปแบบ AI] การแก้ไขการใช้งานหน่วยความจำใน AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # หน่วยความจำ C# ใช้งานอยู่ที่ 220, แต่สำหรับ python เราไม่มีการเข้าถึงกิจกรรม GC โดยตรง
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # โหลดรูปภาพ AI
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # บันทึกรูปภาพ AI หน้าแรกเป็นรูปภาพ PNG
            image.save(firstPageOutputPng, pngOpt)

            # เปลี่ยน ActivePageIndex เป็นหน้าที่สอง
            image.active_page_index = 1

            # บันทึกหน้าที่สองของรูปภาพ AI เป็นรูปภาพ PNG
            image.save(secondPageOutputPng, pngOpt)

            # เปลี่ยน ActivePageIndex เป็นหน้าที่สาม
            image.active_page_index = 2

            # บันทึกหน้าที่สามของรูปภาพ AI เป็นรูปภาพ PNG
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("การใช้งานหน่วยความจำมีขนาดใหญ่เกินไป. {} แทนที่ {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

---
title: บันทึกการเปลี่ยนแปลง Aspose.PSD for .NET 24.1
type: งานเอกสาร
weight: 120
url: /th/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการปล่อยวางสำหรับ [Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **คีย์**     | **สรุป**                                                                                       | **หมวดหมู่** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับรูปภาพ AI หลายหน้า                                            |   คุณลักษณะ   |
| PSDNET-718  | เอฟเฟค Warp Text Effect ไม่ได้ใช้กับข้อความ                                                            |     ปัญหา     |
| PSDNET-1620 | การเรนเดอร์ไม่ถูกต้องของมาสก์ในไฟล์ที่เฉพาะเจาะจง                                             |     ปัญหา     |
| PSDNET-1855 | NullReferenceException ที่ Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor    |     ปัญหา     |
| PSDNET-1883 | [รูปแบบ AI] การแก้ไขการใช้งานหน่วยความจำใน AiExporterUtils                                            |     ปัญหา     |



## **การเปลี่ยนแปลงของ API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API ที่ถูกนำออก:**
- None


## **ตัวอย่างการใช้:**

**PSDNET-718. เอฟเฟค Warp Text Effect ไม่ได้ใช้กับข้อความ**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. การเรนเดอร์ไม่ถูกต้องของมาสก์ในไฟล์ที่เฉพาะเจาะจง**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [รูปแบบ AI] เพิ่มการจัดการพื้นฐานสำหรับรูปภาพ AI หลายหน้า**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// โหลดรูปภาพ AI
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // เริ่มต้นที่หน้านี้คือ 0
    // ดังนั้นหากคุณบันทึกรูป AI โดยไม่เปลี่ยนแปลงคุณสมบัตินี้ จะถูกแสดงและบันทึกหน้าแรก
    image.Save(firstPageOutputPng, new PngOptions());

    // เปลี่ยนดัชพีเพจที่กำลังใช้เป็นหน้าที่สอง
    image.ActivePageIndex = 1;

    // บันทึกรูป AI หน้าที่สองเป็นรูป PNG
    image.Save(secondPageOutputPng, new PngOptions());

    // เปลี่ยนดัชพีเพจที่กำลังใช้เป็นหน้าที่สาม
    image.ActivePageIndex = 2;

    // บันทึกหน้าที่สามของรูป AI เป็นรูป PNG
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException at Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [รูปแบบ AI] การแก้ไขการใช้งานหน่วยความจำใน AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// โหลดรูปภาพ AI
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // บันทึกรูป AI หน้าแรกเป็นรูป PNG
    image.Save(firstPageOutputPng, new PngOptions());

    // เปลี่ยนดัชพีเพจที่กำลังใช้เป็นหน้าที่สอง
    image.ActivePageIndex = 1;

    // บันทึกรูป AI หน้าสองเป็นรูป PNG
    image.Save(secondPageOutputPng, new PngOptions());

    // เปลี่ยนดัชพีเพจที่กำลังใช้เป็นหน้าที่สาม
    image.ActivePageIndex = 2;

    // บันทึกหน้าที่สามของรูป AI เป็นรูป PNG
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("ใช้หน่วยความจำมากเกินไป " + memoryUsed + " แทนที่จะเป็น " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}

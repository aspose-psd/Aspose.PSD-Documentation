---
title: Aspose.PSD for .NET 24.7 - บันทึกการออก​เวอร์ชัน
type: docs
weight: 60
url: /th/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการออกเวอร์ชันสำหรับ [Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                                        | **หมวดหมู่** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | ข้อยกเว้น "การโหลดรูปภาพล้มเหลว" เมื่อเปิดเอกสาร AI                                       | ข้อบกพร่อง      |
| PSDNET-2022 | ข้อจำกัดการแสดงข้อความไม่ถูกต้องในไฟล์ PDF ผลลัพธ์                                     | ข้อบกพร่อง      |
| PSDNET-2061 | แก้ไข ImageSaveException: การส่งออกภาพล้มเหลวสำหรับไฟล์ที่ให้ใน Linux                      | ข้อบกพร่อง      |
| PSDNET-2080 | แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.Drawing                                              | ข้อบกพร่อง      |
| PSDNET-2085 | 'การดำเนินการคณิตศาสตร์นำไปสู่การไหลเวียน' เมื่อสร้างเลเยอร์วัตถุสมาร์ทโดยใช้ JPEG ขนาดใหญ่ | ข้อบกพร่อง      |
| PSDNET-2100 | ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้                                                    | ข้อบกพร่อง      |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- ไม่มี

# **API ที่ถูกนำออก:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-1029. ข้อยกเว้น "การโหลดรูปภาพล้มเหลว" เมื่อเปิดเอกสาร AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. ข้อจำกัดการแสดงข้อความไม่ถูกต้องในไฟล์ PDF ผลลัพธ์**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. แก้ไข ImageSaveException: การส่งออกภาพล้มเหลวสำหรับไฟล์ที่ให้ใน Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. แก้ไขการโหลดฟอนต์เมื่อใช้ Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- ก่อนการอัพเดต. จำนวนฟอนต์ที่ติดตั้ง: " + installedFonts.Families.Length);
    Console.WriteLine("- แพลตฟอร์ม: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- รีเฟรชแคชฟอนต์โดยการพยายามขอชื่อฟอนต์ Adobe สำหรับ 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- หลังการอัพเดต. จำนวนฟอนต์ที่ติดตั้ง: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'การดำเนินการคณิตศาสตร์นำไปสู่การไหลเวียน' เมื่อสร้างเลเยอร์วัตถุสมาร์ทโดยใช้ JPEG ขนาดใหญ่**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. ไฟล์ AI ไม่สามารถแปลงเป็นไฟล์ JPG ได้**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

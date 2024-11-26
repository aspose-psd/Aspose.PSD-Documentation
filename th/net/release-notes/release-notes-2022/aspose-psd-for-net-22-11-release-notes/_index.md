---
title: Aspose.PSD for .NET 22.11 - บันทึกการอัปเดต
type: docs
weight: 20
url: /th/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- ในการอัปเดตนี้มีปัญหาด้านการดึงข้อมูลกลับเวอร์ชันกับการส่งออกด้วย 16-bit ดังนั้นเราขอแนะนำให้ระมัดระวังเมื่อใช้คุณลักษณะนี้ในการใช้งานในเวอร์ชันนี้
กรุณาอย่าอัปเดต Aspose.PSD เป็นเวอร์ชัน 22.9-22.11 ถ้าการประมวลผลภาพ 16-bit เป็นความสาคัญของคุณ

เรากำลังทำงานกำลังค้นหาวิธีการแก้ปัญหาเหล่านี้

{{% /alert %}}

|**Key**|**บทสรุป**|**ประเภท**|
| :- | :- | :- |
|PSDNET-1320|ไม่สามารถส่งออกไฟล์ PSB ขนาดใหญ่อย่าง極|การพัฒนาเพิ่มเติม|
|PSDNET-659|ทำให้จุดศูนย์ของไฟล์สีไร้เส้นทรงเครื่องใช้เคลื่อนย้างได้|คุณลักษณะ|
|PSDNET-1330|วิธีบีบอัด ZipWithoutPrediction ที่ไม่รองรับสำหรับไฟล์ที่แน่นอน|คุณลักษณะ|
|PSDNET-735|หลังจากใช้เมธอดการแปลงสำหรับเลเยอ์อย่างเดียว ลเยอร์ที่บันทึกมีกล่องของข้อมูลไม่ถูกต้อง|ข้อบกพร่อง|
|PSDNET-1234|ข้อยกเวกในการโหลดรูปภาพ PSD ที่มีลวดลาย|ข้อบกพร่อง|
|PSDNET-1244|การส่งออกรูปภาพล้มเหลว (IndexOutOfRangeException) ในการบันทึกไฟล์ PSD พร้อมสัญลักษณ์จีน|ข้อบกพร่อง|
|PSDNET-1303|TimeLine ActiveFrame ทำให้ผลลัพธ์ผิด|ข้อบกพร่อง|
|PSDNET-1307|Regression 22.7: การแสดงผลตัวอักษรภาษาอาระบิกไม่ถูกต้อง|ข้อบกพร่อง|
|PSDNET-1321|Vector Mask บนชั้นกลุ่มทำงานผิดพลาด ภาพสุดท้ายมีรูดำหมดอยู่แต่ไม่ควรจะ|ข้อบกพร่อง|


## **การเปลี่ยนแปลงสำหรับ API สาธารณะ**
# **API ที่เพิ่มเติม:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **API ที่นำออก:**
- ไม่มี


## **ตัวอย่างการใช้งาน:**

**PSDNET-659. ทำให้จุดศูนย์ของไฟล์สีไร้เส้นทรงเครื่องใช้เคลื่อนย้างได้**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // อัปเดตจุด offset
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. หลังจากใช้เมธอดการแปลงสำหรับเลเยอร์อย่างเดียว ลเยอร์ที่บันทึกมีกล่องของข้อมูลไม่ถูกต้อง**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // ตั้งขนาดข้อความใหม่
    const int NewWidth = 250;
    const int NewHeight = 250;

    // กำหนดกลไกใหม่สำหรับการเปลี่ยนขนาดสำหรับเลเยอร์ข้อความที่ใช้ที่นี่
    // ไม่เพียงแต่เลเยอร์แต่ยังมีการเปลี่ยนฐานข้อมูลการแปลงเลเยอร์ข้อความด้วย
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // เหตุผลของมุมลดลงคือเบต้าฟอนต์เริ่มต้น
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // ทุกอย่างถูกต้อง
    }
    else
    {
        throw new Exception("ตำแหน่งไม่ถูกต้อง");
    }
}
{{< /highlight >}}


**PSDNET-1234. ข้อยกเวกในการโหลดรูปภาพ PSD ที่มีลวดลาย**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}


**PSDNET-1244. การส่งออกรูปภาพล้มเหลว (IndexOutOfRangeException) ในการบันทึกไฟล์ PSD พร้อมสัญลักษณ์จีน**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // ตรงนี้ควรจะไม่มีข้อยกเวก
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}


**PSDNET-1303. TimeLine ActiveFrame ทำให้ผลลัพธ์ผิด**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}


**PSDNET-1307. Regression 22.7: การแสดงผลตัวอักษรภาษาอาระบิกผิด**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}


**PSDNET-1320. ไม่สามารถส่งออกไฟล์ PSB ขนาดใหญ่อย่าง極**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}


**PSDNET-1321. Vector Mask บนชั้นกลุ่มทำงานผิดพลาด ภาพสุดท้ายมีรูดำหมดอยู่แต่ไม่ควรจะ**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}


**PSDNET-1330. วิธีบีบอัด ZipWithoutPrediction ที่ไม่รองรับสำหรับไฟล์ที่แน่นอน**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}

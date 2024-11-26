---
title: บันทึกการอัปเดต Aspose.PSD for .NET 22.12
type: คู่มือ
weight: 10
url: /th/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- ในการอัปเดตนี้ได้แก้ไขปัญหา regression ที่เกิดขึ้นกับการส่งออก 16-bit

{{% /alert %}}

|**Key**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDNET-1336|เพิ่มคุณสมบัติ TextOrientation ที่สามารถแก้ไขได้ในอินเทอร์เฟซเท็กซ์|คุณลักษณะ|
|PSDNET-725|การปรับขนาดของไฟล์ PSD ที่ระบุพร้อมกับเลเยอร์มาสก่อนหน้าผลิตแมสที่ไม่ถูกต้อง|ข้อบกพร่อง|
|PSDNET-1277|เพิ่มความสามารถในการบันทึกและโหลดมาสสำหรับภาพ 16 ภาพ|ข้อบกพร่อง|
|PSDNET-1281|ความโปร่งใสที่ไม่ถูกต้องในการบันทึกภาพ 16 บิตเป็นภาพ 16 หรือ 8 บิต|ข้อบกพร่อง|
|PSDNET-1375|แก้ไข CMYK ในสี 16 บิต|ข้อบกพร่อง|


## **การเปลี่ยนแปลง Public API**
# **API ที่เพิ่มเข้ามา:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **API ที่ถูกนำออก:**
- ไม่มี


## **ตัวอย่างการใช้:**

**PSDNET-725. การปรับขนาดของไฟล์ PSD ที่ระบุพร้อมกับเลเยอร์มาสก่อนหน้าผลิตแมสที่ไม่ถูกต้อง**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// ทำการเปิดไฟล์ PSD ต้นฉบับ
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // ทำการปรับขนาด
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// ทำการเปิดไฟล์ PSD หลังการปรับขนาด
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // ทำการแปลงเป็น PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. เพิ่มความสามารถในการบันทึกและโหลดมาสสำหรับภาพ 16 ภาพ**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // ตัวเลือกที่อนุญาตให้บันทึกสี 16 บิต
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // ไฟล์ PSD จะถูกบันทึกพร้อมกับความโปร่งใส
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. ความโปร่งใสที่ไม่ถูกต้องในการบันทึกภาพ 16 บิตเป็นภาพ 16 หรือ 8 บิต**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// ไฟล์ PSD 16 บิตสี (พร้อมกับความโปร่งใส) จะถูกเปิดและบันทึกเป็นสี 16 บิต
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// ไฟล์ PSD 16 บิตที่บันทึกไว้จะถูกสร้างเป็นไฟล์ png พร้อมกับความโปร่งใส
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. เพิ่มคุณสมบัติ TextOrientation ที่สามารถแก้ไขได้ในอินเทอร์เฟซเท็กซ์**

{{< highlight csharp >}}
// โค้ดต่อไปนี้สาธิตความสามารถในการแก้ไขคุณสมบัติ TextOrientation ใหม่
// สิ่งนี้ไม่ได้มีผลต่อการแสดงผลในขณะนี้ แต่เพียงแต่ช่วยให้คุณแก้ไขค่าคุณสมบัติเท่านั้น

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // การอ่านที่ถูกต้อง
    }
    else
    {
        throw new Exception("การอ่านค่าคุณสมบัติ TextOrientation ไม่ถูกต้อง");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // การอ่านที่ถูกต้อง
    }
    else
    {
        throw new Exception("การอ่านค่าคุณสมบัติ TextOrientation ไม่ถูกต้อง");
    }
}
{{< /highlight >}}

**PSDNET-1375. แก้ไข CMYK ในสี 16 บิต**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// ตั้งค่าตัวเลือกการแปลง
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// ทำการแปลงและบันทึก
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// เปิดไฟล์ที่แปลงแล้วและเรนเดอร์เป็น PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

---
title: บันทึกรายละเอียดเวอร์ชัน Aspose.PSD สำหรับ .NET 24.6
type: สารบัญ
weight: 70
url: /th/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

หน้านี้จะบันทึกรายละเอียดการอัปเดตสำหรับ [Aspose.PSD สำหรับ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **รายละเอียด**                                                                         | **ประเภท** |
|:------------|:-----------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | สนับสนุนเลเยอร์แผนที่ความชัน                                                                              | คุณลักษณะ      |
| PSDNET-1670 | [รูปแบบ AI] เพิ่มการสนับสนุน XPacket Metadata ในรูปแบบ AI                                                                               | คุณลักษณะ      |
| PSDNET-1831 | สนับสนุนประเภทการห่อ Inflate, Squeeze, และ Twist                                                                               | คุณลักษณะ      |
| PSDNET-1653 | โหมด Rgb และ Lab ไม่สามารถมีช่องเชื่อมต่ำกว่า 3 และมากกว่า 4 ช่องในไฟล์ที่มีเลเยอร์ ArtBoard                                                                               | บั๊ก      |
| PSDNET-1775 | พื้นที่ประมวลผลบนขอบบนต้องเป็นบวก (พารามิเตอร์ 'areaToProcess') ในการประมวลผลของไฟล์ที่เฉพาะเจาะจง                                                                               | บั๊ก      |
| PSDNET-2052 | การขยายรูปภาพข้ามแผนภาพหลังจากการบันทึก ข้อมูลสูญพันธุ์ แต่ตัวอย่างกล้องดูถูกต้อง                                                                               | บั๊ก      |

## **การเปลี่ยนแปลงใน API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-1450. สนับสนุนเลเยอร์แผนที่ความชัน**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // เพิ่มเลเยอร์การปรับแต่งแผนที่ความชัน
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// ตรวจสอบการบันทึกการเปลี่ยนแปลง
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "อ็อบเจ็กต์ไม่เท่ากัน");
    }
}
{{< /highlight >}}

**PSDNET-1670. [รูปแบบ AI] เพิ่มการสนับสนุน XPacket Metadata ในรูปแบบ AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("อ็อบเจ็คต์ไม่เท่ากัน");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("อ็อบเจ็กต์เทสเท่ากับ null");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // ข้อมูล Xmp Metadata ถูกเพิ่มเข้ามา
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // เราสามารถเข้าถึง Xmp Packages ของไฟล์ AI ได้
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // และเราสามารถเข้าถึงเนื้อหาของแพ็คเกจเหล่านี้ได้
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. สนับสนุนประเภทการห่อ Inflate, Squeeze, และ Twist**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. โหมด Rgb และ Lab ไม่สามารถมีช่องเชื่อมต่ำกว่า 3 และมากกว่า 4 ช่องในไฟล์ที่มีเลเยอร์ ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // ที่นี่ควรจะไม่มีข้อยกเว้น
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. พื้นที่ประมวลผลบนขอบบนต้องเป็นบวก (พารามิเตอร์ 'areaToProcess') ในการประมวลผลของไฟล์ที่เฉพาะเจาะจง**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // ต้องไม่มีข้อยกเว้น
}
{{< /highlight >}}

**PSDNET-2052. การขยายรูปภาพข้ามแผนภาพหลังจากการบันทึก ข้อมูลสูญพันธุ์ แต่ตัวอย่างกล้องดูถูกต้อง**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // ไม่ควรมีข้อผิดพลาดที่นี่
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // ไม่ควรมีข้อผิดพลาดที่นี่
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

---
title: Aspose.PSD สำหรับ .NET 24.2 - บันทึกการเปลี่ยนแปลง
type: docs
weight: 110
url: /th/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}
หน้านี้เก็บบันทึกการปล่อยออกของ [Aspose.PSD สำหรับ .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

| **Key**     | **สรุป**                                                                      | **หมวดหมู่**  |
|:------------|:------------------------------------------------------------------------------|:-------------|
| PSDNET-1503 | จัดการคุณสมบัติมุมสำหรับ PatternFillSettings                               |   คุณลักษณะ   |
| PSDNET-1719 | รองรับการย่อและขยายแนวตั้งและแนวนอนสำหรับ TextLayer                    |     คุณลักษณะ     |
| PSDNET-1783 | [รูปแบบ AI] ดำเนินการตามข้อแตกต่างในการแสดงผลพื้นหลังในรูปแบบ AI ที่ขึ้นอยู่กับ PDF   |     คุณลักษณะ     |
| PSDNET-1611 | เปลี่ยนกลไก Distort ใน warp                                             |     การปรับปรุง     |
| PSDNET-1802 | เร่งความเร็ว warp                                                                |     การปรับปรุง     |
| PSDNET-995  | ข้อยกเว้น "การโหลดรูปภาพล้มเหลว" เมื่อเปิดเอกสาร                         |     ข้อบกพร่อง     |
| PSDNET-1491 | แก้ไขการบันทึกไฟล์ psd ที่มีแบบ Stroke Pattern                                   |     ข้อบกพร่อง     |
| PSDNET-1642 | สไตล์ข้อความไม่ถูกต้องในอ็อบเจกต์สมาร์ทเมื่อเราใช้ ReplaceContents    |     ข้อบกพร่อง     |
| PSDNET-1884 | [รูปแบบ AI] แก้ไขการเรนเดอร์ Cubic Bezier ในไฟล์ AI                        |     ข้อบกพร่อง     |

## **การเปลี่ยนแปลงใน Public API**
# **API เพิ่มเติม:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API ที่ถูกลบ:**
- ไม่มี

## **ตัวอย่างการใช้:**

**PSDNET-1503. จัดการคุณสมบัติมุมสำหรับ PatternFillSettings**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. รองรับการย่อและขยายแนวตั้งและแนวนอนสำหรับ TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [รูปแบบ AI] ดำเนินการตามข้อแตกต่างในการแสดงผลพื้นหลังในรูปแบบ AI ที่ขึ้นอยู่กับ PDF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. ข้อยกเว้น "การโหลดรูปภาพล้มเหลว" เมื่อเปิดเอกสาร**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "PRODUCT.ai");
string outputFile1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(sourceFile1))
{
    image.Save(outputFile1, new PngOptions());
}

string sourceFile2 = Path.Combine(baseFolder, "Dolota.ai");
string outputFile2 = Path.Combine(outputFolder, "Dolota.png");

using (AiImage image = (AiImage)Image.Load(sourceFile2))
{
    image.Save(outputFile2, new PngOptions());
}

string sourceFile3 = Path.Combine(baseFolder, "ARS_novelty_2108_out_01(1).ai");
string outputFile3 = Path.Combine(outputFolder, "ARS_novelty_2108_out_01(1).png");

using (AiImage image = (AiImage)Image.Load(sourceFile3))
{
    image.Save(outputFile3, new PngOptions());
}

string sourceFile4 = Path.Combine(baseFolder, "bit_gear.ai");
string outputFile4 = Path.Combine(outputFolder, "bit_gear.png");

using (AiImage image = (AiImage)Image.Load(sourceFile4))
{
    image.Save(outputFile4, new PngOptions());
}

string sourceFile5 = Path.Combine(baseFolder, "test.ai");
string outputFile5 = Path.Combine(outputFolder, "test.png");

using (AiImage image = (AiImage)Image.Load(sourceFile5))
{
    image.Save(outputFile5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. แก้ไขการบันทึกไฟล์ psd ที่มีแบบ Stroke Pattern**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "StrokeShapePattern.psd");
string outputFile = Path.Combine(outputFolder, "StrokeShapePattern_output.psd");

Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] newPattern = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    PattResource pattResource;
    foreach (var globalLayerResource in image.GlobalLayerResources)
    {
        if (globalLayerResource is PattResource)
        {
            pattResource = (PattResource)globalLayerResource;
            PattResourceData patternItem = pattResource.Patterns[0]; // Stroke internal pattern data

            patternItem.PatternId = guid.ToString();
            patternItem.Name = newPatternName;
            patternItem.SetPattern(newPattern, newPatternBounds);

            break;
        }
    }

    strokeInternalFillSettings.PatternName = newPatternName;
    strokeInternalFillSettings.PatternId = guid.ToString() + "\0";

    shapeLayer.Update();

    image.Save(outputFile);
}

// ตรวจสอบข้อมูลที่เปลี่ยนแปลง
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    Assert.AreEqual(guid.ToString().ToUpper(), strokeInternalFillSettings.PatternId);
    Assert.AreEqual(newPatternName, strokeInternalFillSettings.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. สไตล์ข้อความไม่ถูกต้องในอ็อบเจกต์สมาร์ทเมื่อเราใช้ ReplaceContents**

{{< highlight csharp >}}
string inputFile = Path.Combine(baseFolder, "source.psd");
string output2 = Path.Combine(outputFolder, "output.png");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, psdLoadOptions))
{
    SmartObjectLayer smartObject = (SmartObjectLayer)psdImage.Layers[1];

    using (PsdImage smartObjectImage = (PsdImage)smartObject.LoadContents(psdLoadOptions))
    {
        smartObject.ReplaceContents(smartObjectImage);
    }

    psdImage.Save(output2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [รูปแบบ AI] แก้ไขการเรนเดอร์ Cubic Bezier ในไฟล์ AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Typography.ai");
string outputFilePath = Path.Combine(outputFolder, "Typography.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. เปลี่ยนกลไก Distort ใน warp**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "crow_grid.psd");
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

**PSDNET-1802. เร่งความเร็ว warp**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "output.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var sw = new Stopwatch();
sw.Start();

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}

sw.Stop();

// ค่าเดิม = 193300
// ค่าใหม่ =  55500
int timeInSec = (int)sw.Elapsed.TotalMilliseconds;
if (timeInSec > 100000)
{
    throw new Exception("การประมวลผลใช้เวลานานเกินไป");
}
{{< /highlight >}}

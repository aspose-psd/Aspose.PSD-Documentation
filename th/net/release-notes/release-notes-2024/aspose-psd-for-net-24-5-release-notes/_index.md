---
title: Aspose.PSD for .NET 24.5 - บันทึกการอัปเดต
type: docs
weight: 80
url: /th/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

หน้านี้ประกอบด้วยบันทึกการอัปเดตสำหรับ [Aspose.PSD for .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **สรุป**                                                                            | **หมวดหมู่** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [รูปแบบ AI] เพิ่มการสนับสนุนสำหรับการจัดการไฟล์ AI ที่มีหัวเรื่อง EPSF                      | คุณลักษณะ      |
| PSDNET-1755 | การโปรเซสซิ่งแบบความโปร่งเฉลี่ยผิดพลาดที่กำลังดูไฟล์ psd                        | ข้อผิดพลาด      |
| PSDNET-1942 | การเรนเดอร์ของเลเยอร์รูปทรงบางส่วนไม่ถูกต้อง                                       | ข้อผิดพลาด      |
| PSDNET-1957 | ข้อยกเว้นเมื่อบันทึกไฟล์ PSD มีขนาดมากกว่า 200 MB และมีขนาดใหญ่                          | ข้อผิดพลาด      |
| PSDNET-1998 | ข้อยกเว้นการบันทึกรูปภาพที่ล้มเหลวเมื่อบันทึกเป็น PDF หลังจากอัปเดตจาก 23.7 เป็น 24.3      | ข้อผิดพลาด      |
| PSDNET-2033 | แก้ไขปัญหาในเมธอด GetFontInfoRecords สำหรับฟอนต์จีน                     | ข้อผิดพลาด      |

## **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่มเติม:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **API ที่ถอนออก:** 
- ไม่มี

## **ตัวอย่างการใช้**

**PSDNET-1755. การโปรเซสซิ่งแบบความโปร่งเฉลี่ยผิดพลาดที่กำลังดูไฟล์ psd**

{{< highlight csharp >}}
// การโปรเซสซิ่งแบบความโปร่งเฉลี่ยถูกประมวลผิดพลาดบนการดูไฟล์ psd
// กำหนด BackgroundContents เป็นสีขาว พื้นที่โปร่งสามารถมีสีขาวได้

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    RawColor backgroundColor = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    backgroundColor.SetAsInt(argbValue); // สีขาว

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = backgroundColor,
    };

    psdImage.Save(outputFile, psdOptions);
}
{{< /highlight >}}

**PSDNET-1897. [รูปแบบ AI] เพิ่มการสนับสนุนสำหรับการจัดการไฟล์ AI ที่มีหัวเรื่อง EPSF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("ออบเจกต์ไม่เท่ากัน");
    }
}

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    AssertAreEqual(image.Layers.Length, 2);
    AssertAreEqual(image.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[0].ColorIndex, -1);
    AssertAreEqual(image.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[1].ColorIndex, -1);

    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. การเรนเดอร์ของเลเยอร์รูปทรงบางส่วนไม่ถูกต้อง**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ShapeLayerTest.psd");
string outputFile = Path.Combine(outputFolder, "ShapeLayerTest_output.psd");
const int ImgToPsdRatio = 256 * 65535;

using (var im = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[2];
    IPath path = shapeLayer.Path;
    IPathShape[] pathShapes = path.GetItems();
    List<BezierKnotRecord> knotsList = new List<BezierKnotRecord>();
    foreach (IPathShape pathShape in pathShapes)
    {
        BezierKnotRecord[] knots = pathShape.GetItems();
        knotsList.AddRange(knots);
    }

    // เปลี่ยนคุณสมบัติของเลเยอร์
    var newShape = new PathShape();

    BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(50, 490),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 490),
                    shapeLayer.Container.Size), // จุดยึด
                PointFToResourcePoint(
                    new PointF(150, 490),
                    shapeLayer.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(490, 150),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 50),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 20),
                    shapeLayer.Container.Size),
            },
        },
    };

    newShape.SetItems(bezierKnots);

    List<IPathShape> newShapes = new List<IPathShape>(pathShapes);
    newShapes.Add(newShape);

    IPathShape[] pathShapeNew = newShapes.ToArray();
    path.SetItems(pathShapeNew);

    shapeLayer.Update();

    im.Save(outputFile, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[2];
    IPath path = shapeLayer.Path;
    IPathShape[] pathShapes = path.GetItems();
    List<BezierKnotRecord> knotsList = new List<BezierKnotRecord>();
    foreach (IPathShape pathShape in pathShapes)
    {
        BezierKnotRecord[] knots = pathShape.GetItems();
        knotsList.AddRange(knots);
    }

    AssertAreEqual(3, pathShapes.Length);
    AssertAreEqual(42, shapeLayer.Left);
    AssertAreEqual(14, shapeLayer.Top);
    AssertAreEqual(1600, shapeLayer.Bounds.Width);
    AssertAreEqual(1086, shapeLayer.Bounds.Height);
}

Point PointFToResourcePoint(PointF point, Size imageSize)
{
    return new Point(
        (int)Math.Round(point.Y * (ImgToPsdRatio / imageSize.Height)),
        (int)Math.Round(point.X * (ImgToPsdRatio / imageSize.Width)));
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "ออบเจกต์ไม่เท่ากัน");
    }
}
{{< /highlight >}}

**PSDNET-1957. ข้อยกเว้นเมื่อบันทึกไฟล์ PSD มีขนาดมากกว่า 200 MB และมีขนาดใหญ่**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");
string outputFile = Path.Combine(outputFolder, "output_raw.psd");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // ต้องไม่มีข้อผิดพลาดที่นี่
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. ข้อยกเว้นเมื่อบันทึกรูปภาพล้มเหลวเมื่อบันทึกเป็น PDF หลังจากอัปเดตจาก 23.7 เป็น 24.3**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "CVFlor.psd");
string outputFile = Path.Combine(outputFolder, "_export.pdf");

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2033. แก้ไขปัญหาในเมธอด GetFontInfoRecords สำหรับฟอนต์จีน**

{{< highlight csharp >}}
var fontFolder = Path.Combine(baseFolder, "Font");
string sourceFile = Path.Combine(baseFolder, "bd-worlds-best-pink.psd");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { fontFolder }, true);
    FontSettings.UpdateFonts();

    using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
    {
        foreach (var layer in image.Layers)
        {
            var textLayer = layer as TextLayer;

            if (textLayer != null)
            {
                if (textLayer.Text == "best")
                {
                    // โดยไม่มีการแก้ไขที่นี่ จะเกิดข้อผิดพลาดเพราะฟอนท์จีน
                    textLayer.UpdateText("SUСCESS");
                }
            }
        }
    }
}
finally
{
    FontSettings.Reset();
    FontSettings.UpdateFonts();
}
{{< /highlight >}}

---
title: Aspose.PSD لـ .NET 24.5 - ملاحظات الإصدار
type: docs
weight: 80
url: /ar/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص**                                                                         | **الفئة**       |
|:------------|:------------------------------------------------------------------------------------|:---------------|
| PSDNET-1897 | [تنسيق AI] إضافة دعم لمعالجة ملفات AI مع ترويسة EPSF                                 | ميزة           |
| PSDNET-1755 | تم معالجة الشفافية النصفية بشكل خاطئ في معاينة ملف PSD                         | خطأ       |
| PSDNET-1942 | تقديم طبقة الشكل جزئيًا غير صحيحة                                             | خطأ       |
| PSDNET-1957 | استثناء عند حفظ ملفات PSD بحجم أكبر من 200 ميجابايت وأبعاد كبيرة                | خطأ       |
| PSDNET-1998 | فشل حفظ الصورة باستثناء عند الحفظ في PDF بعد التحديث من 23.7 إلى 24.3         | خطأ       |
| PSDNET-2033 | إصلاح المشكلة في طريقة GetFontInfoRecords للخطوط الصينية                          | خطأ       |

## **تغييرات واجهة برمجة التطبيقات العامة**
# **الواجهات البرمجية المضافة:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **الواجهات البرمجية المحذوفة:**
- بلا

## **أمثلة الاستخدام:**

**PSDNET-1755. تم معالجة الشفافية النصفية بشكل خاطئ في معاينة ملف PSD**

{{< highlight csharp >}}
// تم معالجة الشفافية النصفية بشكل خاطئ في معاينة ملف PSD.
// تم تعيين BackgroundContents إلى الأبيض. يجب أن تكون المناطق الشفافة ذات لون أبيض.

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    RawColor backgroundColor = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    backgroundColor.SetAsInt(argbValue); // أبيض

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

**PSDNET-1897. [تنسيق AI] إضافة دعم لمعالجة ملفات AI مع ترويسة EPSF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("الكائنات غير متساوية.");
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

**PSDNET-1942. تقديم طبقة الشكل جزئيًا غير صحيحة**

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

    // تغيير خصائص الطبقة
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
                    shapeLayer.Container.Size), // نقطة المرجع
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
        throw new Exception(message ?? "الكائنات غير متساوية.");
    }
}
{{< /highlight >}}

**PSDNET-1957. استثناء عند حفظ ملفات PSD بحجم أكبر من 200 ميجابايت وأبعاد كبيرة**

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
    // لا ينبغي أن يحدث أي خطأ هنا
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. فشل حفظ الصورة باستثناء عند الحفظ في PDF بعد التحديث من 23.7 إلى 24.3**

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

**PSDNET-2033. إصلاح المشكلة في طريقة GetFontInfoRecords للخطوط الصينية**

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
                    // بدون هذا الإصلاح، سيحدث استثناء هنا بسبب الخط الصيني.
                    textLayer.UpdateText("نجاح");
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
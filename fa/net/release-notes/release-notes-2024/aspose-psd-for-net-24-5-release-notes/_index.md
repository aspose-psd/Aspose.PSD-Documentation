---
title: Aspose.PSD for .NET 24.5 - یادداشت‌های انتشار
type: docs
weight: 80
url: /fa/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار [Aspose.PSD برای .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/) است.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                         | **دسته‌بندی** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | اضافه کردن پشتیبانی از رفتار فایل‌های AI با هدر EPSF                      | قابلیت      |
| PSDNET-1755 | ناتوانی در پردازش شفافیت نیمه شفاف در پیش‌نمایش فایل psd                        | باگ      |
| PSDNET-1942 | رندر کردن لایه شکل جزئیاً نادرست                                        | باگ      |
| PSDNET-1957 | خطا هنگام ذخیره کردن فایل‌های PSD با اندازه بیشتر از 200 مگابایت و ابعاد بزرگ | باگ      |
| PSDNET-1998 | خطای شکست در ذخیره کردن تصویر زمان ذخیره به PDF پس از آپدیت از نسخه 23.7 به 24.3   | باگ      |
| PSDNET-2033 | رفع مشکل در متد GetFontInfoRecords برای فونت‌های چینی        | باگ      |

## **تغییرات API عمومی**
# **API‌های اضافه‌شده:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **API‌های حذف‌شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDNET-1755. ناتوانی در پردازش شفافیت نیمه شفاف در پیش‌نمایش فایل psd**

{{< highlight csharp >}}
// ناتوانی در پردازش شفافیت نیمه شفاف در پیش‌نمایش فایل psd.
// BackgroundContents به رنگ سفید اختصاص داده شده است. ناحیه‌های شفاف باید رنگ سفید داشته باشند.

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    RawColor backgroundColor = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    backgroundColor.SetAsInt(argbValue); // سفید

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

**PSDNET-1897. اضافه کردن پشتیبانی از رفتار فایل‌های AI با هدر EPSF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("اشیاء برابر نیستند.");
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

**PSDNET-1942. رندر کردن لایه شکل جزئیاً نادرست**

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

    // تغییر خصوصیات لایه
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
                    shapeLayer.Container.Size), // نقطه مرجع
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
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}
{{< /highlight >}}

**PSDNET-1957. خطا هنگام ذخیره کردن فایل‌های PSD با اندازه بیشتر از 200 مگابایت و ابعاد بزرگ**

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
    // در اینجا نباید هیچ خطا وجود داشته باشد
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. خطای شکست در ذخیره کردن تصویر زمان ذخیره به PDF پس از آپدیت از نسخه 23.7 به 24.3**

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

**PSDNET-2033. رفع مشکل در متد GetFontInfoRecords برای فونت‌های چینی**

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
                    // بدون این ترمیم اینجا خطا خواهد بود به دلیل فونت چینی.
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

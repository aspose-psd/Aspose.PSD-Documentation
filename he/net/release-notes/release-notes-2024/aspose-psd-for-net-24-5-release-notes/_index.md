---
title: Aspose.PSD for .NET 24.5 - הערות לשחרור
type: docs
weight: 80
url: /he/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל את ההערות לשחרור של [Aspose.PSD for .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**   | **סיכום**                                                                            | **קטגוריה** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [פורמט AI] הוספת תמיכה בטיפול בקבצי AI עם כותרת EPSF                              | תכונה       |
| PSDNET-1755 | השקפת השקיפות החלקה נעשית בצורה שגויה בתצוגת הקובץ psd                       | באג      |
| PSDNET-1942 | תצוגת שכבת הצורה לא נכונה לגמרי                                               | באג      |
| PSDNET-1957 | חריגה בעת שמירת קבצי PSD עם גודל גדול יותר מ-200 MB וממדים גדולים              | באג      |
| PSDNET-1998 | יש חריגת כשל בשמירת התמונה כאשר משמירים ל- PDF לאחר עדכון מ-23.7 ל-24.3       | באג      |
| PSDNET-2033 | תיקון בעיה בשיטת GetFontInfoRecords עבור הפונטים הסיניים                       | באג      |

## **שינויים ב- API הציבוריים**
# **APIs שנוספים:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **APIs שהוסרו:**
- אף אחד

## **דוגמאות לשימוש:**

**PSDNET-1755. השקיפות החלקה נעשית בצורה שגויה בתצוגת הקובץ psd**

{{< highlight csharp >}}
// השקיפות החלקה נעשית בצורה שגויה בתצוגת הקובץ psd.
// תוכן הרקע מוקצה ללבן. האזורים השקופים צריכים לכלול צבע לבן.

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    RawColor backgroundColor = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    backgroundColor.SetAsInt(argbValue); // לבן

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

**PSDNET-1897. [פורמט AI] הוספת תמיכה בטיפול בקבצי AI עם כותרת EPSF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("האובייקטים אינם שווים.");
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

**PSDNET-1942. תצוגת שכבת הצורה לא נכונה לגמרי**

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

    // שינוי מאפייני השכבה
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
                    shapeLayer.Container.Size), // נקודת עיגון
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
        throw new Exception(message ?? "האובייקטים אינם שווים.");
    }
}
{{< /highlight >}}

**PSDNET-1957. חריגה בעת שמירת קבצי PSD עם גודל גדול יותר מ-200 MB וממדים גדולים**

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
    // לאמור מאותו מקום לאמור
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. חריגת כשל בשמירת התמונה כאשר משמירים ל- PDF לאחר עדכון מ-23.7 ל-24.3**

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

**PSDNET-2033. תיקון בעיה בשיטת GetFontInfoRecords עבור הפונטים הסיניים**

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
                    // בלעדי התיקון הזה כאן יהיה חריגה בגלל הפונט הסיני.
                    textLayer.UpdateText("הצלחה");
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

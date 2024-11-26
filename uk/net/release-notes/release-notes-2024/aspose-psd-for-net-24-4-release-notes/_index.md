---
title: Примітки до версії Aspose.PSD для .NET 24.4
type: docs
weight: 90
url: /uk/net/aspose-psd-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до версії [Aspose.PSD для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**     | **Зміст**                                            | **Категорія** |
|:------------|:-------------------------------------------------------|:-------------|
| PSDNET-1871 | [Формат AI] Додано обробку ресурсу XObjectForm       | Функціонал      |
| PSDNET-1961 | Додано конструктор для ShapeLayer                     | Функціонал      |
| PSDNET-1879 | Виправлено конвертацію файлу Psd з RGB в CMYK         | Помилка          |
| PSDNET-1966 | Конкретний файл PSD не може бути експортований за допомогою Aspose.PSD | Помилка          |

## **Зміни в публічному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Видалені API:**
- Немає

## **Приклади використання:**

**PSDNET-1871. [Формат AI] Додано обробку ресурсу XObjectForm**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Виправлено конвертацію файлу Psd з RGB в CMYK**

{{< highlight csharp >}}
// Перевірте, що psd файл, конвертований в CMYK + RLE 4 канали із файлу psd у RGB + RLE 4 канали, дійсно має 4 канали
// та HasTransparencyData == false.

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    psdImage.HasTransparencyData = false;

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    psdImage.Save(outputFile, psdOptions);
}

using (PsdImage psdImage = (PsdImage)Image.Load(outputFile))
{
    AssertAreEqual(false, psdImage.HasTransparencyData);
    AssertAreEqual((ushort)4, psdImage.Layers[0].ChannelsCount);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Об'єкти не однакові.");
    }
{{< /highlight >}}}

**PSDNET-1961. Додано конструктор для ShapeLayer**

{{< highlight csharp >}}
string outputFile = Path.Combine(outputFolder, "AddShapeLayer_output.psd");

const int ImgToPsdRatio = 256 * 65535;

using (PsdImage newPsd = new PsdImage(600, 400))
{
    ShapeLayer layer = newPsd.AddShapeLayer();

    var newShape = GenerateNewShape(newPsd.Size);
    List<IPathShape> newShapes = new List<IPathShape>();
    newShapes.Add(newShape);
    layer.Path.SetItems(newShapes.ToArray());

    layer.Update();

    newPsd.Save(outputFile);
}

using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    AssertAreEqual(2, image.Layers.Length);

    ShapeLayer shapeLayer = image.Layers[1] as ShapeLayer;
    ColorFillSettings internalFill = shapeLayer.Fill as ColorFillSettings;
    IStrokeSettings strokeSettings = shapeLayer.Stroke;
    ColorFillSettings strokeFill = shapeLayer.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, shapeLayer.Path.GetItems().Length); // 1 Форма
    AssertAreEqual(3, shapeLayer.Path.GetItems()[0].GetItems().Length); // 3 вузли в формі

    AssertAreEqual(-16127182, internalFill.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, strokeSettings.Size);
    AssertAreEqual(false, strokeSettings.Enabled);
    AssertAreEqual(StrokePosition.Center, strokeSettings.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, strokeSettings.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, strokeSettings.LineJoin);
    AssertAreEqual(-16777216, strokeFill.Color.ToArgb()); // ff000000
}

PathShape GenerateNewShape(Size imageSize)
{
    var newShape = new PathShape();

    PointF point1 = new PointF(20, 100);
    PointF point2 = new PointF(200, 100);
    PointF point3 = new PointF(300, 10);

    BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(point1, imageSize),
                          PointFToResourcePoint(point1, imageSize),
                          PointFToResourcePoint(point1, imageSize),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(point2, imageSize),
                          PointFToResourcePoint(point2, imageSize),
                          PointFToResourcePoint(point2, imageSize),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(point3, imageSize),
                          PointFToResourcePoint(point3, imageSize),
                          PointFToResourcePoint(point3, imageSize),
                      }
         },
    };

    newShape.SetItems(bezierKnots);

    return newShape;
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
        throw new Exception(message ?? "Об'єкти не однакові.");
    }
{{< /highlight >}}}

**PSDNET-1966. Конкретний файл PSD не може бути експортований за допомогою Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "1966source.psd");
string outputPng = Path.Combine(outputFolder, "output.png");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

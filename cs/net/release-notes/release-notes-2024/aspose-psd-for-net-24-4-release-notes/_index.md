---
title: Aspose.PSD pro .NET 24.4 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/aspose-psd-pro-net-24-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                              | **Kategorie** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-1871 | [AI Formát] Přidání zpracování XObjectForm              | Funkce       |
| PSDNET-1961 | Přidat konstruktor pro ShapeLayer                       | Funkce       |
| PSDNET-1879 | Oprava konverze souboru Psd z RGB na CMYK                | Chyba        |
| PSDNET-1966 | Specifický soubor PSD nelze exportovat pomocí Aspose.PSD | Chyba        |

## **Veřejné změny ve veřejném API**
# **Přidané API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Odstraněné API:**
- Žádné

## **Příklady použití:**

**PSDNET-1871. [AI Formát] Přidání zpracování XObjectForm**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Oprava konverze souboru Psd z RGB na CMYK**

{{< highlight csharp >}}
// Zkontrolujte, zda se soubor psd převedený na CMYK + RLE 4 kanály ze souboru psd v RGB + RLE 4 kanály skutečně skládá ze 4 kanálů
// a HasTransparencyData == false.

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
        throw new Exception(message ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1961. Přidat konstruktor pro ShapeLayer**

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

    AssertAreEqual(1, shapeLayer.Path.GetItems().Length); // 1 Tvar
    AssertAreEqual(3, shapeLayer.Path.GetItems()[0].GetItems().Length); // 3 uzly v tvaru

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
        throw new Exception(message ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Specifický soubor PSD nelze exportovat pomocí Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "1966source.psd");
string outputPng = Path.Combine(outputFolder, "output.png");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

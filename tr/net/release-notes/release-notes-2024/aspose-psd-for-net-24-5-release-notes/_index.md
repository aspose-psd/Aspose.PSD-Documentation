---
title: Aspose.PSD for .NET 24.5 - Sürüm Notları
type: docs
weight: 80
url: /tr/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                                  | **Kategori** |
|:------------|:------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [AI Format] AI dosyalarının EPSF başlığı ile işlenmesi için destek ekleme                  | Özellik      |
| PSDNET-1755 | Yarı şeffaflık psd dosyası önizlemesinde yanlış işlenir                                   | Hata         |
| PSDNET-1942 | Şekil Katmanı Rendereleme Kısmen Yanlış                                                   | Hata         |
| PSDNET-1957 | 200 MB'dan büyük boyuttaki ve büyük boyutlardaki PSD dosyalarının kaydedilmesi sırasında exception  | Hata         |
| PSDNET-1998 | 24.3 sürümüne güncellemeden sonra PDF'ye kaydederken resmin kaydedilmesi başarısız oldu exception  | Hata         |
| PSDNET-2033 | GetFontInfoRecords methodundaki Çin Yazı Tipleri için sorunu düzelt                     | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım Örnekleri:**

**PSDNET-1755. Yarı şeffaflık psd dosyası önizlemesinde yanlış işlenir**

{{< highlight csharp >}}
// Yarı şeffaflık psd dosyası önizlemesinde yanlış işlenir.
// BackgroundContents Beyaz olarak atandı. Şeffaf alanlar beyaz renkte olmalıdır.

string kaynakDosya = Path.Combine(baseFolder, "frog_nosymb.psd");
string çıkışDosyası = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(kaynakDosya))
{
    RawColor arkaPlanRengi = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbDeğeri = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    arkaPlanRengi.SetAsInt(argbDeğer); // Beyaz

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = arkaPlanRengi,
    };

    psdImage.Save(çıkışDosyası, psdOptions);
}
{{< /highlight >}}

**PSDNET-1897. [AI Format] AI Dosyalarının EPSF başlığı ile işlenmesi için destek ekleme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "example.ai");
string çıkışDosyaYolu = Path.Combine(outputFolder, "example.png");

void AssertEqual(expected, actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objects are not equal.");
    }
}

using (AiImage image = (AiImage)Image.Load(kaynakDosya))
{
    AssertAreEqual(image.Layers.Length, 2);
    AssertAreEqual(image.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[0].ColorIndex, -1);
    AssertAreEqual(image.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[1].ColorIndex, -1);

    image.Save(çıkışDosyaYolu, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. Şekil Katmanı Rendereleme Kısmen Yanlış**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "ShapeLayerTest.psd");
string çıkışDosyası = Path.Combine(outputFolder, "ShapeLayerTest_output.psd");
const int ImgToPsdRatio = 256 * 65535;

using (var im = (PsdImage)Image.Load(kaynakDosya))
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

    // Katman özelliklerini değiştir
    var yeniŞekil = new PathShape();

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
                    shapeLayer.Container.Size), // Anchor point
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

    yeniŞekil.SetItems(bezierKnots);

    List<IPathShape> yeniŞekiller = new List<IPathShape>(pathShapes);
    yeniŞekiller.Add(yeniŞekil);

    IPathShape[] pathShapeNew = yeniŞekiller.ToArray();
    path.SetItems(pathShapeNew);

    shapeLayer.Update();

    im.Save(çıkışDosyası, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(çıkışDosyası))
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

void AssertAreEqual(expected, actual, message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1957. 200 MB'dan büyük boyuttaki ve büyük boyutlardaki PSD dosyalarının kaydedilmesi sırasında exception**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "bigfile.psd");
string çıkışDosyası = Path.Combine(outputFolder, "output_raw.psd");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, loadOptions))
{
    // Burada herhangi bir hata olmamalı
    psdImage.Save(çıkışDosyası, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. 23.7'den 24.3'e güncellemeden sonra PDF'ye kaydederken resmin kaydedilmesi başarısız oldu exception**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "CVFlor.psd");
string çıkışDosyası = Path.Combine(outputFolder, "_export.pdf");

using (var psdImage = (PsdImage)Image.Load(kaynakDosya))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(çıkışDosyası, saveOptions);
}
{{< /highlight >}}

**PSDNET-2033. Çin Yazı Tipleri için GetFontInfoRecords methodundaki sorunu düzeltme**

{{< highlight csharp >}}
var fontKlasörü = Path.Combine(baseFolder, "Font");
string kaynakDosya = Path.Combine(baseFolder, "bd-worlds-best-pink.psd");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { fontKlasörü }, true);
    FontSettings.UpdateFonts();

    using (PsdImage image = (PsdImage)PsdImage.Load(kaynakDosya, psdLoadOptions))
    {
        foreach (var layer in image.Layers)
        {
            var textLayer = layer as TextLayer;

            if (textLayer != null)
            {
                if (textLayer.Text == "best")
                {
                    // Çin yazı tipinden dolayı burada bir hata olmayacak
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

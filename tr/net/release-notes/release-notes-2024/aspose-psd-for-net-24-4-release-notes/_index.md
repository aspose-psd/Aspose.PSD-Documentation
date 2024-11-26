---
title: Aspose.PSD için .NET 24.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-psd-icin-net-24-4-s%C3%BCr%C3%BCm-notlar%C4%B1/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                | **Kategori** |
|:------------|:--------------------------------------------------------|:-------------|
| PSDNET-1871 | [AI Format] XObjectForm kaynak işleme ekleme             | Özellik      |
| PSDNET-1961 | ShapeLayer için Constructor ekleme                       | Özellik      |
| PSDNET-1879 | RGB'den CMYK'ya Psd dosyasının dönüşümünü düzeltme        | Hata         |
| PSDNET-1966 | Belirli bir PSD dosyası, Aspose.PSD kullanılarak dışa aktarılamaz | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-1871. [AI Format] XObjectForm kaynak işleme ekleme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "ornek.ai");
string çıktıDosyaYolu = Path.Combine(outputFolder, "ornek.png");

using (AiImage resim = (AiImage)Image.Load(kaynakDosya))
{
    resim.Save(çıktıDosyaYolu, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. RGB'den CMYK'ya Psd dosyasının dönüşümünü düzeltme**

{{< highlight csharp >}}
// Psd dosyasının gerçekten 4 kanala sahip olduğunu ve HasTransparencyData == false olduğunu kontrol edin.

string kaynakDosya = Path.Combine(baseFolder, "frog_nosymb.psd");
string çıktıDosyası = Path.Combine(outputFolder, "frog_nosymb_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(kaynakDosya))
{
    psdImage.HasTransparencyData = false;

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    psdImage.Save(çıktıDosyası, psdOptions);
}

using (PsdImage psdImage = (PsdImage)Image.Load(çıktıDosyası))
{
    AssertAreEqual(false, psdImage.HasTransparencyData);
    AssertAreEqual((ushort)4, psdImage.Layers[0].ChannelsCount);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1961. ShapeLayer için Constructor ekleme**

{{< highlight csharp >}}
string çıktıDosyası = Path.Combine(outputFolder, "AddShapeLayer_output.psd");

const int ImgToPsdRatio = 256 * 65535;

using (PsdImage newPsd = new PsdImage(600, 400))
{
    ShapeLayer layer = newPsd.AddShapeLayer();

    var yeniŞekil = GenerateNewShape(newPsd.Size);
    List<IPathShape> yeniŞekiller = new List<IPathShape>();
    yeniŞekiller.Add(yeniŞekil);
    layer.Path.SetItems(yeniŞekiller.ToArray());

    layer.Update();

    newPsd.Save(çıktıDosyası);
}

using (PsdImage resim = (PsdImage)Image.Load(çıktıDosyası))
{
    AssertAreEqual(2, resim.Layers.Length);

    ShapeLayer şekilKatmanı = resim.Layers[1] as ShapeLayer;
    ColorFillSettings içDoldurma = şekilKatmanı.Fill as ColorFillSettings;
    IStrokeSettings vuruşAyarları = şekilKatmanı.Stroke;
    ColorFillSettings vuruşDoldurma = şekilKatmanı.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, şekilKatmanı.Path.GetItems().Length); // 1 Şekil
    AssertAreEqual(3, şekilKatmanı.Path.GetItems()[0].GetItems().Length); // 1 Şekilde 3 düğüm

    AssertAreEqual(-16127182, içDoldurma.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, vuruşAyarları.Size);
    AssertAreEqual(false, vuruşAyarları.Enabled);
    AssertAreEqual(StrokePosition.Center, vuruşAyarları.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, vuruşAyarları.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, vuruşAyarları.LineJoin);
    AssertAreEqual(-16777216, vuruşDoldurma.Color.ToArgb()); // ff000000
}

PathShape GenerateNewShape(Size resimBoyutu)
{
    var yeniŞekil = new PathShape();

    PointF nokta1 = new PointF(20, 100);
    PointF nokta2 = new PointF(200, 100);
    PointF nokta3 = new PointF(300, 10);

    BezierKnotRecord[] bezierNoktaları = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(nokta1, resimBoyutu),
                          PointFToResourcePoint(nokta1, resimBoyutu),
                          PointFToResourcePoint(nokta1, resimBoyutu),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(nokta2, resimBoyutu),
                          PointFToResourcePoint(nokta2, resimBoyutu),
                          PointFToResourcePoint(nokta2, resimBoyutu),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(nokta3, resimBoyutu),
                          PointFToResourcePoint(nokta3, resimBoyutu),
                          PointFToResourcePoint(nokta3, resimBoyutu),
                      }
         },
    };

    yeniŞekil.SetItems(bezierNoktaları);

    return yeniŞekil;
}

Point PointFToResourcePoint(PointF nokta, Size resimBoyutu)
{
    return new Point(
        (int)Math.Round(nokta.Y * (ImgToPsdRatio / resimBoyutu.Height)),
        (int)Math.Round(nokta.X * (ImgToPsdRatio / resimBoyutu.Width)));
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Belirli bir PSD dosyası, Aspose.PSD kullanılarak dışa aktarılamaz**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "1966source.psd");
string çıktıPng = Path.Combine(outputFolder, "çıktı.png");

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Save(çıktıPng, new PngOptions());
}
{{< /highlight >}}

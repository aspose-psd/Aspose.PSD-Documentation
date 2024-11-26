---
title: Aspose.PSD for .NET 23.5 - Sürüm Notları
type: docs
weight: 80
url: /tr/net/aspose-psd-for-net-23-5-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                    | **Kategori** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-343  | Filtre Desteği: Keskinleştir -> Keskinleştir                                | Özellik     |
| PSDNET-1179 | 32 bitle bölmelere sahip olmayan PSD dosyasını (RGB/8 bit veya RGB/16 bit) kaydetme | Özellik      |
| PSDNET-1408 | ShapeLayer için vsms veya vmsk kaynaklarından yol nesnelerini işleme ekle     | Özellik      |
| PSDNET-1508 | Mesh noktalarının birbirleri üzerindeki etkisini ekleyin                     | Özellik      |


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **Kaldırılan API'ler:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **Kullanım Örnekleri:**

**PSDNET-343. Filtre Desteği: Keskinleştir -> Keskinleştir**

{{< highlight csharp >}}
string sourceFile = "keskin_kaynak.psd";
string outputPsd = "keskin_cikti.psd";
string outputPng = "keskin_cikti.png";

void BeklenenleEşitseNesneleriKontrolEt(object beklenen, object gerçek)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception("Nesneler eşit değil.");
    }
}

using (var görüntü = (PsdImage)Image.Load(sourceFile))
{
    SmartObjectLayer akıllıObj = (SmartObjectLayer)görüntü.Layers[1];

    // akıllı filtreleri düzenle
    SharpenSmartFilter keskinleştir = (SharpenSmartFilter)akıllıObj.SmartFilters.Filters[0];

    // filtre değerlerini kontrol et
    BeklenenleEşitseNesneleriKontrolEt(BlendMode.Normal, keskinleştir.BlendMode);
    BeklenenleEşitseNesneleriKontrolEt(100d, keskinleştir.Opacity);
    BeklenenleEşitseNesneleriKontrolEt(true, keskinleştir.IsEnabled);

    // filtre değerlerini güncelle
    keskinleştir.BlendMode = BlendMode.Divide;
    keskinleştir.Opacity = 75;
    keskinleştir.IsEnabled = false;

    // yeni filtre öğeleri ekle
    var filtreler = new List<SmartFilter>(akıllıObj.SmartFilters.Filters);
    filtreler.Add(new SharpenSmartFilter());
    akıllıObj.SmartFilters.Filters = filtreler.ToArray();

    // değişiklikleri uygula
    akıllıObj.SmartFilters.UpdateResourceValues();
    akıllıObj.UpdateModifiedContent();

    görüntü.Save(outputPsd);
    görüntü.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. PSD dosyasını (RGB/8 bit veya RGB/16 bit) 32 bit katmanlara sahip olmadan kaydetme**

{{< highlight csharp >}}
string girişDosyası = "giriş_8bit_rle.psd";
string çıktıPsdDosyası = "çıktı_32bit.psd";
string çıktıResimDosyası32 = "32bitten_çıktı.png";

using (PsdImage kaynakImg = (PsdImage)Image.Load(girişDosyası))
{
    PsdSeçenekleri tümSeçenekler = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    kaynakImg.Save(çıktıPsdDosyası, tümSeçenekler);

    using (var img32 = Image.Load(çıktıPsdDosyası))
    {
        img32.Save(çıktıResimDosyası32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. ShapeLayer için vsms veya vmsk kaynaklarından yol nesnelerini işleme ekle**

{{< highlight csharp >}}
string kaynakDosya = "ShapeLayerTest.psd";
string çıktıDosya = "ShapeLayerTest-çıktı.psd";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer şekilKatmanı = resim.Layers[1];
    VectorPathDataResource vektörYolVeriKaynağı = (VectorPathDataResource)şekilKatmanı.Resources[1];

    bool tümPiksellerleBaşlayanDolgu;
    List<IPathShape> şekiller = GetShapesFromResource(vektörYolVeriKaynağı, out tümPiksellerleBaşlayanDolgu);

    // Bir şekli kaldır
    şekiller.RemoveAt(1);

    // Değişiklik yapılan verileri kaynağa kaydet
    List<VectorPathRecord> yol = new List<VectorPathRecord>();
    yol.Add(new PathFillRuleRecord(null));
    yol.Add(new InitialFillRuleRecord(tümPiksellerleBaşlayanDolgu));

    for (ushort i = 0; i < şekiller.Count; i++)
    {
        PathShape şekil = (PathShape)şekiller[i];
        şekil.ShapeIndex = i;
        yol.AddRange(şekil.ToVectorPathRecords());
    }

    vektörYolVeriKaynağı.Paths = yol.ToArray();

    resim.Save(çıktıDosya);
}

// Kaydedilen dosyadaki değişen değerleri kontrol et
using (PsdImage resim = (PsdImage)Image.Load(çıktıDosya, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer şekilKatmanı = resim.Layers[1];
    VectorPathDataResource vektörYolVeriKaynağı = (VectorPathDataResource)şekilKatmanı.Resources[1];

    bool tümPiksellerleBaşlayanDolgu;
    List<IPathShape> şekiller = GetShapesFromResource(vektörYolVeriKaynağı, out tümPiksellerleBaşlayanDolgu);

    // Kaydedilen dosyanın 1 şekle sahip olması gerekir
    BeklenenleEşitseNesneleriKontrolEt(1, şekiller.Count);
}

void BeklenenleEşitseNesneleriKontrolEt(object beklenen, object gerçek, string mesaj = null)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception(mesaj ?? "Nesneler eşit değil.");
    }
}

List<IPathShape> GetShapesFromResource(VectorPathDataResource vektörYolVeriKaynağı, out bool tümPiksellerleBaşlayanDolgu)
{
    List<IPathShape> şekiller = new List<IPathShape>();
    LengthRecord uzunlukKaydı = null;
    tümPiksellerleBaşlayanDolgu = false;
    List<BezierKnotRecord> bezierKnotKayıtları = new List<BezierKnotRecord>();

    foreach (var yolKaydı in vektörYolVeriKaynağı.Paths)
    {
        if (yolKaydı is LengthRecord)
        {
            if (bezierKnotKayıtları.Count > 0)
            {
                şekiller.Add(new PathShape(uzunlukKaydı, bezierKnotKayıtları.ToArray()));
                uzunlukKaydı = null;
                bezierKnotKayıtları.Clear();
            }

            uzunlukKaydı = (LengthRecord)yolKaydı;
        }
        else if (yolKaydı is BezierKnotRecord)
        {
            bezierKnotKayıtları.Add((BezierKnotRecord)yolKaydı);
        }
        else if (yolKaydı is InitialFillRuleRecord)
        {
            InitialFillRuleRecord başlangıçDolguKurallıKayıt = (InitialFillRuleRecord)yolKaydı;
            tümPiksellerleBaşlayanDolgu = başlangıçDolguKurallıKayt.IsFillStartsWithAllPixels;
        }
    }

    if (bezierKnotKayıtları.Count > 0)
    {
        şekiller.Add(new PathShape(uzunlukKaydı, bezierKnotKayıtları.ToArray()));
        uzunlukKaydı = null;
        bezierKnotKayıtları.Clear();
    }

    return şekiller;
}
{{< /highlight >}}

**PSDNET-1508. Mesh noktalarının birbirlerine etkisini ekleyin**

{{< highlight csharp >}}
string kaynakDosya = "Alt_Sağ.psd";
string çıktıDosya = "çıktı.png";

using (var resim = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    resim.Save(çıktıDosya, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}
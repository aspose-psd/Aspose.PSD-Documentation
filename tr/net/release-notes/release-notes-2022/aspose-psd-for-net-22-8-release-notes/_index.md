---
title: Aspose.PSD için .NET 22.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-22-8-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1225|Yükleyicideki sorunları araştırma ve düzeltme|Geliştirme|
|PSDNET-800|PSD Dosyasından Kare Zaman Çizelgesi Desteği|Özellik|
|PSDNET-1219|'mlst' kaynağının ShmdResource içinde alt kaynak olarak bulunması desteği|Özellik|
|PSDNET-814|Katmanın karıştırma seçenekleri etkileşimlerini çağırdığımızda katmanın Hash değerinin değişmesi|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-800. PSD Dosyasından Kare Zaman Çizelgesi Desteği**

{{< highlight csharp >}}
string kaynakDosya = "image1219.psd";
string ciktiPsd = "output_image800.psd";

using (PsdImage psdResim = (PsdImage)Image.Load(kaynakDosya))
{
    TimeLine zamanCizelgesi = TimeLine.InitializeFrom(psdResim);

    // 1. karenin atılma yöntemini değiştir
    zamanCizelgesi.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // 2. karedeki gecikmeyi değiştir
    zamanCizelgesi.Frames[1].Delay = 15;

    // 2. karedeki 'Katman 1' opaklığını değiştir
    LayerState katmanDurumu11 = zamanCizelgesi.Frames[1].LayerStates[zamanCizelgesi.LayerIds[1]];
    katmanDurumu11.Opacity = 50;

    // 'Katman 1'i 3. karede sol-alt köşeye taşı
    LayerState katmanDurumu21 = zamanCizelgesi.Frames[2].LayerStates[zamanCizelgesi.LayerIds[1]];
    katmanDurumu21.Offset = new Point(-50, 230);

    // Yeni kare ekle
    List<Frame> kareler = new List<Frame>(zamanCizelgesi.Frames);
    kareler.Add(new Frame(zamanCizelgesi));
    zamanCizelgesi.Frames = kareler.ToArray();

    // 'Katman 1'in 4. karedeki karışım modunu değiştir
    LayerState katmanDurumu31 = zamanCizelgesi.Frames[3].LayerStates[zamanCizelgesi.LayerIds[1]];
    katmanDurumu31.BlendMode = BlendMode.Dissolve;

    // Değişiklikleri PsdResim örneğine uygula
    zamanCizelgesi.ApplyTo(psdResim);
    psdResim.Save(ciktiPsd);
}
{{< /highlight >}}

**PSDNET-814. Katmanın karıştırma seçenekleri etkileşimlerini çağırdığımızda katmanın Hash değerinin değişmesi**

{{< highlight csharp >}}
string kaynakDosya = "AllTypesLayerPsd.psd";

using (var resim = (PsdImage)Image.Load(kaynakDosya))
{
    var katman = resim.Layers[0];
    var baslangicHash = katman.GetHashCode();
    var etkiler = katman.BlendingOptions.Effects;
    var sonHash = katman.GetHashCode();

    if (baslangicHash != sonHash)
    {
        throw new Exception("Hash değişmemeli");
    }
}
{{< /highlight >}}

**PSDNET-1219. 'ShmdResource' içinde alt kaynak olarak bulunan 'mlst' kaynağını destekleme**

{{< highlight csharp >}}
string kaynakDosya = "image1219.psd";
string ciktiPsd = "output_image1219.psd";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    Layer katman1 = resim.Layers[1];
    ShmdResource shmdKaynak = (ShmdResource)katman1.Resources[8];
    MlstResource mlstKaynak = (MlstResource)shmdKaynak.SubResources[0];

     ListStructure katmanDurumlariListesi = (ListStructure)mlstKaynak.Items[1];
    DescriptorStructure frame1KatmanDurumu = (DescriptorStructure)katmanDurumlariListesi.Types[1];
    BooleanStructure katmanEtkin = (BooleanStructure)frame1KatmanDurumu.Structures[0];

    // 1. karedeki 'Katman 1'i etkisizleştir
    katmanEtkin.Value = false;

    resim.Save(ciktiPsd);
}
{{< /highlight >}}

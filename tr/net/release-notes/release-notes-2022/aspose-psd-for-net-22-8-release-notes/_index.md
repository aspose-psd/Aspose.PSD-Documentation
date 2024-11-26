---
title: Aspose.PSD for .NET 22.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-22-8-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa [Aspose.PSD for .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1225|Kurulumdaki sorunları araştırmak ve düzeltmek|Geliştirme|
|PSDNET-800|PSD Dosyasından Kare Zaman Çizelgesi Desteği|Özellik|
|PSDNET-1219|ShmdResource içinde bulunan 'mlst' kaynağını destekleme|Özellik|
|PSDNET-814|layer.BlendingOptions.Effects çağrıldığında Katmanın Hash'ini değiştir|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
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


# **Kaldırılan API'lar:**
- Yok


## **Kullanım örnekleri:**

**PSDNET-800. PSD Dosyasından Kare Zaman Çizelgesi Desteği**

{{< highlight csharp >}}
string kaynakDosya = "resim1219.psd";
string ciktiPsd = "çıktı_resim800.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(kaynakDosya))
{
    TimeLine zamanÇizgisi = TimeLine.InitializeFrom(psdImage);

    // 1. karenin atılma yöntemini değiştir
    zamanÇizgisi.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // 2. karenin gecikmesini değiştir
    zamanÇizgisi.Frames[1].Delay = 15;

    // 2. karede 'Katman 1' in opaklığını değiştir
    LayerState katmanDurumu11 = zamanÇizgisi.Frames[1].LayerStates[zamanÇizgisi.LayerIds[1]];
    katmanDurumu11.Opacity = 50;

    // 'Katman 1' i 3. çerçevede sola-alt köşeye taşı
    LayerState katmanDurumu21 = zamanÇizgisi.Frames[2].LayerStates[zamanÇizgisi.LayerIds[1]];
    katmanDurumu21.Offset = new Point(-50, 230);

    // Yeni kare ekleyin
    List<Frame> kareler = new List<Frame>(zamanÇizgisi.Frames);
    kareler.Add(new Frame(zamanÇizgisi));
    zamanÇizgisi.Frames = kareler.ToArray();

    // 'Katman 1' in 4. çerçevedeki karışım modunu değiştir
    LayerState katmanDurumu31 = zamanÇizgisi.Frames[3].LayerStates[zamanÇizgisi.LayerIds[1]];
    katmanDurumu31.BlendMode = BlendMode.Dissolve;

    // Değişiklikleri PsdImage örneğine uygula
    zamanÇizgisi.ApplyTo(psdImage);
    psdImage.Save(ciktiPsd);
}
{{< /highlight >}}

**PSDNET-814. layer.BlendingOptions.Effects çağrıldığında Katmanın Hash'ini değiştir**

{{< highlight csharp >}}
string kaynakDosya = "TümTiplerLayerPsd.psd";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    var katman = görüntü.Layers[0];
    var başlangıçHash = katman.GetHashCode();
    var effects = katman.BlendingOptions.Effects;
    var bitişHash = katman.GetHashCode();

    if (başlangıçHash != bitişHash)
    {
        throw new Exception("Hash değişmemeli");
    }
}
{{< /highlight >}}

**PSDNET-1219. ShmdResource içinde bulunan 'mlst' kaynağını destekleme**

{{< highlight csharp >}}
string kaynakDosya = "resim1219.psd";
string ciktiPsd = "çıktı_resim1219.psd";

using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    Layer katman1 = görüntü.Layers[1];
    ShmdResource shmdKaynak = (ShmdResource)katman1.Resources[8];
    MlstResource mlstKaynak = (MlstResource)shmdKaynak.SubResources[0];

    ListStructure katmanDurumlarıListesi = (ListStructure)mlstKaynak.Items[1];
    DescriptorStructure karelerDurum1 = (DescriptorStructure)katmanDurumlarıListesi.Types[1];
    BooleanStructure katmanEtkin = (BooleanStructure)karelerDurum1.Structures[0];

    // 1. karedeki katmanı devre dışı bırak
    katmanEtkin.Value = false;

    görüntü.Save(ciktiPsd);
}
{{< /highlight >}}

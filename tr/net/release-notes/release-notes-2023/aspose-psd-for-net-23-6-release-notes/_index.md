---
title: Aspose.PSD için .NET 23.6 - Sürüm Notları
type: docs
weight: 70
url: /tr/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:----------|:------------|
| PSDNET-1401 | Zamana Göre API'yi Yeniden Düzenle | İyileştirme |
| PSDNET-1517 | Warp Rendere Eyleminde Sanal Nesnelerin Yeniden İşlenmesini Kaldır | İyileştirme |
| PSDNET-1528 | Warp Rendere Optimizasyon Eylemi | İyileştirme |
| PSDNET-147  | Eşik Ayarlama Katmanının Desteği | Özellik |
| PSDNET-149  | Seçici Renk Ayarlama Katmanının Desteği | Özellik |
| PSDNET-801  | PSD Zamana Çizgisinin Animasyonlu Gif Dosyasına Aktarılabilme Yeteneği | Özellik |
| PSDNET-1555 | Metin Katmanı için Dikdörtgensel Çerçevesizlık Desteği | Özellik |
| PSDNET-1582 | Şekil Katmanının Desteği | Özellik |
| PSDNET-864  | Akıllı nesne içindeki görüntünün güncellenmemesi | Hata |
| PSDNET-1404 | PSD dosyası RGB ve Lab modlarının 3 kanaldan az veya 4 kanaldan fazla içerememesi nedeniyle PSD olarak kaydedilemiyor | Hata |
| PSDNET-1546 | Metin Hizalama, Photoshop'un düzenleme modunda Metin Katmanı açıldığında kayboluyor | Hata |
| PSDNET-1548 | PSD dosyasını kaydederken boş referans istisnası | Hata |
| PSDNET-1578 | Şekil Katmanının yüklenmesinde istisna: Vektör başlangıç sınırları için noktalar henüz desteklenmiyor | Hata |
| PSDNET-1579 | Vogk Kaynağının yüklenmesinde istisna: Noktalar DoubleStructures olarak kaydedildi, biz UnitStructures olarak okuyoruz | Hata |
| PSDNET-1581 | Şekil Katmanının Katman Türü boş | Hata |


## **Herkese Açık API Değişiklikleri**
# **Eklenen API'ler:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Kaldırılan API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
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


## **Kullanım Örnekleri:**

**PSDNET-147. Eşik Ayarlama Katmanı Desteği**

{{< highlight csharp >}}
string eşikKatmanlıKaynakDosya = "çiçekler_eşik_kaynak.psd";
string eşikKatmanlıÇıktıPsd = "çiçekler_eşik_çıktı.psd";
string eşikKatmanlıÇıktıPng = "çiçekler_eşik_çıktı.png";

string eşiksizKaynakDosya = "çiçekler_kaynak.psd";
string eşiksizÇıktıPsd = "çiçekler_çıktı.psd";
string eşiksizÇıktıPng = "çiçekler_çıktı.png";

void BeklenenleEşitMi(object beklenen, object gerçek)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception("Nesneler eşit değil.");
    }
}

// Görüntüden Eşik ayarlama katmanını al, kontrol et ve değiştir.
using (var görüntü = (PsdImage)Image.Load(eşikKatmanlıKaynakDosya))
{
    foreach (var katman in görüntü.Layers)
    {
        if (katman is ThresholdLayer)
        {
            // Eşik ayarlama katmanını al.
            ThresholdLayer eşikKatmanı = (ThresholdLayer)katman;
            var seviye = eşikKatmanı.Seviye;

            // Katman parametrelerini kontrol et.
            BeklenenleEşitMi(seviye, (kısa)115);

            // Katman parametrelerini ayarla.
            eşikKatmanı.Seviye = 50;

            görüntü.Save(eşikKatmanlıÇıktıPsd);
            görüntü.Save(eşikKatmanlıÇıktıPng, yeni PngOptions());
        }
    }
}

// Görüntüye Eşik ayarlama katmanını ekle ve ayarla.
using (var görüntü = (PsdImage)Image.Load(eşiksizKaynakDosya))
{
    // Eşik Ayarlama katmanı ekle.
    ThresholdLayer eşikKatmanı = görüntü.AddThresholdAdjustmentLayer();

    // Katman parametrelerini ayarla.
    eşikKatmanı.Seviye = 115;

    görüntü.Save(eşiksizÇıktıPsd);
    görüntü.Save(eşiksizÇıktıPng, yeni PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Seçici Renk Ayarlama Katmanı Desteği**

... (Diğer örnekler için özgün dosyayı gözden geçiriniz)
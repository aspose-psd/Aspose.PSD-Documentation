---
title: Aspose.PSD için .NET 22.5 - Sürüm Notları
type: docs
weight: 80
url: /tr/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içermektedir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-952|ILayerEffect Arayüzüne EffectType özelliğini ekle|Özellik|
|PSDNET-1146|ChannelData Sınıfının Refaktörü|Geliştirme|
|PSDNET-657|Opacity özelliğinin DropShadowEffect için çalışmasını sağlayın|Hata|
|PSDNET-825|Belirli bir durumda ayar katmanının transparan katman üzerinden yanlış çizilmesi|Hata|
|PSDNET-1168|Colorize yöntemini geliştirin. Grileştirme + doygunluk %100 olmadığında doğru rengi ayarla|Hata|
|Makale|[Aspose.PSD'nin Docker'da Nasıl Çalıştırılacağı](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Dokümantasyon|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EffectType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.BevelEmboss


# **Kaldırılan API'lar:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Kullanım örnekleri:**

**PSDNET-657. DropShadowEffect için Opacity özelliğinin çalışmasını sağlama**

{{< highlight csharp >}}
string girişDosyası = "giriş.psd";
string çıkışResmi20 = "çıkışResmi20.png";
string çıkışResmi200 = "çıkışResmi200.png";

using (PsdImage psdResmi = (PsdImage)Image.Load(girişDosyası, new LoadOptions()))
{
    Katman çalışmaKatmanı = psdResmi.Layers[1];

    DropShadowEffect dropGölgeEtkisi = çalışmaKatmanı.BlendingOptions.AddDropShadow();
    dropGölgeEtkisi.Distance = 0;
    dropGölgeEtkisi.Size = 8;

    // Opacity = 20 örneği
    dropGölgeEtkisi.Opacity = 20;
    psdResmi.Save(çıkışResmi20, new PngOptions());

    // Opacity = 200 örneği
    dropGölgeEtkisi.Opacity = 200;
    psdResmi.Save(çıkışResmi200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Belirli bir durumda ayar katmanının transparan katman üzerinden yanlış çizilmesi**

{{< highlight csharp >}}
string kaynakDosya = "giriş_825.psd";
string çıkışPng = "çıkış_psdnet825.png";

using (var psdResmi = (PsdImage)Image.Load(kaynakDosya))
{
    foreach (var öge in psdResmi.Layers)
    {
        öge.IsVisible = false;
    }
    var katman = psdResmi.Layers[3];
    psdResmi.Layers[1].IsVisible = true;
    psdResmi.Layers[3].IsVisible = true;
    psdResmi.Layers[4].IsVisible = true;
    psdResmi.Layers[7].IsVisible = true;

    var genişlik = katman.Width;
    var yükseklik = katman.Height;
    var katmanSınırları = new Rectangle(katman.Left, katman.Top, genişlik, yükseklik);
    var sınırlar = new Rectangle(0, 0, genişlik, yükseklik);
    var görüntü = new PsdImage(sınırlar.Width, sınırlar.Height);

    görüntü.SaveArgb32Pixels(sınırlar, psdResmi.LoadArgb32Pixels(katmanSınırları));

    görüntü.Save(çıkışPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. ILayerEffect Arayüzüne EffectType özelliğini ekle**

{{< highlight csharp >}}
string girişDosyası = "giriş.psd";
string çıkışOlmadan = "çıkışOlmadan.png";
string çıkışİle = "çıkışİle.png";

using (PsdImage psdResmi = (PsdImage)Image.Load(girişDosyası, new LoadOptions()))
{
    psdResmi.Save(çıkışOlmadan, new PngOptions());

    Katman çalışmaKatmanı = psdResmi.Layers[1];

    DropShadowEffect dropGölgeEtkisi = çalışmaKatmanı.BlendingOptions.AddDropShadow();
    dropGölgeEtkisi.Distance = 0;
    dropGölgeEtkisi.Size = 8;
    dropGölgeEtkisi.Opacity = 20;

    foreach (ILayerEffect iEtki in çalışmaKatmanı.BlendingOptions.Effects)
    {
        if (iEtki.EffectType == LayerEffectsTypes.DropShadow)
        {
            // yakalandı
            psdResmi.Save(çıkışİle, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Colorize yöntemini geliştirin. Grileştirme + doygunluk %100 olmadığında doğru rengi ayarla**

{{< highlight csharp >}}
string srcDosya = "Colorize.psd";            
string çıkışBasit = "çıkış_basit.png";
string çıkışColorize = "çıkış_colorize.png";

using (var psdResmi = (PsdImage)Image.Load(srcDosya))
{
    // Colorize özelliği olmayan resim
    psdResmi.Save(çıkışBasit, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Colorize özelliğini ayarla
    foreach (Layer katman in psdResmi.Layers)
    {
        if (katman is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)katman;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Colorize özelliği olan resim
    psdResmi.Save(çıkışColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

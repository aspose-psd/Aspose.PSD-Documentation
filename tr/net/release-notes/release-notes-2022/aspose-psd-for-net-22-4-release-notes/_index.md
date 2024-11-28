---
title: Aspose.PSD for .NET 22.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-psd-for-net-22-4-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.4](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-261|Dış Parlama Katman Etkisinin Oluşturulması|Özellik|
|PSDNET-1123|Sha256 Lisansının Desteklenmesi|Geliştirme|
|PSDNET-1107|Çoklu satırlı metnin Photoshop'taki sonuçla eşleşmeyen konumu|Hata|
|PSDNET-1113|Metin kaynak verilerinin ayrıştırılmasında PSD dosyasının yüklenmesi ile ilgili sorun|Hata|
|PSDNET-1129|PSD olarak kaydedildikten sonra özel desenin yanlış konumu|Hata|


## **Halka açık API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.JustificationMode
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Left
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Right
- F:Aspose.PSD.FileFormats.Psd.JustificationMode.Center
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddOuterGlow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Intensity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsAntiAliasing
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Noise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.IsSoftBlend
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Range
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.Jitter


# **Kaldırılan API'ler:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-261. Dış Parlama Katman Etkisinin Oluşturulması**
{{< highlight csharp >}}
string src = "GreenLayer.psd";
string output = "output261.png";

using (var image = (PsdImage)Image.Load(src))
{
    OuterGlowEffect effect = image.Layers[1].BlendingOptions.AddOuterGlow();
    effect.Range = 10;
    effect.Spread = 10;
    ((IColorFillSettings)effect.FillColor).Color = Color.Red;
    effect.Opacity = 128;
    effect.BlendMode = BlendMode.Normal;

    image.Save(output, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1107. Çoklu satırlı metnin Photoshop'taki sonuçla eşleşmeyen konumu**

{{< highlight csharp >}}
string src = "source1107.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var image = (PsdImage)Image.Load(src))
{ 
   var txtLayer = image.AddTextLayer("Satır 1 metin\rSatır 2 metin\rSatır 3 metin", new Rectangle(200, 200, 500, 500));
   var portions = txtLayer.TextData.Items;

   portions[0].Paragraph.Justification = JustificationMode.Left;
   portions[1].Paragraph.Justification = JustificationMode.Right;
   portions[2].Paragraph.Justification = JustificationMode.Center;

   txtLayer.TextData.UpdateLayerData();

   image.Save(outputPsd);
   image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1113. Metin kaynak verilerinin ayrıştırılmasında PSD dosyasının yüklenmesi ile ilgili sorun**

{{< highlight csharp >}}
string sourceFile = "input.psd";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    // Başarılı bir şekilde yüklendi.
}
{{< /highlight >}}

**PSDNET-1129. PSD olarak kaydedildikten sonra özel desenin yanlış konumu**

{{< highlight csharp >}}
string sourceFile = "input_1129.psd";
string outputPsd = "out_psdnet1129.psd";
string outputPng = "out_psdnet1129.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

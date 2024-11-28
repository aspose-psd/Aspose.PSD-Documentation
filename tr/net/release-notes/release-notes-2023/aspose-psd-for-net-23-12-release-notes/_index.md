---
title: Aspose.PSD için .NET 23.12 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-icin-net-23-12-sürüm-notları/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içerir

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                  | **Kategori** |
|:------------ |:---------------------------------------------------------------------------------------------------------- |:------------|
| PSDNET-1679  | [AI Format] Yeni sürümde Raster Görüntü oluşturmaya destek ekleme                                              | Özellik     |
| PSDNET-1454  | GdflResrource'da Gürültü türü Gradyanı işleme                                                               | Özellik     |
| PSDNET-1827  | Metin Katmanı Güncelleme Sonrası Kaydedilirken "Nesne başvurusu bir nesnenin örneğine ayarlanmadı" hatası   | Hata        |
| PSDNET-1776  | MacOS'ta yazı tiplerinin manuel yükleme sorununu System.Drawing.Common ve Aspose.Drawing ile düzeltme       | Hata        |
| PSDNET-1536  | PsdLoadOptions'da AllowWarpRepaint, istisnaya neden olur                                                      | Hata        |
| PSDNET-1714  | [AI Format] Çapraz referans akışlarının işlenmesini uygulama                                                  | Geliştirme  |
| PSDNET-1834  | VectorPathDataResource için Lisans Kontrolü yanlış çalışıyor                                                | Geliştirme  |
| PSDNET-770   | PSD görüntüsünde gömülü akıllı nesne olarak herhangi bir görüntü dosyasını açın                             | Geliştirme  |
| PSDNET-1864  | Aspose.PSD Eklenti Lisans Sistemi                                                                          | Geliştirme  |



## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **Kaldırılan API'ler:**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Kullanım örnekleri:**

**PSDNET-1679. [AI Format] Yeni sürümde Raster Görüntü oluşturmaya destek ekleme**

{{< highlight csharp >}}
            string kaynakDosya = Path.Combine(baseFolder, "raster.ai");
            string çıktıDosyası = Path.Combine(outputFolder, "raster_output.png");

            using (AiImage görüntü = (AiImage)Image.Load(kaynakDosya))
            {
                görüntü.Save(çıktıDosyası, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. GdflResrource'da Gürültü türü Gradyanı işleme**

{{< highlight csharp >}}
            string kaynakDosya = "Gradient-Fill.psd";
            string hedefDosya = "Gradient-Fill-out.psd";

            using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions()))
            {
                Katman katman = görüntü.Layers[1];

                foreach (LayerResource kaynak in katman.Resources)
                {
                    GdFlResource gdFlKaynak = kaynak as GdFlResource;

                    if (gdFlKaynak != null)
                    {
                        gdFlKaynak.Scale = 90;
                        gdFlKaynak.Angle = 30;
                        gdFlKaynak.Dither = false;
                        gdFlKaynak.AlignWithLayer = true;
                        gdFlKaynak.Reverse = false;

                        break;
                    }
                }

                görüntü.Save(hedefDosya, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-1827. Metin Katmanı Güncelleme Sonrası Kaydedilirken "Nesne başvurusu bir nesnenin örneğine ayarlanmadı" hatası**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "input_1827.psd");
string çıktıDosyası = Path.Combine(outputFolder, "out_1827.psd");

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosya))
{
    foreach (var katman in psdGörüntü.Layers)
    {
        if (katman is TextLayer metinKatmanı)
        {
            metinKatmanı.TextData.UpdateLayerData();
        }
    }

    // Burada hata olmamalı
    psdGörüntü.Save(çıktıDosyası);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint, PsdLoadOptions'da istisnaya neden olur**

{{< highlight csharp >}}
            string kaynakDosya = @"SizeChart-4 Colors.psd";
            string çıktıDosyası = @"SizeChart-4 Colors.png";

            using (var psdGörüntü = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true })) 
			{ 
				psdGörüntü.Save(çıktıDosyası + "_original.png", new PngOptions()
				{
					ColorType = PngColorType.TruecolorWithAlpha,
					Progressive = true,
					CompressionLevel = 9
				});
			}
{{< /highlight >}}

**PSDNET-1834. VectorPathDataResource için Lisans Kontrolü yanlış çalışıyor**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. PSD görüntüsünde gömülü akıllı nesne olarak herhangi bir görüntü dosyasını açın**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "empty.psd");

string ağaçDosyasıEkle = Path.Combine(baseFolder, "tree.psd");
string donDosyasıEkle = Path.Combine(baseFolder, "frost.png");

string çıktıAğaçDosyası = Path.Combine(outputFolder, "tree_export.psd");
string çıktıDonDosyası = Path.Combine(outputFolder, "frost_export.psd");

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream akım = new FileStream(ağaçDosyasıEkle, FileMode.Open))
    {
        using (SmartObjectLayer akıllıKatman = new SmartObjectLayer(akım))
        {
            psdGörüntü.AddLayer(akıllıKatman);

            psdGörüntü.Save(çıktıAğaçDosyası, new PsdOptions());                        
        }
    }
}

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream akım = new FileStream(donDosyasıEkle, FileMode.Open))
    {
        using (SmartObjectLayer akıllıKatman = new SmartObjectLayer(akım))
        {
            psdGörüntü.AddLayer(akıllıKatman);

            psdGörüntü.Save(çıktıDonDosyası, new PsdOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1864. Aspose.PSD Eklenti Lisans Sistemi**

{{< highlight csharp >}}            
    var metered = new Metered();
    metered.SetMeteredKey(pluginPublic, pluginPrivate);
			
	// Eklentiye özgü manipülasyon
{{< /highlight >}}
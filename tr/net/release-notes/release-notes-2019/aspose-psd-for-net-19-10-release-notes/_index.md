---
title: Aspose.PSD for .NET 19.10 - Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, Aspose.PSD for .NET 19.10 için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-207|[Renk Denge Ayarlama Katmanı Desteği](/psd/tr/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Özellik|
|PSDNET-145|[Ters Çevirme Ayarlama Katmanı Desteği](/psd/tr/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Özellik|
|PSDNET-139|[Bikübik Yeniden Örnekleyiciyi Uygula](/psd/tr/net/modifying-images/#modifyingimages-implementbicubicresampling)|Özellik|
|PSDNET-169|[Kırpma Maskesi ile PSD'nin PDF'ye Dönüştürülmesi Desteği Ekle](/psd/tr/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Özellik|
|PSDNET-168|[Ayar Katmanlarıyla PSD'nin PDF'ye Dönüştürülmesi Desteği Ekle](/psd/tr/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Özellik|
|PSDNET-179|Katman DropShadowEffect'i Alındığında Sorun|Geliştirme|
|PSDNET-203|Metin / karakterleriyle güncellendiğinde dosya Photoshop'ta açılamaz|Hata|
|PSDNET-199|PSD dosyası, metin katmanı sadece satır kesme içerdiğinde kaydedilemez|Hata|
|PSDNET-185|Yanlış Font boyutu çıkarıldı|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**
**PSDNET-207. Renk Denge Ayarlama Katmanı Desteği**

{{< highlight java >}}

            var dosyaYolu = "ColorBalance.psd";

            var çıkışYolu = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(dosyaYolu))

            {

                foreach (var katman in im.Layers)

                {

                    var cbKatman = katman as ColorBalanceAdjustmentLayer;

                    if (cbKatman != null)

                    {

                        cbKatman.ShadowsCyanRedBalance = 30;

                        cbKatman.ShadowsMagentaGreenBalance = -15;

                        cbKatman.ShadowsYellowBlueBalance = 40;

                        cbKatman.MidtonesCyanRedBalance = -90;

                        cbKatman.MidtonesMagentaGreenBalance = -25;

                        cbKatman.MidtonesYellowBlueBalance = 20;

                        cbKatman.HighlightsCyanRedBalance = -30;

                        cbKatman.HighlightsMagentaGreenBalance = 67;

                        cbKatman.HighlightsYellowBlueBalance = -95;

                        cbKatman.PreserveLuminosity = true;

                    }

                }

                im.Save(çıkışYolu);

            }

{{< /highlight >}}

**PSDNET-145. Ters Çevirme Ayarlama Katmanı Desteği**

{{< highlight java >}}

            var dosyaYolu = "InvertStripes_before.psd";

            var çıkışYolu = "InvertStripes_after.psd";

            using (var im = (PsdImage)Image.Load(dosyaYolu))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(çıkışYolu);

            }

{{< /highlight >}}

**PSDNET-139. Bikübik Yeniden Örnekleyiciyi Uygula**

{{< highlight java >}}

             string kaynakDosya = "örnek.psd";

            string hedefAdı = "BikübikKabarcıklarSonrası.psd";

            // Mevcut bir görüntüyü PsdImage sınıfının bir örneğine yükle

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))

            {

                görüntü.Resize(300, 300, ResizeType.CubicConvolution);

                görüntü.Save(hedefAdı, new PsdOptions(görüntü));

            }

            string kaynakDosya = "örnek.psd";

            string hedefAdı = "BikübikKediGözleriSonrası.psd";

            // Mevcut bir görüntüyü PsdImage sınıfının bir örneğine yükle

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))

            {

                görüntü.Resize(300, 300, ResizeType.CatmullRom);

                görüntü.Save(hedefAdı, new PsdOptions(görüntü));

            }

{{< /highlight >}}

...
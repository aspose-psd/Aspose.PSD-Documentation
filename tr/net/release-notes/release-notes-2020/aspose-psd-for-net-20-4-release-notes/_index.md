---
title: Aspose.PSD for .NET 20.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-psd-for-net-20-4-sürüm-notları/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-567|'Vektör Oluşum Verileri' kaynağının desteklenmesi|Özellik|
|PSDNET-373|lclrResource (Tablo rengi ayarı) desteği|Özellik|
|PSDNET-563|LengthRecord verilerinden özelliklerin desteklenmesi. (Yol işlemleri (boolean işlemler), katman içinde şeklin dizini, bézier düğüm kayıtlarının sayısı)|Özellik|
|PSDNET-425|Görüntü Bölüm Kaynağı #1010 Arka plan renginin desteklenmesi|Özellik|
|PSDNET-530|Çalışma zamanında Dolgu Katmanlarının eklenmesi|Özellik|
|PSDNET-424|Görüntü Bölüm Kaynağı #1009 Kenar bilgisinin desteklenmesi|Özellik|
|PSDNET-592|AI Format Dosyalarında Katmanların Desteklenmesi|Özellik|
|PSDNET-256|Gradyan Örtüsü Katman Efektinin Okunması ve Düzenlenmesinin Desteklenmesi|Özellik|
|PSDNET-257|Gradyan Örtüsü Katman Efektinin Rendelenmesi|Özellik|
|PSDNET-585|GradientOverlayEffect.BlendMode özelliği değişikliklerinin Photoshop'ta gösterilmemesi|Hata|
|PSDNET-561|Grayscale ColorMode ve 16 bit kanal başına 16 bit ile PSD görüntüsünün grayscale PSD formatına kaydedilmesinin düzeltilmesi|Hata|
|PSDNET-560|Grayscale ColorMode ve 16 bit kanal başına 16 bit ile PSD görüntüsünün PNG formatına kaydedilmesinin düzeltilmesi|Hata|

## **Genel API Değişiklikleri**
# **Yeni Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **Kaldırılan API'lar:**
- Hiçbiri

## **Kullanım Örnekleri:**
**PSDNET-567. 'Vektör Oluşum Verileri' kaynağının desteklenmesi**

{{< highlight java >}}

         // VogkResource Desteği

        static void VogkResourceDesteğiÖrneği()

        {

            string dosyaAdı = "VectorOriginationDataResource.psd";

            string cikisDosyaAdı = "out_VectorOriginationDataResource_.psd";

            using (var psdGörüntü = (PsdImage)Image.Load(dosyaAdı))

            {

                var kaynak = GetVogkResource(psdGörüntü);

                // Okuma

                if (kaynak.ShapeOriginSettings.Length != 1 ||

                    !kaynak.ShapeOriginSettings[0].IsShapeInvalidated ||

                    kaynak.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource hatalı okundu.");

                }

                // Düzenleme

                kaynak.ShapeOriginSettings = new[]

                {

                    kaynak.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                psdGörüntü.Save(cikisDosyaAdı);

            }

        }

        static VogkResource GetVogkResource(PsdImage görüntü)

        {

            var katman = görüntü.Layers[1];

            VogkResource kaynak = null;

            var kaynaklar = katman.Resources;

            for (int i = 0; i < kaynaklar.Length; i++)

            {

                if (kaynaklar[i] is VogkResource)

                {

                    kaynak = (VogkResource)kaynaklar[i];

                    break;

                }

            }

            if (kaynak == null)

            {

                throw new Exception("VogkResource bulunamadı.");

            }

            return kaynak;

        }   

{{< /highlight >}}
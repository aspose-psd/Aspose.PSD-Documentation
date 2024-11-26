---
title: Aspose.PSD için .NET 20.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-673|LnkE Kaynağının Desteklenmesi|Özellik|
|PSDNET-392|britResource'un Desteklenmesi (Parlaklık/Kontrast Ayarlama Katmanı Kaynağı)|Özellik|
|PSDNET-629|Desteklenmeyen formatlar olarak açılmaya çalışıldığında görüntü olarak hata mesajının değiştirilmesi|Geliştirme|
|PSDNET-594|Katlama Maskesinin Kaydedilememesi|Hata|
|PSDNET-597|Yeni Katman Grubu oluşturulduktan sonra PSD dosyasının kaydedilmeye çalışılması durumunda Photoshop uyarısı alınması|Hata|
|PSDNET-618|Klasöre uygulanmayan Kırpma maskesi|Hata|
|PSDNET-625|Aspose.PSD for .NET ile dosyanın açılamaması|Hata|
|PSDNET-650|PSD'nin PDF'ye dönüştürülmesi sırasında resmin kaydedilememesi istisnası|Hata|
|PSDNET-655|Kesme işlemi PSD görüntüsündeki Kırpma yolu geçersiz yapar|Hata|
|PSDNET-662|Gölge Etkisine sahip Belirli bir PSD dosyasının kaydedilmeye çalışılmasıyla NullReference İstisnası|Hata|
|PSDNET-666|Image.CanLoad(pdfStream) için Aspose.PSD'nin true dönmesi|Hata|
|PSDNET-676|Oluşturulan PNG'de katmanların render edilmemesi|Hata|
|PSDNET-677|TextData'ya erişimde istisna|Hata|
|PSDNET-679|PSD'nin kaydedilmesi sırasında ImageSaveException hatası|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Kaldırılan API'ler:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Kullanım örnekleri:**
**PSDNET-606. LnkE Kaynağının Desteklenmesi**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("Gerçek değer {0} beklenen {1} ile eşleşmiyor.", actual, expected));
     }
 
 // Kodların devamı...
{{< /highlight >}}

**PSDNET-201. Belge dönüşüm ilerleme desteği**

{{< highlight csharp >}}
// C# kodları...
{{< /highlight >}}

**PSDNET-386. britResource (Parlaklık/Kontrast Ayarlama Katmanı Kaynağı) Desteği**

{{< highlight csharp >}}
 /* Bu Örnek, PSD Resminin Parlaklık/Kontrast Katman Kaynağı - BritResource'u programlı olarak nasıl değiştirebileceğinizi göstermektedir.

   Bu, Düşük Seviye Aspose.PSD API'dir. Parlaklık/Kontrast Katmanını, PSD dosyası içeriği üzerinde daha fazla kontrol sağlayan API'ı kullanabilirsiniz, 

   ancak doğrudan Photoshop kaynağı düzenleme, PSD dosya içeriği üzerinde daha fazla kontrol sağlar.  */
{{< /highlight >}}

**PSDNET-596. Passthrough (Geçiş) Karıştırma Modlu Katman Grubu Render Edilmez**

{{< highlight csharp >}}
 // C# kodları...
{{< /highlight >}}

**PSDNET-610. Belirli bir Psd dosyasını resme dönüştürmeye çalışırken NullReference İstisnası**

{{< highlight csharp >}}
 // C# kodları...
{{< /highlight >}}

**PSDNET-636. Maske sınırları boş olan ayar katmanıyla PSD dosyalarının yanlış yeniden boyutlandırılması**

{{< highlight csharp >}}
// C# kodları...
{{< /highlight >}}

**PSDNET-652. Geçerli LnkE Kaynağı ve adobeStockLicenseState özelliğine sahip belirli PSD dosyasını yüklerken OverflowException**

{{< highlight csharp >}}
// C# kodları...
{{< /highlight >}}

**PSDNET-638. Boş Katman Grubuna katman grubu eklendikten sonra Yanlış Katman Sırası**

{{< highlight csharp >}}
 // C# kodları...
{{< /highlight >}} 

**PSDBET-219. DefaultReplacementFont ayarını ImageOptionsBase sınıfına taşıma**

{{< highlight csharp >}}
 // C# kodları...
{{< /highlight >}}
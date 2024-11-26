---
title: Aspose.PSD için .NET 20.12 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-for-net-20-12-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD için .NET 20.12](https://www.nuget.org/packages/Aspose.PSD/) sürümü için yayın notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-757|Katmanları Akıllı Nesne Katmanına dönüştürmeyi destekleme|Özellik|
|PSDNET-764|SmartObjectLayer.ReplaceContents yöntemi PSB dosyası eklemeye çalışırsak NullReferenceException fırlatıyor|Hata|
|PSDNET-773|CMYK 8-bit ve CMYK 16-bit Görüntülerin yanlış renderlanması, katman Tuvalden büyükse|Hata|
|PSDNET-782|Kaydedilen PSB dosyası API'mizle açılabilir, ancak Photoshop'ta açılamaz|Hata|
|PSDNET-783|Belirli bir PSD'de Paylaşılan veri kaynağıyla Akıllı Katmanı değiştirmeye çalışırsak bir istisna alırız|Hata|
|PSDNET-172|Kafa karışıklığını önlemek için FileFormatVersion'ın adı PsdVersion'a değiştirildi|Geliştirme|
|PSDNET-620|Aspose.PSD .NET'ten Compact framework yapılandırmasını kaldırma|Geliştirme|
|PSDNET-765|PsB dosyasını SmartObjectLayers ile açmaya çalışırken PsdImageException: Bilinmeyen kaynak başlığı|Geliştirme|
|PSDNET-798|Aspose.PSD ve Aspose.Imaging Ürünlerinin tutarlılığını sağlamak için Vektör Maskesi Sınıflarının Hiyerarşisini Çekirdek Ad alanına taşıma|Geliştirme|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.PsdVersion
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.PsdVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.PsdVersion
- T:Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord
- ...

## **Kullanım Örnekleri:**
**PSDNET-757. Katmanları Akıllı Nesne Katmanına dönüştürmeyi destekleme**
{{< highlight csharp >}}
      string dataDir = "PSDNET757_1\\";
      string outputDir = dataDir + "output\\";
      
      // Bu örnekler, PSD dosyasındaki katmanları akıllı nesne katmanına dönüştürmenin nasıl yapıldığını göstermektedir
      ExampleOfConvertingToSmartObjectLayer("ThreeRegularLayers", 0, 1);
      ...
{{< /highlight >}}

**PSDNET-764. SmartObjectLayer.ReplaceContents yöntemi PSB dosyası eklemeye çalışırsak NullReferenceException fırlatıyor**
{{< highlight csharp >}}
      // Bu örnek, ReplaceContents yönteminin belirtilen PSD dosyasıyla doğru şekilde çalıştığını gösterir.
      const string baseFolder = "PSDNET764_1\\";
      const string outputFolder = baseFolder + "output\\";
      ...
{{< /highlight >}}
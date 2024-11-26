---
title: Aspose.PSD için Java 23.6 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-icin-java-23-6-sürüm-notları/
---

{{% alert color="primary" %}} Bu sayfa [Aspose.PSD için Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) sürümüne ait sürüm notlarını içerir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                                                       | **Kategori** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | TimeLine API'si Refactor Edildi                                                                                                                  | Geliştirme   |
| PSDJAVA-480 | Warp render ederken artefaktları kaldırma                                                                                                       | Geliştirme   |
| PSDJAVA-481 | Warp render optimizasyonu                                                                                                                       | Geliştirme   |
| PSDJAVA-482 | Eşik Ayarlama Katmanı Desteği                                                                                                                   | Özellik      |
| PSDJAVA-483 | Seçici Renk Ayarlama Katmanı Desteği                                                                                                            | Özellik      |
| PSDJAVA-484 | PSD TimeLine'ın Animasyonlu Gif dosyasına aktarım yeteneği                                                                                       | Özellik      |
| PSDJAVA-485 | Kare dışı sınırları olmayan Metin Katmanı desteği                                                                                                | Özellik      |
| PSDJAVA-486 | Şekil Katmanı Desteği                                                                                                                           | Özellik      |
| PSDJAVA-487 | Akıllı nesnede görüntü değiştiğinde güncellenmiyor                                                                                               | Hata         |
| PSDJAVA-488 | PSD dosyası, aşağıdaki istisna ile PSD olarak kaydedilemiyor: Rgb ve Lab modları, 3 kanaldan az ve 4 kanaldan fazla içerebilir                        | Hata         |
| PSDJAVA-489 | Photoshop'un düzenleme modunu kullanarak Metin Katmanı açıldığında Metin Hizalaması kayboluyor                                                | Hata         |
| PSDJAVA-490 | PSD dosyasını kaydederken Null referans istisnası                                                                                                | Hata         |
| PSDJAVA-491 | Şekil Katmanı yüklenirken istisna oluştu: Vektör köken sınırlar için puanlar henüz desteklenmiyor                                            | Hata         |
| PSDJAVA-492 | VogkResource yüklenirken istisna oluştu: Noktalar DoubleStructures olarak kaydedildi, biz UnitStructures olarak okuyoruz                      | Hata         |
| PSDJAVA-493 | Şekil Katmanı'nın KatmanTürü boş                                                                                        | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- ...

# **Kaldırılan API'lar:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- ...

## **Kullanım Örnekleri:**

**PSDJAVA-482. Eşik Ayarlama Katmanı Desteği**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-483. Seçici Renk Ayarlama Katmanı Desteği**

{{< highlight java >}}
...
{{< /highlight >}}

......  

**PSDJAVA-484. PSD TimeLine'ın Animasyonlu Gif dosyasına aktarım yeteneği**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-487. Akıllı nesnede görüntü değiştiğinde güncellenmiyor**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-479. TimeLine API'si Refactor Edildi**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-488. PSD dosyası, aşağıdaki istisna ile PSD olarak kaydedilemiyor: Rgb ve Lab modları, 3 kanaldan az ve 4 kanaldan fazla içerebilir**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-480. Warp render ederken artefaktları kaldırma**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-481. Warp render optimizasyonu**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-489. Photoshop'un düzenleme modunu kullanarak Metin Katmanı açıldığında Metin Hizalaması kayboluyor**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-485. Kare dışı sınırları olmayan Metin Katmanı desteği**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-491. Şekil Katmanı yüklenirken istisna oluştu: Vektör köken sınırlar için puanlar henüz desteklenmiyor**

**PSDJAVA-492. VogkResource yüklenirken istisna oluştu: Noktalar DoubleStructures olarak kaydedildi, biz UnitStructures olarak okuyoruz**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-493. Şekil Katmanı'nın KatmanTürü boş**

{{< highlight java >}}
...
{{< /highlight >}}

**PSDJAVA-486. Şekil Katmanı Desteği**

{{< highlight java >}}
...
{{< /highlight >}}
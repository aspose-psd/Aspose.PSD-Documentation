---
title: PSD İyileştirmeleri için Ayar Katmanı Kullanımı
weight: 100
type: docs
description: Aspose.PSD için Java kullanarak ayar katmanı kullanımı örnekleri
keywords: [ayar katmanı, fotoğraf iyileştirme, eğriler ayarı, seviyeler iyileştirmesi, ters çevirme, fotoğraf filtresi, psd api, java, kod örneği]
url: tr/java/ayar-katmanı-iyileştirme/
---

## **Genel Bakış**

Bu makale, Aspose.PSD için Java'da ayar katmanlarının düzenlenmesini keşfeder. Ayar katmanları, resim düzenleme alanında güçlü bir özelliktir ve görüntülerinizde yıkıcı olmayan değişiklikler yapmanıza olanak tanır. Aspose.PSD, görüntülerinizin çeşitli yönlerini değiştirmek için kullanabileceğiniz kapsamlı bir ayar katmanı sınıfı seti sağlar.

Ayar katmanlarının düzenlenmesini göstermek için, sayfanın sonunda bir PSD görüntüsünü yükleyen ve katmanlarına farklı ayarlamalar uygulayan bir örnek kod parçacığı sunacağız.

Aşağıdaki kod parçacığında, PSD görüntüsünü PsdImage.load() yöntemini kullanarak yükleme işlemiyle başlarız. Ardından, çıktı PNG dosyalarını kaydetme seçeneklerini kurarız. PngOptions sınıfı, çıktı görüntü için renk türünü belirlememizi sağlar.

Daha sonra, PSD görüntüsündeki her katmanın üzerinden geçer ve tipini isAssignable() yöntemini kullanarak kontrol ederiz. Katman belirli bir türde ise, cast() yöntemini kullanarak onu bu türe dönüştürür ve istenen ayarı uygularız. Örneğin, BrightnessContrastLayer'ın parlaklık ve kontrastını ayarlarız, LevelsLayer'ın seviyelerini değiştiririz, CurvesLayer'a bir eğri noktası ekleriz ve benzer işlemleri yaparız.

Diğer ayarlamaları uygulamak için ilgili katmanlara ek kod ekleyebilirsiniz. Aspose.PSD, [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) gibi geniş bir ayar katmanı sınıfı yelpazesi sunar.

Son olarak, değiştirilmiş görüntüyü PsdImage sınıfının save() yöntemi ile kaydederiz.

Bu, Aspose.PSD için Java'da ayar katmanlarını düzenlemenin temel bir genel bakışını sağlar. Ayarlamaları gereksinimlerinize göre özelleştirebilir ve API belgelerinde mevcut olan çeşitli seçenekleri keşfedebilirsiniz.

Lütfen aşağıdaki tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}

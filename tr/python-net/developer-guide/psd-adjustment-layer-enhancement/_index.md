---
title: Python Kullanarak PSD Geliştirmeleri İçin Düzenleme Katmanı Kullanımı
weight: 100
type: docs
description: Aspose.PSD aracılığıyla ayarlama katmanının Python üzerinden örnekleri
keywords: [ayar katmanı, fotoğraf iyileştirme, eğri ayarı, seviyelerin iyileştirilmesi, tersine çevirme, fotoğraf filtresi, psd api, python, kod örneği]
url: tr/python-net/adjustment-layer-enhancement/
---

## **Genel Bakış**

Bu makalede, Aspose.PSD'nin Python için ayarlama katmanlarının düzenlenmesini keşfedeceğiz. Ayarlama katmanları, görüntü düzenleme alanında güçlü bir özelliktir ve görüntülerinize yıkıcı olmayan değişiklikler yapmanıza olanak tanır. Aspose.PSD, görüntülerinizin çeşitli yönlerini değiştirebileceğiniz kapsamlı bir ayarlama katmanı sınıfı seti sunar.

Ayarlama katmanlarının düzenlenmesini göstermek için, sayfanın sonunda bir PSD görüntüsünü yükleyen ve katmanlarına farklı ayarlamalar uygulayan örnek bir kod parçası kullanacağız.

Aşağıdaki kod parçasında, PSD görüntüsünü PsdImage.load() metodu kullanarak yüklemeye başlıyoruz. Ardından, çıktı PNG dosyaları için seçenekleri ayarlıyoruz. PngOptions sınıfı, çıktı görüntü için renk tipini belirtmemize olanak tanır.

Daha sonra, PSD görüntüsündeki her katmana döngüyle giriyor ve tipini is_assignable() metodu kullanarak kontrol ediyoruz. Katman belirli bir türdeyse, onu belirtilen türe dönüştürmek ve istenen ayarı uygulamak için cast() metodunu kullanıyoruz. Örneğin, BrightnessContrastLayer'ın parlaklık ve kontrastını ayarlıyor, LevelsLayer'ın seviyelerini değiştiriyor, CurvesLayer'a eğri noktası ekliyoruz ve benzeri işlemler yapıyoruz.

Diğer ayarlamaları uygulamak için ilgili katmanlarına ek kod ekleyebilirsiniz. Aspose.PSD, [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) ve daha fazlası gibi geniş bir ayarlama katmanı sınıfı yelpazesi sunar.

Son olarak, PsdImage sınıfının save() metoduyla değiştirilmiş görüntüyü kaydediyoruz.

Bu kod, Aspose.PSD'nin Python için ayarlama katmanlarını düzenleme hakkında temel bir genel bakış sağlar. Ayarlamaları gereksinimlerinize göre özelleştirebilir ve API belgelerindeki çeşitli seçenekleri keşfedebilirsiniz.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-ayer-enhancement.py" >}}

---
title: Kullandığı Ayar Katmanını PSD Geliştirmeleri İçin
weight: 100
type: docs
description: Aspose.PSD'nin C# aracılığıyla ayar katmanlarını kullanma örnekleri
keywords: [ayar katmanı, fotoğrafı geliştirme, eğri ayarı, seviyelerin iyileştirilmesi, tersine çevirme, fotoğraf filtresi, psd api, C#, csharp, kod örneği]
url: tr/net/ayar-katmani-gelistirme/
---

## Genel Bakış

Bu makalede, Aspose.PSD'nin C# kullanarak ayar katmanlarını düzenleme işlemini keşfedeceğiz. Ayar katmanları, görüntü düzenlemede güçlü bir özelliktir ve görüntülerinize yıkıcı olmayan değişiklikler yapmanıza olanak tanır. Aspose.PSD, görüntülerinizin çeşitli yönlerini değiştirmek için kullanabileceğiniz kapsamlı bir ayar katmanı sınıf seti sağlar.

Ayar katmanlarını düzenlemenin gösterilmesi için, bu sayfanın sonunda bir PSD görüntüsünü yükleyen ve katmanlarına farklı ayarlamalar uygulayan bir örnek kod parçacığını kullanacağız.

Aşağıdaki kod parçacığında, PSD görüntüsünü `PsdImage.Load()` yöntemini kullanarak yükleme işlemine başlıyoruz. Daha sonra, çıkış PNG dosyaları için kaydetme seçeneklerini kurarız. `PngOptions` sınıfı, çıkış görüntü için renk türünü belirtmemize olanak tanır.

Daha sonra, PSD görüntüsündeki her katmana döngü yaparız ve `IsAssignable()` yöntemini kullanarak tipini kontrol ederiz. Katman belirli bir türdeyse, `Cast()` yöntemini kullanarak o türü dönüştürür ve istenen ayarı uygularız. Örneğin, bir `BrightnessContrastLayer`'ın parlaklığını ve kontrastını ayarlarız, bir `LevelsLayer`'ın seviyelerini değiştiririz, bir `CurvesLayer`'a eğri noktası ekleriz ve benzeri.

Diğer ayarları ilgili katmanlara uygulamak için ek kod ekleyebilirsiniz. Aspose.PSD, [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) gibi geniş bir ayar katmanı sınıf yelpazesi sağlar.

Son olarak, `PsdImage` sınıfının `Save()` yöntemini kullanarak değiştirilmiş görüntüyü kaydederiz.

Bu kod, Aspose.PSD'nin C# için ayar katmanlarını düzenleme hakkında temel bir genel bakış sağlar. Ayarlamaları ihtiyaçlarınıza göre özelleştirebilir ve API belgesinde mevcut olan çeşitli seçenekleri keşfedebilirsiniz.

## Örnek

İşte Aspose.PSD'nin C# için ayar katmanlarını nasıl kullanacağını gösteren bir kod örneği:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Daha ayrıntılı bilgi ve örnekler için lütfen [Aspose.PSD for C# belgelerini](https://docs.aspose.com/psd/net/) ziyaret edin.


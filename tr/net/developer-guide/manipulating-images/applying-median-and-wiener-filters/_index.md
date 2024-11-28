---
title: Orta ve Wiener Filtrelerinin Uygulanması
type: docs
weight: 10
url: /tr/net/orta-ve-wiener-filtrelerinin-uygulanmasi/
---

## **Orta ve Wiener Filtrelerinin Uygulanması**
Orta filtre, genellikle gürültüyü kaldırmak için kullanılan bir doğrusal olmayan dijital filtreleme tekniğidir. Bu tür gürültü azaltma, daha sonraki işlemlerin sonuçlarını iyileştirmek için tipik bir ön işleme adımıdır. Wiener filtresi, aditif gürültü ve bulanıklaşma tarafından bozulmuş görüntüler için MSE (ortalama kare hatası) optimal sabit doğrusal filtre olarak kabul edilir. Aspose.PSD API geliştiricileri, bir orta filtre uygulayabilir ve gauss wiener filtresini görüntülere uygulayabilir. Bu makale, orta filtresi ve gauss wiener filtresinin nasıl uygulanacağını göstermektedir.
### **Orta Filtresi Uygulanması**
Aspose.PSD, [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) sınıfını [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) üzerine bir filtre uygulamak için sağlar. Aşağıda verilen kod parçacığı, bir raster görüntüye orta filtrenin nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Gauss Wiener Filtresinin Uygulanması**
Aspose.PSD, [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) sınıfını [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) üzerine bir filtre uygulamak için sağlar. Aşağıda verilen kod parçacığı, bir raster görüntüye gauss wiener filtresinin nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Renkli Görüntüye Gauss Wiener Filtresinin Uygulanması**
Aspose.PSD, renkli görüntüler için [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)sağlar. Aşağıda verilen kod parçacığı, bir renkli görüntüye gauss wiener filtresinin nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Hareketli Wiener Filtresinin Uygulanması**
Aspose.PSD, [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) sınıfını [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) üzerine bir filtre uygulamak için sağlar. Aşağıda verilen kod parçacığı, bir raster görüntüye hareketli wiener filtresinin nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Bir Görüntü Üzerinde Düzeltme Filtresi Uygulama**
Bu makale, bir görüntü üzerinde düzeltme filtrelerini uygulamak için Aspose.PSD for .NET'in kullanımını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için verimli ve kolay kullanımlı yöntemler sunmaktadır. Aspose.PSD for .NET, filtreleme için [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)ve [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) sınıflarını açığa çıkarmıştır. BilateralSmoothingFilterOptions sınıfı bir boyut olarak bir tamsayıya ihtiyaç duyar. Yeniden boyutlandırma işlemlerini gerçekleştirmek için adımlar aşağıdaki gibidir:

1. Görüntüyü Image sınıfının sağladığı Load fabrika yöntemi ile yükle.
1. Görüntüyü RasterImage'a dönüştür.
1. Bir BilateralSmoothingFilterOptions ve SharpenFilterOptions sınıfı örneği oluştur.
1. [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) yöntemini çağırırken dikdörtgeni görüntü sınırları olarak ve BilateralSmoothingFilterOptions sınıfı örneğini belirlerken.
1. [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) yöntemini çağırırken dikdörtgeni görüntü sınırları olarak ve SharpenFilterOptions sınıfı örneğini belirlerken.
1. Kontrastı ayarla
1. Parlaklığı ayarla
1. Sonuçları kaydet.


## **Bradley eşikleme algoritmasını kullanma**
Görüntü eşikleme, grafik uygulamalarda kullanılmaktadır. Bir görüntünün eşiklenmesinin amacı, pikselleri "koyu" veya "açık" olarak sınıflandırmaktır. Aspose.PSD API, görüntüleri dönüştürürken Bradley eşikleme kullanmanıza olanak tanır. Aşağıdaki kod parçacığı, eşik değerini tanımlamanın ve ardından Bradley'nin eşikleme algoritmasını çağırmanın nasıl yapıldığını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}

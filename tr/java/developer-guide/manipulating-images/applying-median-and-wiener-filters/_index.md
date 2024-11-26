---
title: Median ve Wiener Filtrelerinin Uygulanması
type: docs
weight: 10
url: /tr/java/median-ve-wiener-filtrelerinin-uygulanmasi/
---

## **Median ve Wiener Filtrelerinin Uygulanması**
Ortalama filtre, genellikle gürültüyü kaldırmak için kullanılan bir doğrusal olmayan dijital filtreleme tekniğidir. Bu tür gürültü azaltma, sonraki işlemlerin sonuçlarını iyileştirmek için tipik bir ön işleme adımıdır. Wiener filtresi, ek gürültü ve bulanıklık ile bozulmuş görüntüler için MSE (ortalama karesel hata) en uygun sabit doğrusal filtre konumundadır. Aspose.PSD for Java API geliştiricileri, görüntüdeki gürültüyü azaltmak için ortalama filtreyi uygulayabilir ve Gauss wiener filtreyi uygulayabilirler. Bu makale, ortalama filtre ve Gauss wiener filtresinin nasıl uygulanabileceğini göstermektedir.
### **Median Filtresi Uygulanması**
Aspose.PSD, filtre uygulamak için MedianFilterOptions sınıfını sağlar. Aşağıda verilen kod örneği, bir rastgele görüntüye ortalamalı filtre uygulamanın nasıl olduğunu göstermektedir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Gauss Wiener Filtresi Uygulaması**
Aspose.PSD, bir RasterImage üzerinde filtre uygulamak için GaussWienerFilterOptions sınıfını sağlar. Aşağıda verilen kod örneği, bir rastgele görüntüye Gauss wiener filtresi nasıl uygulanırı göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Renkli Görüntüye Gauss Wiener Filtresi Uygulanması**
Aspose.PSD, renkli görüntüler için GaussWienerFilterOptions sağlar. Aşağıda verilen kod örneği, bir renkli görüntüye Gauss wiener filtresi nasıl uygulanırı göstermektedir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Hareket Wiener Filtresi Uygulanması**
Aspose.PSD, bir RasterImage üzerinde filtre uygulamak için MotionWienerFilterOptions sınıfını sağlar. Aşağıda verilen kod örneği, bir rastgele görüntüye hareket wiener filtresi nasıl uygulanırı göstermektedir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Bir Görüntüde Düzeltme Filtresi Uygulama**
Bu makale, bir görüntü üzerinde düzeltme filtrelerini uygulamak için Aspose.PSD for Java kullanımını göstermektedir. Aspose.PSD API'leri, bu amaca ulaşmak için etkili ve kullanımı kolay yöntemler sunmaktadır. Aspose.PSD for Java, filtreleme için BilateralSmoothingFilterOptions ve SharpenFilterOptions sınıflarını sunmuştur. BilateralSmoothingFilterOptions sınıfı, bir tamsayıya ihtiyaç duyar. Düzeltme işlemini gerçekleştirmek için adımlar aşağıdaki gibidir:


1. Görüntüyü Image sınıfı tarafından sunulan Load fabrika yöntemi kullanarak yükleyin.
1. Görüntüyü RasterImage'e dönüştürün.
1. BilateralSmoothingFilterOptions ve SharpenFilterOptions sınıflarının örneklerini oluşturun.
1. RasterImage.Filter yöntemini çağırırken görüntü sınırlarını ve BilateralSmoothingFilterOptions sınıfı örneğini belirtin.
1. RasterImage.Filter yöntemini çağırırken görüntü sınırlarını ve SharpenFilterOptions sınıfı örneğini belirtin.
1. Kontrastı ayarlayın.
1. Parlaklığı ayarlayın.
1. Sonuçları kaydedin.

Aşağıdaki kod parçacığı, düzeltme filtresini nasıl uygulayacağınızı gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Bradley eşikleme algoritmasını kullanma**
Görüntü eşikleme, grafik uygulamalarda kullanılır. Bir görüntünün eşiklenmesinin amacı pikselleri ya "koyu" ya da "açık" şeklinde sınıflandırmaktır. Aspose.PSD API'si, görüntüleri dönüştürürken Bradley eşikleme kullanmanıza olanak tanır. Aşağıdaki kod örneği, eşik değerini tanımlamanın ve ardından Bradley'e ait eşikleme algoritmasını nasıl çağırabileceğinizi gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}

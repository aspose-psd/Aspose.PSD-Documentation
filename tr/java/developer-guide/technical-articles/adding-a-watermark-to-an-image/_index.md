---
title: Bir Resme Filigran Ekleme
type: docs
weight: 20
url: /tr/java/bir-resme-filigran-ekleme/
---

## **Bir Resme Filigran Ekleme**
Bu belge, Aspose.PSD kullanarak bir resme filigran eklemenin nasıl yapılacağını açıklamaktadır. Bir resme filigran eklemek, resim işleme uygulamaları için yaygın bir gereksinimdir. Bu örnek, metni resim yüzeyine çizmek için Graphics sınıfını kullanmaktadır.
### **Filigran Ekleme**
İşlemi göstermek için diskten bir BMP resmi yükleyeceğiz ve Graphics sınıfının DrawString yöntemini kullanarak resim yüzeyine filigran olarak bir dize çizeceğiz. Resmi PngOptions sınıfını kullanarak PNG formatına kaydedeceğiz. Aşağıda, bir resme filigran eklemenin nasıl yapılacağını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, takip etmesini kolaylaştırmak için kısımlara ayrılmıştır. Adım adım, örnekler nasıl yapılacağını göstermektedir:

1. Bir resim yükle.
1. Bir Graphics nesnesi oluştur ve başlat.
1. Font ve SolidBrush nesnelerini oluştur ve başlat.
1. Graphics sınıfının DrawString yöntemini kullanarak bir dizeyi filigran olarak çiz.
1. Resmi PNG olarak kaydet.

Aşağıdaki kod parçacığı, resme filigran eklemenin nasıl yapılacağını göstermektedir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Diyagonal Filigran Ekleme**
Bir resme diyagonal filigran eklemek, yukarıda tartışıldığı gibi yatay bir filigran eklemeye benzerdir, ancak birkaç farklılık bulunmaktadır. İşlemi göstermek için diskten bir JPG resmi yükleyecek, Matrix sınıfı bir nesnesini kullanarak dönüşümler ekleyecek ve Graphics sınıfının DrawString yöntemini kullanarak resim yüzeyine filigran olarak bir dize çizeceğiz. Aşağıda, bir resme diyagonal filigran eklemenin nasıl yapılacağını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, takip etmesi kolay olması için kısımlara ayrılmıştır. Adım adım, örnekler nasıl yapılacağını göstermektedir:

1. Bir resim yükle.
1. Bir Graphics nesnesi oluştur ve başlat.
1. Font ve SolidBrush nesnelerini oluştur ve başlat.
1. Resmin boyutunu SizeF nesnesinde al.
1. Bir Matrix sınıfı örneği oluştur ve bileşik dönüşüm gerçekleştir.
1. Dönüşümü Graphics nesnesine atayın.
1. Bir StringFormat nesnesi oluşturun ve başlatın.
1. Graphics sınıfının DrawString yöntemini kullanarak bir dizeyi filigran olarak çiz.
1. Sonuç resmi kaydet.

Aşağıdaki kod parçacığı, bir diyagonal filigran eklemenin nasıl yapılacağını göstermektedir.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

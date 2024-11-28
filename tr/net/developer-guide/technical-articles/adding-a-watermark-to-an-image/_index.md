---
title: Bir Resme Filigran Ekleme
type: docs
weight: 30
url: /tr/net/resme-filigran-ekleme/
---

## **Bir Resme Filigran Ekleme**
Bu belge, Aspose.PSD kullanarak bir resme filigran eklemenin nasıl yapılacağını açıklar. Bir resme filigran eklemek, resim işleme uygulamaları için yaygın bir gereksinimdir. Bu örnek, bir dizeyi resim yüzeyine çizmek için Graphics sınıfını kullanan bir örnektir.
### **Filigran Ekleme**
İşlemi göstermek için diskten bir BMP resim yükleyecek ve Graphics sınıfının DrawString yöntemini kullanarak resim yüzeyine filigran olarak bir dize çizilecektir. PngOptions sınıfını kullanarak resmi PNG biçiminde kaydedeceğiz. Aşağıda, bir resme filigran eklemenin nasıl yapılacağını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, kolayca takip edilebilmesi için parçalara ayrılmıştır. Adım adım, örnekler, aşağıdakileri nasıl yapılacağını göstermektedir:

1. Bir resim [yükle](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2).
1. Bir Graphics nesnesi oluştur ve başlat.
1. Font ve [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush) nesnelerini oluştur ve başlat.
1. Graphics sınıfının [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) yöntemini kullanarak dizeyi filigran olarak çiz.
1. Resmi PNG olarak kaydet.

Aşağıdaki kod parçacığı, resme filigran ekleme işlemini göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Çapraz Bir Filigran Ekleme**
Bir resme çapraz bir filigran eklemek, yukarıda tartışılan yatay bir filigran eklemeye benzerdir, ancak birkaç farklılık vardır. İşlemi göstermek için diskin bir JPG resmini yükleyecek, Matrix sınıfından bir nesne kullanarak dönüşümler ekleyecek ve Graphics sınıfının DrawString yöntemini kullanarak resim yüzeyine bir dizeyi filigran olarak çizeceğiz. Aşağıda, bir resme çapraz bir filigran eklemenin nasıl yapılacağını gösteren bir kod örneği bulunmaktadır. Örnek kaynak kodu, kolayca takip edilebilmesi için parçalara ayrılmıştır. Adım adım, örnekler, aşağıdakileri nasıl yapılacağını göstermektedir:

1. Bir resim yükle.
1. Bir Graphics nesnesi oluştur ve başlat.
1. [Font](https://reference.aspose.com/psd/net/aspose.psd/font) ve SolidBrush nesnelerini oluştur ve başlat.
1. Resmin [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef) nesnesindeki boyutunu al.
1. Matrix sınıfından bir örnek oluştur ve bileşik dönüşüm gerçekleştir.
1. Dönüşümü Graphics nesnesine atayın.
1. [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat) nesnesi oluştur ve başlat.
1. Graphics sınıfının DrawString yöntemini kullanarak dizeyi filigran olarak çiz.
1. Sonuç resmi kaydet.

Aşağıdaki kod parçacığı, resme çapraz bir filigran eklemenin nasıl yapılacağını göstermektedir.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}

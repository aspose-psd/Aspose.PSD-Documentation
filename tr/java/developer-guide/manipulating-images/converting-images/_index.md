---
title: Resimleri Dönüştürme
type: docs
weight: 20
url: /tr/java/resimleri-donusturma/
---

## **Resimleri Siyah Beyaz ve Gri Tonlama Formuna Dönüştürme**
Bazen, basım veya arşivleme amaçları için renkli resimleri siyah beyaz veya gri tonlama formuna dönüştürmeniz gerekebilir. Bu makale, bunu başarmak için Aspose.PSD API'sının Java kullanarak kullanımını gösteren iki yöntemi aşağıda belirtilen şekilde kullanmayı göstermektedir.

- Binarizasyon
- Gri Tonlama
### **Binarizasyon**
Binarizasyon kavramını anlamak için, bir Binari Resim'i tanımlamak önemlidir; yani her piksel için yalnızca iki mümkün değeri olan dijital bir resim. Normalde, bir binari resim için kullanılan iki renk siyah ve beyazdır, ancak herhangi iki renk de kullanılabilir. Binarizasyon, her pikselin bir bit olarak saklandığı bi-seviyeli bir resme dönüştürme işlemidir (0 veya 1), burada 0 renksizliği, 1 renk varlığını ifade eder. Aspose.PSD Java API şu anda iki Binarizasyon yöntemini desteklemektedir.
#### **Sabit Eşikli Binarizasyon**
Aşağıdaki kod örneği, sabit eşikli binarizasyonun bir resme nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Otsu Eşikli Binarizasyon**
Aşağıdaki kod örneği, Otsu eşikli binarizasyonun bir resme nasıl uygulanacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Gri Tonlama**
Gri Tonlama, sürekli tonlu bir resmi kesintisiz gri tonlar içeren bir resme dönüştürme işlemidir. Aşağıdaki kod örneği, Gri Tonlama'nın nasıl kullanılacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **GIF Resim Katmanlarını TIFF Resme Dönüştürme**
Bazen, bir PSD Resmin katmanlarını başka bir raster resim formatına dönüştürmek uygulama gereksinimini karşılamak için gereklidir. Aspose.PSD API, bir PSD Resminin katmanlarını başka bir raster resim formatına dönüştürme özelliğini destekler. İlk olarak, resmin bir örneğini oluşturacak ve yerel diskin PSD resmini yükleyeceğiz, ardından Her bir katmanda yinelenen bir işlem yapacağız. Daha sonra bloğu TIFF resme dönüştüreceğiz. Aşağıdaki kod örneği, PSD resim katmanlarını TIFF resimlere dönüştürmenin nasıl yapılacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **CMYK PSD'yi CMYK TIFF'e Dönüştürme**
Aspose.PSD for Java ile, geliştiriciler CMYK PSD dosyasını CMYK tiff formatına dönüştürebilir. Bu makale, Aspose.PSD kullanarak CMYK PSD dosyasını CMYK tiff formatına nasıl dönüştüreceğinizi göstermektedir. Aspose.PSD for Java ile PSD resimleri yüklenebilir ve TiffOptions sınıfını kullanarak çeşitli özellikler ayarlanabilir ve resmin kaydedilmesi veya dışa aktarılması sağlanabilir. Aşağıdaki kod örneği, bu özelliğin nasıl gerçekleştirileceğini göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Resimleri Dışa Aktarma**
Aspose.PSD, PSD dosya formatlarını diğer formatlara dönüştürmek için özel sınıflar sağlamanın yanı sıra zengin bir dizi resim işleme rutini sunar. Bu kütüphane kullanılarak PSD resimlerinin dönüştürülmesi çok basit ve sezgiseldir. Bu amaç için ImageOptions ad alanında bazı özel sınıflar aşağıda belirtilmiştir.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Aspose.PSD for Java API ile PSD resimlerini dışa aktarmak çok kolaydır. İhtiyacınız olan tek şey ImageOptions ad alanından uygun bir sınıf nesnesidir. Bu sınıfları kullanarak, Aspose.PSD ile oluşturulmuş, düzenlenmiş veya sadece yüklenmiş herhangi bir resmi desteklenen herhangi bir formata kolayca dışa aktarabilirsiniz.
## **Resimleri Birleştirme**
Bu örnek, Graphics sınıfını kullanır ve iki veya daha fazla resmi tek bir tam resim içine nasıl birleştireceğinizi gösterir. İşlemi göstermek için, örnek olarak yeni bir PsdImage oluşturur ve Graphics sınıfı tarafından sergilenen Draw Image metodu kullanılarak Resimleri kanvas yüzeyine çizer. Graphics sınıfı kullanılarak iki veya daha fazla resim, sonuç resminin görünümünde aralık olmadan ve sayfa olmaksızın birleştirilebilir. Kanvas boyutu sonuç resmin boyutuna eşit olmalıdır. Aşağıdaki kod örneği, resimleri bir arada birleştirmek için Graphics sınıfının Draw Image metodu nasıl kullanılacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Resimleri Genişletme ve Kırpma**
Aspose.PSD API, resmi resim dönüşüm işlemi sırasında genişletebilir veya kırparak gerçekleştirme izni verir. Geliştirici, yüklenen resmin genişlemesi veya kırpılması için X ve Y koordinatlarını içeren bir dikdörtgen oluşturmalı ve dikdörtgen kutusunun genişliğini ve yüksekliğini belirtmelidir. Dikdörtgenin X,Y ve Genişlik, Yüksekliği, yüklenen resmin genişletilmesi veya kırpılması işlemini belirtecek. Resim dönüşümü sırasında resmi genişletmek veya kırpmanız gerekiyorsa, aşağıdaki adımları uygulayın:

1. Bir RasterImage sınıfı örneği oluşturun ve mevcut resmi yükleyin.
1. Bir ImageOption sınıfı Örneği oluşturun.
1. Bir Rectangle sınıfı örneği oluşturun ve dikdörtgenin X,Y ve Genişlik, Yükseklik değerlerini başlatın.
1. RasterImage sınıfının Save metodu çağırın ve çıktı dosya adını, resim seçeneklerini ve dikdörtgen nesnesini parametre olarak geçirin.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **XMP Verilerini Okuma ve Yazma**
XMP (Genişletilebilir Meta Veri Platformu), bir ISO standardıdır. XMP, genişletilebilir meta verilerin tanımı ve işlenmesi için bir veri modeli, bir serileştirme biçimi ve temel özellikleri standartlaştırır. Ayrıca XMP bilgilerini popüler bir görüntü dosyasına (örneğin JPEG) gömmek için bir rehber sağlar. Aspose.PSD for Java API'sını kullanarak geliştiriciler, XMP meta verilerini görüntülere okuyabilir veya yazabilirler. Bu makale, XMP meta verilerinin bir görüntüden nasıl okunabileceğini ve görüntülere XMP meta verilerinin nasıl yazılabileceğini göstermektedir.
### **XMP Meta Verisi Oluşturma, Yazma ve Dosyadan Okuma**
XMP ad alanını kullanarak, geliştirici XMP meta veri nesnesi oluşturabilir ve bunu bir görüntüye yazabilir. Aşağıdaki kod örneği, XMP ad alanında bulunan XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage ve DublinCorePackage paketlerinin nasıl kullanılacağını göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Çok İş Parçacıklı Ortamda Resimleri Dışa Aktarma**
Aspose.PSD for Java artık çok iş parçacıklı ortamda resimleri dönüştürmeyi desteklemektedir. Aspose.PSD for Java, kodun çok iş parçacıklı ortamda çalıştırılması sırasında işlemlerin optimize edilmiş performansını sağlar. Aspose.PSD for Java'daki tüm resim seçenek sınıfları (örneğin BmpOptions, TiffOptions, JpegOptions, vb.) IDisposable arabirimini uygular. Bu nedenle, Kaynak özelliği ayarlandığında resim seçenek sınıf nesnesinin uygun şekilde atılması geliştirici için bir zorunluluktur. Aşağıdaki kod örneği, söz konusu işlevselliği açıklamaktadır.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}


Aspose.PSD şimdi çok iş parçacıklı ortamda çalışırken SyncRoot özelliğini destekler. Geliştiriciler, bu özelliği kaynak akışına erişimi senkronize etmek için kullanabilirler. Aşağıdaki kod örneği, SyncRoot özelliğinin nasıl kullanılabileceğini göstermektedir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

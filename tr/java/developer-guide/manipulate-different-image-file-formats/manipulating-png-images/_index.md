---
title: PNG Görüntülerini Düzenleme
type: docs
weight: 30
url: /tr/java/manipulating-png-images/
---

## **PNG Görüntüleri için Şeffaflığı Belirtme**
PNG formatında resimleri kaydetmenin avantajlarından biri şeffaf arka plana sahip olabilmesidir. Aspose.PSD for Java, PngImage ve RasterImage sınıfları için şeffaflığı belirtme özelliği sağlar. Aspose.PSD for Java API, yeni PNG görüntüleri oluştururken veya mevcut görüntüleri PNG formatına dönüştürürken herhangi bir rengi şeffaf olarak belirtmek için kullanılabilir. Bu amaçlar için, Aspose.PSD for Java API'sı şeffaf renk özelliğini ve şeffaf olarak render edilmesi gereken herhangi bir rengi belirten ayarlanabilir PngColorType özelliğini sunmaktadır. Aşağıdaki kod parçası, mevcut bir PSD görüntüsünün PngImage aşırı yüklenmiş yapıcı kullanılarak PNG görüntüsüne dönüştürülmesini ve istenen rengin şeffaf olarak belirtilmesini göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **PNG Görüntüleri için Çözünürlüğü Belirleme**
Aspose.PSD for Java, horizontal ve dikey çözünürlük parametrelerini belirlemek için kullanılabilecek ResolutionSetting sınıfını sunar, PNG dahil tüm görüntü formatları için. Bu makale, Aspose.PSD for Java API'sını kullanarak PNG görüntü formatı için yatay ve dikey çözünürlük parametrelerini belirleme yöntemini göstermektedir. Aşağıdaki kod parçası, mevcut bir PSD görüntüsünü yükler ve PNG formatına dönüştürürken aynı zamanda çözünürlüğü değiştirir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **PNG Dosyalarını Sıkıştırma**
Taşınabilir Ağ Grafik (PNG), bir bit eşiğinin üzerinden bir bit eşiğinden bir bit eşiğinden bir bit eşiğinden bir bit eşiğine doğru bir yollar. Bu değeri ayarlarken dosya boyutunu sıkıştırır ve resim kalitesini düşürmez. Bu makale, Aspose.PSD API'larının size PNG dosya boyutunu kontrol etme imkanı tanıdığını açıklar. Aspose.PSD API'ları, PNG dosya formatı için sıkıştırma seviyelerini belirlemek için int türü CompressionLevel özelliğine sahip olan PngOptions sınıfını kullanabilir. Bu özellik 0 ile 9 arasında bir değer kabul eder, 9 maksimum sıkıştırmadır. Aşağıdaki kod parçası, Aspose.PSD for Java API'sını kullanarak Sıkıştırma Seviyelerini belirlemenin nasıl yapıldığını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **PNG Görüntüleri için Bit Derinliğini Belirtme**
Görüntüleme bit derinliği, bir bit eşiğinin bir bitmap görüntüsünde tek bir pikselin rengini belirtmek için kullanılan bit sayısıdır. Diğer tüm bit eşiğleri formatlarında olduğu gibi, PNG renk derinliği de 1-bit (2 renk), 2-bit (4 renk), 4-bit (16 renk) ve 8-bit (256 renk) gibi bit şeklinde temsil edilir. Aspose.PSD for Java API'sı, PngOptions sınıfı tarafından sağlanan BitDepth özelliğini kullanarak PNG görüntüleri için bit derinliğini ayarlamak için kullanılabilir. Şu anda, BitDepth özelliği, grayscale ve dizinlenmiş renk türleri için 1, 2, 4 veya 8 bitler olarak ayarlanabilir. Diğer tüm renk türleri için yalnızca 8 bit desteklenmektedir. Aşağıdaki kod parçası, bir PNG görüntüsü için Bit Derinliğini nasıl ayarlayacağını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **PNG Görüntülerine Filtre Yöntemleri Uygulama**
Aspose.PSD for Java, PNG görüntüsü için filtre türünü belirlemede kullanılabilecek PngFilterType türünü sunar. Aşağıdaki kod parçası, bir PSD dosyasına filtre uygulanarak PNG görüntüsüne nasıl dönüştürüleceğini göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Şeffaf Bir PNG Görüntüsünün Arka Plan Rengini Değiştirme**
PNG formatındaki görüntüler şeffaf arka plana sahip olabilir. Aspose.PSD for Java, şeffaf arka plana sahip bir PNG görüntüsünün arka plan rengini değiştirme özelliği sağlar. Aspose.PSD for Java API, şeffaf bir PNG görüntüsünün rengini ayarlamak/değiştirmek için kullanılabilir. Aşağıdaki kod parçası, şeffaf bir PNG görüntüsünün arka plan rengini nasıl ayarlayacağını göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}

---
title: Resimleri Düzenleme
type: docs
weight: 50
url: /tr/java/resimleri-duzenleme/
---

## **Raster Görüntüler İçin Rasterleme**
Rasterleme, aslında bir resmi oluşturan noktaların desenini değiştirerek yeni renkler ve tonlarının illüzyonunu yaratma tekniğidir. Bu teknik, resimlerin renk aralığını 256 (veya daha az) renge indirgeme işleminin en yaygın yoludur. Aspose.PSD, RasterImage sınıfı için rasterleme desteği sağlar ve Dither metodu ile iki parametre alarak dithering işlemi sağlar. İlk parametre, uygulanacak Dithering yöntemiyle iki olası seçenek olan FloydSteinbergDithering ve ThresholdDithering türündedir. Dither metodu için ikinci parametre, tam sayı olan BitCount'dur. BitCount, dithering sonucu için örnekleme boyutunu tanımlar. Varsayılan değer 1'dir ve siyah-beyazı temsil eder, izin verilen değerler ise sırasıyla 1, 4, 8 olup 2, 4 ve 256 renk paletleri oluşturur.

## **Parlaklık, Kontrast ve Gama Ayarı**
Dijital resimlerde renk ayarlamaları, çoğu resim işleme kütüphanesinin sağladığı temel özelliklerden biridir. Renk ayarlamaları şu şekilde kategorize edilebilir.

1. Parlaklık, rengin ışıklılığı veya karanlığına atıfta bulunur. Bir resmin parlaklığını artırmak tüm renkleri aydınlatırken, parlaklığı azaltmak tüm renkleri karartır.
2. Kontrast, bir resimdeki nesneleri veya detayları daha belirgin hale getirmeye yöneliktir. Bir resmin kontrastını artırmak, ışık ve koyu bölgeler arasındaki farkı artırır, böylece ışık bölgeleri daha açık ve koyu bölgeler daha koyu hale gelir. Kontrastı azaltmak, daha açık ve daha koyu bölgelerin yaklaşık olarak aynı kalmasını sağlar, ancak genel olarak resim daha homojen hale gelir.
3. Gama, bir objeyi aydınlatan dolaylı ışıklandırmanın kontrastını ve parlaklığını optimize eder.
### **Parlaklık Ayarı**
Aspose.PSD for Java API'sı, RasterImage sınıfı için parlaklık ayarlamak için bir DeğiştirParlaklık metodu sağlar ve bu metotla bir parametre olarak bir tamsayı değeri ile parlaklık ayarlanabilir. En yüksek parametre değeri daha parlak bir resmi temsil eder. İşte karşılaştırma amacıyla orijinal resim ve sonuç resmi.

## **Kontrast Ayarı**
RasterImage sınıfı tarafından sunulan DeğiştirKontrast metodu, bir resmin Kontrastını ayarlamak için bir kayan nokta değeri ile kullanılabilir.

En yüksek parametre değeri, verilen resimde daha yüksek bir kontrastı temsil eder. İşte karşılaştırma amacıyla orijinal resim ve sonuç resmi.

### **Gama Ayarı**
RasterImage sınıfı tarafından sunulan GamaAyarla metodu iki versiyona sahiptir. Aşırı yüklemelerin biri bir kayan nokta değeri kabul eder ve Gama düzeltmesini kırmızı, mavi ve yeşil renk kanal katsayıları için gerçekleştirir. Diğeri ise her renk katsayısını ayrı ayrı temsil eden üç kayan nokta parametre kabul eder. Aşağıdaki kod örneği, bir resimde Gama Ayarını nasıl uygulayacağını göstermektedir.

## **Resme Bulanıklık Ekleme**
Bu makale, bir görüntüde Bulanıklık efekti uygulamak için Aspose.PSD for Java'nın kullanımını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için etkili ve kolay kullanımlı yöntemler sunmuştur. Aspose.PSD for Java, bulanıklık efekti oluşturmak için GaussianBlurFilterOptions sınıfını kullanmıştır. GaussianBlurFilterOptions sınıfı, bir resimde bulanıklık efekti oluşturmak için yarıçap ve sigma değerlerine ihtiyaç duyar. Yeniden boyutlandırma işlemini yapmak için izlenmesi gereken adımlar aşağıdaki gibidir:

1. Image sınıfı tarafından sağlanan Load fabrika metodunu kullanarak bir görüntü yükleyin.
2. Görüntüyü RasterImage'e dönüştürün.
3. Default kurucuyu veya yarıçap ve sigma değerlerini sağlayarak GaussianBlurFilterOptions sınıfından bir örnek oluşturun.
4. GaussianBlurFilterOptions sınıfı örneğini belirtirken RasterImage.Filter yöntemini çağırırken dikdörtgeni (resmin sınırları olarak) belirtin ve GaussianBlurFilterOptions sınıfı örneğini sağlayın.
5. Sonuçları kaydedin.

Aşağıdaki kod örneği, bir resimde bulanıklık efekti oluşturmanın nasıl yapıldığını göstermektedir.

## **Resim Şeffaflığını Doğrulama**
Bu makale, resim şeffaflığını kontrol etmek için Aspose.PSD for Java'nın kullanımını göstermektedir. Resim şeffaflığını kontrol etmenin adımları aşağıdaki gibidir:

1. Image sınıfı tarafından sağlanan Load fabrika metodunu kullanarak bir görüntü yükleyin.
2. Şeffaflığın sıfır olduğunu kontrol edin, eğer şeffaflık sıfırsa resim şeffafsızdır.
3. Aşağıdaki kod örneği, resmin şeffaf olup olmadığını nasıl kontrol edeceğinizi göstermektedir.

## **Kayıplı GIF Sıkıştırıcısı Uygulama**
Aspose.PSD for Java kullanarak geliştiriciler, piksel farkını ayarlayabilirler. GIF'in sıkıştırması, gördüğü piksellerin dizini temelinde yapılandırılmıştır. Normal kodlayıcı, resimdeki piksellerle tam olarak eşleşen en uzun piksel dizesini arar. Kayıplı bir kodlayıcı ise, resimdeki piksellerle "yeterince benzer" olan en uzun piksel dizisini seçer. Aşağıdaki kod, bahsedilen işlevselliğin kodunu göstermektedir.

## **Bikübik Yeniden Örnekleme Uygulama**
Yeniden örnekleme, bir resmin piksel boyutlarını değiştirdiğiniz anlamına gelir. Düşük örnekleme yaptığınızda, pikselleri ortadan kaldırıyorsunuz ve dolayısıyla resminizden bilgi ve detay siliyorsunuz. Büyük örnekleme yaptığınızda ise piksel ekliyorsunuz. Photoshop, bu pikselleri interpolasyon kullanarak ekler. Bu makale, Aspose.PSD for Java kullanarak Bikübik Yeniden Örnekleme nasıl yapılacağını göstermektedir.

Aşağıdaki kod, bahsedilen işlevselliğin kodunu göstermektedir.

## **Ters Renklendirme Ayarı Katmanı**
Bu makale, Aspose.PSD for Java kullanarak **Ters Renklendirme ayarı katmanı** nasıl gerçekleştirileceğini göstermektedir. Ayar katmanları, çoğunlukla renk düzeltmesi için kullanılan özel bir tür katmandır. Kendi içeriğe sahip olmazlar, altlarındaki katmanlardaki bilgileri ayarlarlar. Ters Renklendirme ayarı katmanı, bir resmin renklerini tersine çevirerek negatif bir etki oluşturur.

Aşağıdaki kod, bahsedilen işlevselliğin kodunu göstermektedir.

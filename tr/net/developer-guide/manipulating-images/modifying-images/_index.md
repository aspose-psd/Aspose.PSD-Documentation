---
title: Resimleri Düzenleme
type: docs
weight: 50
url: /tr/net/resimleri-duzenleme/
---

## **Raster Resimler için Dithering**
Dithering, aslında bir görüntü oluşturan noktaların desenini değiştirerek yeni renkler ve tonlar illüzyonunu yaratma tekniğidir. Resimlerin renk aralığını 256 (veya daha az) renge indirgemek için en yaygın kullanılan yöntemdir. Aspose.PSD, [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı için Dither yöntemini tanıtarak dithering desteği sağlar. Bu yöntem, uygulanacak DitheringMethod türünde iki olası seçenek olan FloydSteinbergDithering ve ThresholdDithering'i kabul eden iki parametreyi içerir. Dither yönteminin ikinci parametresi tam sayı türündedir ve dithering sonucu için örnekleme boyutunu tanımlayan BitCount olarak adlandırılır. Varsayılan değer 1 olup siyah ve beyazı temsil eder, izin verilen değerler ise 1, 4, 8 olup sırasıyla 2, 4 ve 256 renk paleti oluştururlar.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimleriCizmeveBiçimleme-DitheringRastgeleResimlerIçin-DitheringRastgeleResimlerIçin.cs" >}}
## **Parlaklık, Kontrast ve Gama Ayarı**
Dijital görüntülerde renk ayarları, çoğu resim işleme kütüphanesinin sağladığı temel özelliklerden biridir. Renk ayarları aşağıdaki şekilde kategorilendirilebilir.

1. Parlaklık, bir rengin ışıklılığı veya karanlığına atıfta bulunur. Bir görüntünün parlaklığını arttırmak, tüm renkleri aydınlatırken parlaklığı azaltmak tüm renkleri karartır.
1. Kontrast, bir görüntüdeki nesneleri veya detayları daha belirgin hale getirme anlamına gelir. Bir görüntünün kontrastını artırmak, ışık ve karanlık alanlar arasındaki farkı artırır, böylece ışık alanlar daha açık, karanlık alanlar daha koyu hale gelir. Kontrastı azaltmak ise daha aydınlık ve karanlık alanların yaklaşık olarak aynı kalmasını sağlar ancak genel görüntü daha homojen hale gelir.
1. Gamma, görüntüde bir nesneyi aydınlatan dolaylı ışık kontrastını ve parlaklığını optimize eder.

### **Parlaklık Ayarı**
Aspose.PSD için .NET API, [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı için parlaklık ayarını yapmak için kullanılabilecek [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) yöntemini sağlar. Burada parametre olarak bir tam sayı değeri geçirilerek resim parlaklığı ayarlanabilir. En yüksek parametre değeri daha parlak bir görüntüyü temsil eder. Aşağıda orijinal resim ve karşılaştırma için sonuç resmi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimleriCizmeveBiçimleme-ParlaklıkAyarı-ParlaklıkAyarı.cs" >}}

### **Kontrast Ayarı**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı tarafından sağlanan [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) yöntemi, bir resmin Kontrastını ayarlamak için float değerini parametre olarak geçerek kullanılabilir.

En yüksek parametre değeri, verilen resimde daha yüksek bir kontrastı belirtir. Aşağıda orijinal resim ve karşılaştırma için sonuç resmi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimleriCizmeveBiçimleme-KontrastAyarı-KontrastAyarı.cs" >}}
### **Gama Ayarı**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfı tarafından sağlanan [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) yönteminin iki versiyonu bulunmaktadır. Aşırı yükleme işlemlerinden biri bir float değerini kabul eder ve kırmızı, mavi ve yeşil kanal katsayıları için Gama düzeltmesini gerçekleştirir. Diğer yüklemenin üç float parametresi, her bir renk katsayısını ayrı ayrı temsil eder. Aşağıdaki kod örneği, bir resimde Gama Ayarını nasıl ayarlayacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimleriCizmeveBiçimleme-GamaAyarı-GamaAyarı.cs" >}}
## **Bir Resme Bulanıklık Ekleme**
Bu makale, Aspose.PSD for .NET'i kullanarak bir resimde Bulanıklık efektini nasıl uygulayacağınızı göstermektedir. Aspose.PSD API'leri bu amaca ulaşmak için etkili ve kullanımı kolay yöntemler sunmaktadır. Aspose.PSD for .NET, anlık bulanıklık efekti oluşturmak için [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) sınıfını sunmaktadır. [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) sınıfı, bir resimde bulanıklık efekti oluşturmak için yarıçap ve sigma değerlerine ihtiyaç duyar. Yeniden boyutlandırma işlemini yapmak için izlenmesi gereken adımlar şunlardır:

1. Görüntü sınıfı tarafından sağlanan Load fabrika yöntemi kullanılarak bir resim yükleyin.
1. Görüntüyü [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) türüne dönüştürün.
1. Boş bellek alanı oluşturarak [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) sınıfından bir örnek oluşturun veya yarıçap ve sigma değerlerini yapılandırıcıda sağlayın.
1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter yöntemini çağırırken dikdörtgeni görüntü sınırları ve [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) sınıf örneğini belirtin.
1. Sonuçları kaydedin.

Aşağıdaki kod örneği, bir resimde bulanıklık efekti oluşturmayı nasıl yapılacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimleriCizmeveBiçimleme-BirResimdeBulanıklıkEkleme-BirResimdeBulanıklıkEkleme.cs" >}}
## **Resim Şeffaflığını Doğrulama**
Bu makale, Aspose.PSD for .NET ile resim şeffaflığını kontrol etmeyi göstermektedir. Resim şeffaflığını kontrol etmek için izlenmesi gereken adımlar şunlardır:

1. [Image](https://reference.aspose.com/psd/net/aspose.psd/image) sınıfı tarafından sağlanan fabrika yöntemi [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) kullanılarak bir resim yükleyin.
1. Şeffaflık sıfır ise resmin şeffaf olduğunu kontrol edin.
1. Aşağıdaki kod örneği, resmin şeffaf olup olmadığını kontrol etmenin nasıl yapıldığını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Örnekler-CSharp-Aspose-ResimCizmeveBicimleme-ResimŞeffaflığınıDoğrulama-ResimŞeffaflığınıDoğrulama.cs" >}}
## **Sonlu GIF Sıkıştırıcıyı Uygulama**
Aspose.PSD for .NET ile geliştiriciler, bir piksel farkı ayarlayabilirler. GIF sıkıştırması, "sözlük" adını verdiği gördüğü pikseller dizisinden oluşur. Normal kodlayıcı, tam olarak resimdeki piksellerle eşleşen en uzun piksel dizisini sözlükte arar. Kayıplı kodlayıcı, resimdeki piksellere "yeterince benzer" en uzun piksel dizisini seçer. Aşağıda belirtilen işleve ait kodun gösterimi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizmeveBicimleme-SonluGIFSıkıştırıcıyıUygulma-SonluGIFSıkıştırıcıyıUygulma.cs" >}}
## **Bikübik Yeniden Örnekleme Uygulama**
Yeniden örnekleme yapmak, bir resmin piksel boyutlarını değiştirdiğiniz anlamına gelir. Küçültme yaptığınızda, pikselleri kaldırıyorsunuz ve dolayısıyla resminizden bilgi ve detayları siliyorsunuz. Büyüttüğünüzde ise piksel ekliyorsunuz. Photoshop, bu pikselleri enterpolasyon kullanarak ekler. Bu makale, Aspose.PSD for .NET kullanarak Bikübik Yeniden Örnekleme işlemini nasıl gerçekleştirebileceğinizi açıklamaktadır.

Aşağıda belirtilen işleve ait kodun gösterimi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizmeveBiçimleme-BikübikYenidenÖrneklemeUygulama-BikübikYenidenÖrneklemeUygulama.cs" >}}
## **Renk Dengesi Ayarlama Katmanı**
Bu makale, Aspose.PSD for .NET'i kullanarak bir resimde **Renk Dengesi ayarlama katmanını** nasıl uygulayacağınızı göstermektedir. Renk dengesi ayarlama katmanı, görüntülerinin renklendirilmesini ayarlama yeteneği sağlar. Üç renk kanalını ve bunların karşılıklı renklerini sunar ve bu çiftlerin dengesini ayarlayarak bir fotoğrafın görünümünü değiştirebilirsiniz.

Aşağıda belirtilen işleve ait kodun gösterimi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizmeveBiçimleme-RenkDengesiAyarKatmanı-RenkDengesiAyarKatmanı.cs" >}}
## **Negatif Ayarlama Katmanı**
Bu makale, Aspose.PSD for .NET'i kullanarak **Negatif ayarlama katmanını** nasıl uygulayacağınızı göstermektedir. Bir ayarlama katmanı, genellikle renk düzeltmesi için başta olmak üzere kullanılan özel bir türdür. Kendi içeriklerine sahip olmak yerine, normalde altlarındaki katmanlardaki bilgileri ayarlarlar. Negatif ayarlama katmanı, bir resmin renklerini ters çevirerek fotoğrafın negatif etkisini oluşturur.

Aşağıda belirtilen işleve ait kodun gösterimi bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-ResimCizmeveBiçimleme-NegatifAyarKatmanı-NegatifAyarKatmanı.cs" >}}

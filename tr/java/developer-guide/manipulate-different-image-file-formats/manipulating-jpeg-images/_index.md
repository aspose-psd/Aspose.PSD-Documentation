---
title: JPEG Görüntülerini Düzenleme
type: docs
weight: 20
url: /tr/java/jpeg-goruntulerini-duzenleme/
---

## **JPEG EXIF Etiketlerini Okumak ve Değiştirmek İçin ExifData Sınıfını Kullanma**


Neredeyse tüm dijital kameralar (akıllı telefonlar dahil), tarayıcılar ve diğer görüntü işleyen sistemler resimleri EXIF (Değiştirilebilir Görüntü Dosyası) bilgileriyle kaydeder. Kamera ayarları ve sahne bilgileri kameranın görüntü dosyasına kaydedilir. EXIF verileri, ayrıca diyafram hızını, bir fotoğrafın çekildiği tarih ve saatini, odak uzunluğunu, pozlama telafisini, ölçüm desenini ve bir flaşın kullanılıp kullanılmadığı gibi bilgileri de içerir. Aspose.Imaging API'leri, verilen bir görüntüden EXIF bilgisini çıkarmayı son derece kolay ve basit hale getirdi. Geliştiriciler, EXIF bilgilerini görüntülere yazabilir veya mevcut bilgileri gereksinimlerine göre değiştirebilirler. Aspose.Imaging, ExifData sınıfını okuma, yazma ve değiştirme işlemleri için sağlarken Aspose.PSD.Exif.Enums isim alanı ise işlem sırasında kullanılan ilgili numaralandırmaları içerir.

### **EXIF Verilerini Okuma**
Aspose.PSD API'leri, bir görüntüden EXIF verilerini okuma olanağı sağlar. Aşağıdaki adımlar, bir görüntüden EXIF bilgisini okumak için ExifData sınıfının nasıl kullanılacağını gösterir.

- Fabrika yöntemi Load kullanılarak PSD Görüntüsü yüklenir.
- PSD kaynakları arasında JPEG küçük resim aranır.
- ExifData sınıfının bir örneği çıkarılır.

Gerekli bilgiler alınır ve konsola yazılır.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-TumEXIFEtiketleriniOku-TumEXIFEtiketleriniOku.java" >}}

Alternatif olarak, geliştiriciler aşağıdaki kod parçacığı kullanarak belirli bilgileri de alabilirler.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-BelirliEXIFEtiketBilgileriniOku-BelirliEXIFEtiketBilgileriniOku.java" >}}

### **EXIF Verilerini Yazma ve Değiştirme**
Aspose.PSD API'leri kullanılarak geliştiriciler, bir görüntünün yeni EXIF bilgilerini yazabilir ve mevcut EXIF verilerini değiştirebilir. Hem Yazma hem de Değiştirme işlemleri, bir görüntünün yüklenmesini ve EXIF verilerinin bir ExifData sınıfı örneğine alınmasını gerektirir. Daha sonra ExifData sınıfı tarafından sunulan özelliklere erişerek bunları uygun şekilde ayarlayabilirler. Görüntülerin işlenmesi için JPEG veya TIFF görüntüleri olması gerektiğini unutmayın, çünkü bunlar genellikle PSD küçük resimleridir. Kullanımı göstermek için örnek kod aşağıdaki gibidir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-YazmaVeDegistirmeEXIFVerisi-YazmaVeDegistirmeEXIFVerisi.java" >}}

## **PSD Kaynaklarından Küçük Resimler Çıkarma**
Küçük resimler, tam çerçeveden ziyade resmin önemli bir bölümünü her göstermek için kullanılan küçültülmüş sürümlerdir. Bazı görüntü dosyalarında (özellikle dijital kamerayla çekilenlerde) bir küçük resim görüntüsü dosyaya gömülü olabilir. Aspose.PSD API'si, PSD kaynak küçük resimlerini çıkarmanıza ve bunları ayrı bir yerde diske kaydetmenize olanak tanır. Küçük resim kaynakları, küçük resim verilerini alabilen ExifData.Thumbnail özelliğini içerir. Aşağıdaki kod parçacığı, bunu nasıl kullanacağınızı gösterir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-PSDKaynaklarindanKucukResimCikarma-KucukResimCikarma.java" >}}


Yukarıda tartışılan yaklaşımı kullanarak küçük resmi diğer desteklenen dosya biçimlerine kaydedebilirsiniz. BMP ve PNG gibi diğer görüntü biçimlerine küçük resim verilerini dışa aktarmak istiyorsanız, diğer görüntü dışa aktarma seçeneklerini kullanmalısınız.

### **JFIF Segmentlerinden Küçük Resimler Çıkarma**
PSD küçük resim kaynaklarının JFIF veya ExifData bölümlerinden küçük resimlerin çıkarılması da mümkündür. Aşağıdaki kod, JFIF veya ExifData bölümünden küçük resim verilerinin nasıl çıkarılacağını gösterir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-PSDKaynaklarindanKucukResimCikarma-KucukResimCikarma.java" >}}


Yukarıda tartışılan yaklaşımı kullanarak küçük resmi diğer desteklenen dosya biçimlerine kaydedebilirsiniz. BMP ve PNG gibi diğer görüntü biçimlerine küçük resim verilerini dışa aktarmak istiyorsanız, diğer görüntü dışa aktarma seçeneklerini kullanmalısınız.

### **JFIF Segmentine Küçük Resim Ekleme**
Aşağıdaki kod örneği, yüklenen bir PSD görüntüsünün JFIF segmentine bir küçük resim eklemek için JFIF.Thumbnail özelliğini nasıl kullanacağını gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-JFIFSegmentineKucukResimEkleme-KucukResimEkleme.java" >}}

Küçük resim verileri diğer segment verileriyle birlikte toplamda 65,545 bayttan büyük olamaz, bu nedenle JPEG formatı özelliklerinden dolayı büyük görüntülerin küçük resmi olarak belirlenmesi gerektiğinde istisna oluşabilir.

### **EXIF Segmentine Küçük Resim Ekleme**
Aşağıdaki kod örneği, yüklenen bir PSD görüntüsünün EXIF segmentine bir küçük resim eklemek için ExifData.Thumbnail özelliğinin nasıl kullanılacağını gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-EXIFSegmentineKucukResimEkleme-KucukResimEkleme.java" >}}

Bu durumda, Aspose.PSD API'si küçük resim görüntüsünün boyutunu tahmin edemez, ancak tüm EXIF veri segmentinin boyutunu kontrol edebilir. Bu 65,535 bayttan büyük olamaz.

## **JPEG EXIF Etiketlerini Okumak ve Değiştirmek İçin JpegExifData Sınıfını Kullanma**
Aspose.PSD API'leri, JPEG görüntü biçimleri için özel olan JpegExifData sınıfını sağlar ve EXIF bilgilerini almak ve güncellemek için bu sınıfın nasıl kullanılacağını gösterir. Aspose.PSD.Exif.JpegExifData sınıfı, JPEG görüntüleri için EXIF veri konteynırı olarak hizmet verir ve standart JPEG EXIF etiketlerini almanın yollarını aşağıdakiler gibi gösterir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-EXIFSegmentineKucukResimEkleme-KucukResimEkleme.java" >}}

### **Tüm EXIF Etiketlerinin Tam Listesi**
Yukarıdaki kod parçacığı, Aspose.PSD.Exif.JpegExifData sınıfı tarafından sunulan özellikler kullanılarak birkaç EXIF Etiketini okur. Bu özelliklerin tam listesi burada bulunmaktadır. Aşağıdaki kod, System.Reflection.PropertyInfo sınıfını kullanarak tüm EXIF etiketlerini okuyacaktır.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-TumEXIFEtiketListesiniOku-TumEXIFEtiketListesi.java" >}}

## **JPEG Görüntülerinin Otomatik Yönlendirilmesi**
Fotoğraflar, 90°, 180°, 270° veya hiçbir açıyla döndürülmüş bir kamerayla çekilebilir. Çoğu dijital kamera, JPEG görüntülerin EXIF etiketleri olarak görüntü verileriyle birlikte yönlendirme bilgisini depolar. Bu bilgi, görüntülerin yönlendirilmesini düzeltmek için kullanılabilir. Aspose.PSD API'leri, Java API için JpegImage sınıfındaki AutoRotate yöntemini jpeg görüntülerin yönlendirmesini otomatik olarak düzeltmek için sağlar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-JPEGGoruntulerininOtomatikYonlendirilmesi-JPEGGoruntulerininOtomatikYonlendirilmesi.java" >}}

## **CMYK ve YCCK ile JPEG-LS Desteği**

Aspose.PSD, Java API'si JPEG-LS için CMYK ve YCCK renk modellerini destekler. Aşağıdaki kod parçacığı, bu desteği nasıl kullanacağınızı gösterir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-JPEGLSileCMYKKu-YCCKDestegi-JPEGLSileCMYKKu-YCCKDestegi.java" >}}

## **JPEG-LS Görüntülerinde 2-7 bitlik sampıl destegi**


Aspose.PSD, Java API'si 2-7 bitlik örnekleme ile JPEG-LS görüntülerini destekler. Aşağıdaki kod parçacığı, bu desteği nasıl kullanacağınızı gösterir:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-2ve7BitlikJPEGDestegi-2ve7BitlikJPEGDestegi.java" >}}

## **JPEG Görüntüleri için ColorType ve CompressionType Ayarlama**


Aspose.PSD, Java API'si, JPEG görüntüleri için Renk Türü ve Sıkıştırma Türü desteği sağlar ve bunları boşluk ve ilerici olarak ayarlar. Aşağıdaki kod parçacığı, bu desteği nasıl kullanacağınızı gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ornekler-src-main-java-com-aspose-psd-ornekler-GoruntuDuzenlemeVeDonusum-JPEG-RenkTuruVeSikistirmaTuru-RenkTuruVeSikistirmaTuru.java" >}}

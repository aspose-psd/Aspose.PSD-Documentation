---
title: JPEG Görüntülerini Düzenleme
type: docs
weight: 30
url: /tr/ağ/dijital-kamera-jpeg-görüntülerini-düzenleme/
---

## **Jpeg EXIF Etiketlerini Okumak ve Değiştirmek İçin ExifData Sınıfı Kullanımı**
Neredeyse tüm dijital kameralar (akıllı telefonlar da dahil), tarayıcılar ve diğer görüntü işleme sistemleri görüntüleri EXIF (Değiştirilebilir Görüntü Dosyası) bilgileri ile kaydeder. Kamera ayarları ve sahne bilgileri kameranın görüntü dosyasına kaydedilir. EXIF verileri ayrıca bir fotoğrafın çekildiği tarih ve saat, enstantane hızı, odak uzaklığı, pozlama telafisi, ölçüm modeli ve flaş kullanımı gibi bilgileri içerir. Aspose.Imaging API'ları, verilen bir görüntüden EXIF bilgilerini çıkarmayı çok kolay ve basit hale getirmiştir. Geliştiriciler, ExifData sınıfını kullanarak görüntülere EXIF verileri yazabilir veya mevcut bilgileri gereksinimlerine göre değiştirebilir. Aspose.PSD, EXIF verilerini okumak, yazmak ve değiştirmek için [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) sınıfını sağlarken [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) ad alanı işlemde kullanılan ilgili numaralı listeleri içerir.
### **EXIF Verilerini Okuma**
Aspose.PSD API'leri, belirli bir görüntüden EXIF verilerini okuma yöntemleri sağlar. Aşağıdaki adımlar, bir görüntüden EXIF bilgilerini okumak için ExifData sınıfının kullanımını açıklar.

- PSD Görüntüsünü fabrika yöntemi Yükle'yi kullanarak yükleyin.
- PSD kaynakları arasında Jpeg küçük resmi bulun.
- ExifData sınıfından bir örnek çıkarın.

Gerekli bilgileri alın ve konsola yazın.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}

Alternatif olarak, geliştiriciler aşağıdaki kod örneğini kullanarak belirli bilgilere de erişebilir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **EXIF Verilerini Yazma ve Değiştirme**
Aspose.PSD API'leri kullanılarak geliştiriciler, bir görüntünün yeni EXIF bilgilerini yazabilir ve mevcut EXIF verilerini değiştirebilir. Hem Yazma hem de Değiştirme işlemleri bir görüntünün yüklenmesini ve EXIF verilerinin ExifData sınıfı örneğine alınmasını gerektirir. Daha sonra, ExifData sınıfı tarafından sunulan özelliklere erişerek bunları ilgili şekilde ayarlayabilirsiniz. Not edilmesi gereken husus, manipülasyon için kullanılacak olan görüntülerin genellikle PSD küçük resimleri olan Jpeg veya Tiff görüntüleri olması gerektiğidir. Kullanımı göstermek için örnek kod aşağıda verilmiştir:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **PSD Kaynaklarından Küçük Resimler Çıkarma**
Küçük resimler, tam çerçevenin yerine resmin önemli bir bölümünü göstermek için kullanılan boyutları küçültülmüş sürümleridir. Bazı görüntü dosyalarında (özellikle dijital kamerayla çekilenler) bir küçük resim görüntüsü dosyaya gömülü olabilir. Aspose.PSD API'sı, PSD kaynak küçük resimlerini çıkartmanıza ve ayrı bir şekilde diske kaydetmenize olanak tanır. Küçük resim kaynakları, küçük resmi geri almak için kullanılabilen ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) özelliğini içerir. Aşağıdaki kod parçacığı, bunu nasıl kullanacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

Yukarıda tartışılan yaklaşımı kullanarak küçük resmi diğer desteklenen dosya formatlarına kaydetmek için kullanabilirsiniz. Eğer küçük resim verilerini BMP & PNG gibi diğer dosya formatlarına dışa aktarmak istiyorsanız, lütfen diğer görüntü dışa aktarım seçeneklerini kullanın.
### **JFIF Segmentlerinden Küçük Resimler Çıkarma**
PSD küçük resim kaynaklarının JFIF segmentlerinden veya EXIF verilerinden küçük resimler çıkarmak da mümkündür. Aşağıdaki kod, JFIF veya ExifData segmentlerinden küçük resim verilerini çıkarma işlemini gösterir:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

Yukarıda tartışılan yaklaşımı kullanarak küçük resmi diğer desteklenen dosya formatlarına kaydetmek için kullanabilirsiniz. Eğer küçük resim verilerini BMP & PNG gibi diğer görüntü formatlarına dışa aktarımak istiyorsanız, lütfen diğer görüntü dışa aktarım seçeneklerini kullanın.
### **JFIF Segmentine Küçük Resim Ekleme**
Aşağıdaki kod parçacığı, yüklenen bir PSD görüntüsünün JFIF segmentine bir küçük resim eklemek için JFIF. Thumbnail özelliğini nasıl kullanacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

JPEG formatı özellikleri nedeniyle diğer segment verileriyle birlikte küçük resim resimleri 65,545 bayttan fazla kaplamamalıdır. Büyük resimlerin küçük resim olarak ayarlanması gereken durumlarda istisnalar oluşabilir.
### **EXIF Segmentine Küçük Resim Ekleme**
Aşağıdaki kod parçacığı, yüklenmiş bir PSD görüntüsünün EXIF segmentine bir küçük resim eklemek için ExifData.Thumbnail özelliğinin nasıl kullanılacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

Bu durumda, Aspose.PSD API'sı küçük resim resminin boyutunu tahmin edemez, ancak EXIF veri segmentinin boyutunu kontrol edebilir. Bu 65,535 bayttan büyük olamaz.
## **Jpeg EXIF Etiketlerini Okumak ve Değiştirmek İçin JpegExifData Sınıfı Kullanımı**
Aspose.PSD API'ları, Jpeg görüntü biçimlerine özgü olan [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) sınıfını sağlar ve EXIF bilgilerini alıp güncellemek için bu sınıfı kullanır. Bu makale, JpegExifData sınıfını kullanarak aynı işlemi gerçekleştirmenin nasıl yapıldığını göstermektedir. Aspose.PSD.Exif.JpegExifData sınıfı, Jpeg görüntüler için EXIF veri konteyneri olarak hizmet eder ve aşağıda gösterildiği gibi standart Jpeg EXIF etiketlerini almanın yollarını sağlar:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Tüm EXIF Etiketlerinin Tam Listesi**
Yukarıdaki kod parçacığı, Aspose.PSD.Exif.JpegExifData sınıfının sunduğu özellikleri kullanarak birkaç EXIF Etiketini okur. Bu özelliklerin tam listesi burada mevcuttur. Aşağıdaki kod, [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) sınıfını kullanarak tüm EXIF etiketlerini okuyacaktır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Jpeg Görüntülerinin Otomatik Doğrultma Düzeltmesi**


Fotoğraflar, 90°, 180°, 270° veya hiç (normal düzlem) döndürülmüş bir kamerayla çekilebilir. Çoğu dijital kamera, JPEG görüntülerin EXIF etiketleri olarak resim verilerinin yanında doğrultma bilgisini saklar. Bu bilgiyi, görüntülerin doğrultmasını düzeltmek için kullanabilirsiniz. Aspose.PSD API'ları, JpegImage sınıfı için AutoRotate yöntemini sağlayarak JPEG görüntülerin doğrultmasını otomatik olarak düzeltmek için AutoRotate yöntemini sunar. Aspose.PSD için .NET API ile AutoRotate yöntemini nasıl kullanabileceğinizi aşağıda görebilirsiniz.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **JPEG-LS ile CMYK ve YCCK Desteği**


Aspose.PSD için .NET API, JPEG-LS ile CMYK ve YCCK renk modellerini destekler. Aşağıdaki kod parçacığı, JPEG-LS için bu desteği nasıl kullanacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **JPEG-LS Görüntülerinde 2-7 bitlik örneklere Destek**


Aspose.PSD için .NET API, 2-7 bitlik örneklere sahip JPEG-LS görüntülerini destekler. Aşağıdaki kod parçacığı, JPEG-LS için bu desteği nasıl kullanacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **JPEG Görüntüleri İçin Renk ve Sıkıştırma Türünü Ayarlama**


Aspose.PSD için .NET API, JPEG görüntüleri için Renk Türü ve Sıkıştırma Türü desteği sağlar ve bunları gri tonlama ve ilerici olarak ayarlar. Aşağıdaki kod parçacığı, bu desteği nasıl kullanacağınızı göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}



Yüklenen bir PSD görüntüsünün EXIF segmentine bir küçük resim eklemek için ExifData.Thumbnail özelliğini nasıl kullanacağınızı gösteren kod parçacığı:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

Bu durumda, Aspose.PSD API'sı küçük resim resminin boyutunu tahmin edemez, ancak EXIF veri segmentinin boyutunu kontrol edebilir. Bu 65,535 bayttan büyük olamaz.

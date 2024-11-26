---
title: Görüntüleri Dönüştürme
type: docs
weight: 20
url: /tr/net/goruntuleri-donusturme/
---

## **Görüntüleri Siyah Beyaz ve Gri Tonlamalıya Dönüştürme**
Bazen renkli görüntüleri siyah beyaz veya gri tonlamalıya dönüştürmeniz gerekebilir, bunu yazdırma veya arşivleme amaçları için. Bu makale, Aspose.PSD for .NET API'nin kullanımını göstererek bu işlemi, aşağıda belirtildiği gibi iki yöntem kullanarak nasıl gerçekleştireceğinizi gösterir.

- Binarizasyon
- Gri tonlama
### **Binarizasyon**
Binarizasyon kavramını anlamak için öncelikle Binary Image'ı tanımlamak önemlidir; bu bir piksel için sadece iki olası değere sahip dijital bir görüntüdür. Normalde, bir ikili görüntü için kullanılan iki renk siyah ve beyazdır, ancak herhangi iki renk kullanılabilir. Binarizasyon, bir görüntüyü iki seviyeliye dönüştürme işlemidir, yani her piksel bir bit (0 veya 1) olarak depolanır, burada 0 renksizliği ve 1 renk varlığını belirtir. Aspose.PSD for .NET API şu anda iki Binarizasyon yöntemini desteklemektedir.
#### **Sabit Eşikle Binarizasyon**
Aşağıdaki kod parçacığı, sabit eşikle binarizasyonun bir görüntüye nasıl uygulanabileceğini gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-SabitEşikleBinarizasyon-SabitEşikleBinarizasyon.cs" >}}

#### **Otsu Eşikle Binarizasyon**
Aşağıdaki kod parçacığı, Otsu eşikle binarizasyonun bir görüntüye nasıl uygulanabileceğini gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-OtsuEşikleBinarizasyon-OtsuEşikleBinarizasyon.cs" >}}

### **Gri Tonlamalı**
Gri tonlama, sürekli tonlu bir görüntüyü, kesintili gri tonları olan bir görüntüye dönüştürme işlemidir. Aşağıdaki kod parçacığı, Gri Tonlama'nın nasıl kullanılacağını gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-Grisalama-Grisalama.cs" >}}

## **GIF Görüntü Katmanlarını TIFF Görüntüye Dönüştürme**
Bazen PSD Görüntüsünün katmanlarını başka bir raster görüntü formatına dönüştürmek ve çıkarmak gerekebilir bir uygulama ihtiyacını karşılamak için. Aspose.PSD API, bir PSD Görüntüsünün katmanlarını başka bir raster görüntü formatına çıkarma ve dönüştürme özelliğini destekler. İlk olarak bir görüntü örneği oluşturacak ve PSD görüntüyü yerel diskten yükleyeceğiz, ardından Her katmanda döngü yapacağız. Daha sonra bloğu TIFF görüntüsüne dönüştüreceğiz. Aşağıdaki kod parçacığı, PSD görüntü katmanlarını TIFF görüntülerine dönüştürmenin nasıl yapıldığını gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-GIFGoruntuKatmanlariToTIFF-GIFGoruntuKatmanlariToTIFF.cs" >}}

## **CMYK PSD'yi CMYK TIFF'ye Dönüştürme**
Aspose.PSD for .NET kullanarak geliştiriciler, CMYK PSD dosyasını CMYK tiff formatına dönüştürebilirler. Bu makale, Aspose.PSD ile bir CMYK PSD dosyasını CMYK tiff formatına nasıl dönüştürüleceğini gösterir. Aspose.PSD for .NET ile PSD görüntülerini yükleyebilir ve ardından [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) sınıfını kullanarak çeşitli özellikleri ayarlayabilir ve görüntüyü kaydedebilir veya dışa aktarabilirsiniz. Aşağıdaki kod parçacığı, bu özelliği nasıl başarabileceğinizi gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-CMYKPSDdenCMYKTiff-CMYKPSDdenCMYKTiff.cs" >}}

## **Görüntüleri Dışa Aktarma**
Aspose.PSD, zengin bir görüntü işleme rutin setinin yanı sıra PSD dosya formatlarını başka formatlara dönüştürmek için özel sınıflar da sağlar. Bu kitaplık kullanılarak, PSD görüntülerinin dönüşümü çok basit ve sezgiseldir. Bu amaçla [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) ad alanındaki bazı özel sınıflar aşağıda listelenmiştir.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Aspose.PSD for .NET API ile PSD görüntülerini dışa aktarmak çok kolaydır. Tek ihtiyacınız olan, [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) ad alanından uygun bir sınıf örneğidir. Bu sınıfları kullanarak, Aspose.PSD for .NET ile oluşturulan, düzenlenen veya sadece yüklenen herhangi bir görüntüyü desteklenen herhangi bir formata kolayca dışa aktarabilirsiniz.

## **Görüntüleri Birleştirme**
Bu örnek, Graphics sınıfını kullanır ve iki veya daha fazla görüntüyü tek bir tam görüntüde birleştirmenin nasıl yapıldığını gösterir. İşlemi göstermek için, örnek, Graphics sınıfının çıplak Image yöntemi kullanarak görüntüleri kanvas yüzeyine çizer ve yeni PsdImage oluşturur. Graphics sınıfının sergilediği Draw Image yöntemini kullanarak, iki veya daha fazla görüntü, bu şekilde birleştirilebilir. Sonuç görüntü, görüntü parçaları arasında boşluk olmayan ve sayfalar olmayan bir şekilde tam bir görüntüyi gösterecek şekilde birleştirilir. Kanvas boyutu sonuç görüntü boyutuna eşit olmalıdır. Aşağıda, görüntüleri birleştirmek için Graphics sınıfının [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) yönteminin nasıl kullanılacağını gösteren kod örneği bulunmaktadır.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-CizimveFormatlamaGoruntuler-BirlestirilmisGoruntuler-BirlestirilmisGoruntuler.cs" >}}

## **Görüntüleri Genişletme ve Kırpma**
Aspose.PSD API, görüntü dönüşüm işlemi sırasında bir görüntüyü genişletebilmenizi veya kırpmınıza olanak sağlar. Geliştirici, bir dikdörtgen oluşturmalı ve X ve Y koordinatlarını belirlemeli ve dikdörtgen kutusunun genişliğini ve yüksekliğini belirtmelidir. Dikdörtgenin X, Y ve Genişlik, Yükseklik'in, yüklenen görüntünün genişletilmesini veya kırılmasını gösterecektir. Görüntü dönüşümü sırasında görüntüyü genişleterek veya kırparak işlem yapılması gerekiyorsa, aşağıdaki adımları gerçekleştirin:

1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) sınıfının bir örneği oluşturun ve mevcut görüntüyü yükleyin.
1. ImageOption sınıfının bir örneğini oluşturun.
1. [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) sınıfının bir örneğini oluşturun ve dikdörtgenin X, Y ve Genişlik, Yükseklik'ini başlatın.
1. RasterImage sınıfının [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) yöntemini çağırırken, çıktı dosya adını, görüntü seçeneklerini ve dikdörtgen nesnesini parametre olarak iletil.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-CizimveFormatlamaGoruntuler-GenisletveKesGoruntuler-GenisletveKesGoruntuler.cs" >}}

## **XMP Verilerini Okuma ve Yazma**
XMP (Genişletilebilir Meta Veri Platformu), bir ISO standardıdır. XMP, genişletilebilir meta verilerin tanımlanması ve işlenmesi için bir veri modeli, bir serileştirme biçimi ve temel özelliklerin standartlaştırılmasını sağlar. Ayrıca, XMP bilgilerini JPEG gibi popüler bir görüntüye gömme yöntemleri hakkında rehberlik sunar, böylece bu tür uygulamalar tarafından desteklenmeyen uygulamaların okunabilirliğini bozmadan gömülü XMP bilgilerini ekleyebilir. Aspose.PSD for .NET API kullanarak, geliştiriciler görüntülere XMP meta verilerini okuyabilir veya yazabilir. Bu makale, XMP meta verilerinin bir görüntüden okunabileceğini ve görüntülere XMP meta verilerinin yazılabileceğini gösterir.
### **XMP Meta Verisi Oluşturma, Yazma ve Dosyadan Okuma**
Xmp ad alanının yardımıyla geliştirici, XMP meta veri nesnesi oluşturabilir ve bunu bir görüntüye yazabilir. Aşağıdaki kod parçacığı, [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp) ad alanında bulunan XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage ve DublinCorePackage paketlerini nasıl kullanacağınızı gösterir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-CizimveFormatlamaGoruntuler-XMPMetadataOlusturma-XMPMetadataOlusturma.cs" >}}

## **Görüntüleri Çok İplikli Ortamda Dışa Aktarma**
Aspose.PSD for .NET artık çok iplikli ortamda görüntüleri dönüştürmeyi desteklemektedir. Aspose.PSD for .NET, kodun çok iplikli ortamda çalıştırılması sırasında işlemlerin optimize edilmiş performansını sağlar. Aspose.PSD for .NET'teki tüm [görüntü seçeneği](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) sınıfları (ör. BmpOptions, TiffOptions, JpegOptions vb.), IDisposable arabirimini uygular. Bu nedenle, kaynak özelliği ayarlandığında geliştiricinin görüntü seçenekleri sınıf nesnesini doğru şekilde atmasının gerekli olduğu bir gerçektir. Aşağıdaki kod parçacığı, söz konusu işlevselliği göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-CokIplikEnvanterindeGoruntuleriDışaAktar-CokIplikEnvanterindeGoruntuleriDışaAktar.cs" >}}

Aspose.PSD şimdi çok iplikli bir ortamda çalışırken SyncRoot özelliğini destekler. Geliştiriciler, kaynak akışına erişimi eşitlemek için bu özelliği kullanabilir. Aşağıdaki kod parçacığı, SyncRoot özelliğinin nasıl kullanılabileceğini göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Ornekler-CSharp-Aspose-Donusum-SyncRoot-SyncRoot.cs" >}}

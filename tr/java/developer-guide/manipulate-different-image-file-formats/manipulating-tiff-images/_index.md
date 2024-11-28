---
title: TIFF Görüntülerini Düzenleme
type: docs
weight: 40
url: /tr/java/tiff-goruntulerini-duzenleme/
---

## **Farklı Ayarlarla Çerçeveler Ekle**
TIFF çok esnek bir formattır ve farklı boyutlarda, sıkıştırma ve diğer ayarlarla farklı çerçeveler eklenmesine izin verir. Aspose.PSD API'leri, karmaşık belgeler oluşturmaya yardımcı olacak şekilde herhangi bir boyuttaki TIFF çerçevesini eklemenize olanak tanır. Eğer çerçeveleri tümü eşit hale getirmek için ekleme işlemi sırasında ayarlamanız gerekiyorsa, aşağıdaki adımları uygulayın:

- İstenen seçeneklerle yeni boş bir çerçeve oluşturun veya CreateFrameFrom yöntemini kullanarak çıktı seçenekleri belirtilmiş kaynak çerçeveyi kopyalayın.
- Kaynak çerçeve/görüntüyü istenen boyuta yeniden boyutlandırın.
- Kaynak çerçeve/görüntü piksellerini yeni çerçeveye ekleyin.
- Yeni çerçeveyi çıktı TIFF görüntüsüne ekleyin.
## **PSD Görüntüsündeki Katmanları Çoklu Sayfalı TIFF Dosya Biçimine Dışa Aktarma**
Bazı durumlarda, PSD görüntü katmanlarını çoklu sayfalı TIFF dosya biçimine dışa aktarmanız gerekebilir. Bu makale, bu görevi Aspose.PSD for Java API'sını kullanarak nasıl gerçekleştirebileceğimizi gösterecektir. İlk olarak, PSD görüntüsünü diskten yükleyeceğiz. Daha sonra PSD görüntü katmanları üzerinde yinelenecek ve karşılık gelen katmanlardan TiffFrame oluşturacağız. Son olarak, elde edilen TIFF görüntüsünü diskte tek bir dosyaya kaydedeceğiz.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **TiffOptions Yapılandırması**


Geliştiriciler, TiffOptions sınıfının farklı özelliklerini ayarlayabilirler. Bu belgede, sonuç görüntü özelliklerini kontrol eden 4 ana özelliği odaklanacağız.

Bu özellikler aşağıda listelenmiştir.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Boş bir TiffOptions yapısını başlattığımızda, her seçenek varsayılan değerine ayarlanır, örneğin sıkıştırma None olarak ayarlanır, BitsPerSample 1 olarak ve Photometric MinIsWhite olarak ayarlanır. Bu formata kaydetme, son görüntünün siyah-beyaz olmasını sağlar ve bu tür seçenekler kombinasyonu için beklenen davranıştır. Renkli sonuçlar elde etmek için yukarıdaki tüm özellikleri, istenen renk uzayına karşılık gelen değerlere ayarlamalısınız veya bu makalenin ilerleyen bölümlerinde tartışılan ön tanımlı ayarlarla TiffOptions yapısını başlatarak Tüm bu özellikleri ayarlayın. Aşağıda, istenilen sonuçlara ulaşmak için ayarlayabileceğiniz beklenen parametre değerlerini tanımlayan bir tablo bulunmaktadır. Lütfen unutmayın, bir yüklü/oluşturulan görüntüyü TIFF dosya biçimine kaydetmek için 4 sütunu da TiffOptions aracılığıyla ayarlamalısınız.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Sıkıştırılmamış|1/4/8/16 (palet, renk modu) yalnızca tek kanal|None|
|MinIsWhite/MinIsBlack|LZW/Sıkıştırılmamış|1/4/8/16 (gri ton, modu) yalnızca tek kanal|None|
|Palet|LZW/Sıkıştırılmamış|8 (palet, renk modu) yalnızca tek kanal|Yatay (LZW aynı örnekler için daha fazla sıkıştırma sağlanır)|
|MinIsWhite/MinIsBlack|LZW/Sıkıştırılmamış|8 (gri ton, modu) yalnızca tek kanal|Yatay (LZW aynı örnekler için daha fazla sıkıştırma sağlanır)|
|RGB|LZW/Sıkıştırılmamış|[8,8,8] (3 RGB kanalı)|None/Yatay|
|RGB|LZW/Sıkıştırılmamış|[8,8,8,8] (3 RGB kanalı ve TiffOptions.AlphaStorage aracılığıyla ek alfa kanalı ayarlanabilir) Aslında herhangi bir ek kanal sayısı desteklenir ancak her kanalın 8 bit boyutunda olması gerekir [8,8,8,8,8,8]|None/Yatay|
Tüm 4 özellik TiffOptions aracılığıyla ayarlanmalıdır herhangi bir görüntü formatını Tiff biçimine kaydetmek için. Farklı kombinasyonlar kullanırken, bazı görüntüleyiciler (Windows Fotoğraf Görüntüleyici de dahil olmak üzere) sunulan görüntüyü oluşturmak için sunulan desteklerini reddedebilir. Bu durumda, testleriniz için farklı bir görüntüleyici seçiniz.
### **TiffOptions Sınıfı İçin Ön Tanımlı Ayarlar**
Kullanıcıların işini kolaylaştırmak ve Tiffoptions örneğinin yanlış yapılandırılmasını önlemek için, Aspose.PSD for Java API, TiffExpectedFormat türünde bir parametre kabul eden başka bir yapılandırıcıyı ortaya koymuştur. TiffExpectedFormat numaralandırmasından seçilen bir değere dayanarak, API, istenilen sonuçları elde etmek için TiffOptions örneği için tüm zorunlu özellikleri otomatik olarak yapılandırır. Örnek kodlara geçmeden önce, kullanımın daha iyi anlaşılabilmesi için TiffExpectedFormat alanlarının listesi ve ayrıntıları aşağıda verilmiştir.



- TiffExpectedFormat.Default: Alanı Varsayılana ayarlamak, Tiffoptions sınıfının varsayılan yapıcı ile aynı gibi davranır, sıkıştırma ayarlanmadan ve BitsPerPixel 1 olarak ayarlanarak siyah-beyaz bir sonuç üretilir. Diğer biçim özgü özelliklerin manuel olarak istenen sonuçlara göre ayarlanması gerektiğinde bu alanın kullanılması tavsiye edilir.
- TiffExpectedFormat.TiffCcitRle: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) TIFF biçiminde RLE kodlamaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffCcittFax3: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) TIFF biçiminde CCITT Fax3 kodlamaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffCcittFax4: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) TIFF biçiminde CCITT Fax4 kodlamaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffDeflateBW: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) TIFF biçiminde Deflate sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffDeflateRGB: Sonucu RGB (renk) TIFF biçiminde Deflate sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffJpegRGB: Sonucu RGB (renk) TIFF biçiminde Jpeg sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffJpegYCBCR: Sonucu YCBCR (renk) TIFF biçiminde Jpeg sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffLzwBW: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) TIFF biçiminde LZW sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffLzwRGB: Sonucu RGB (renk) TIFF biçiminde LZW sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffLzwRGBA: Sonucu RGBA (şeffaletli renk) TIFF biçiminde LZW sıkıştırmaya özgü olarak ayarlama.
- TiffExpectedFormat.TiffNoCompressionBW: Sonucu 1 BitsPerPixel'lık (siyah-beyaz) sıkıştırılmamış TIFF biçiminde kaydetmeye özgü olarak ayarlama.
- TiffExpectedFormat.TiffNoCompressionRGB: Sonucu RGB (renk) sıkıştırılmamış TIFF biçiminde kaydetmeye özgü olarak ayarlama.
- TiffExpectedFormat.TiffNoCompressionRGBA: Sonucu RGBA (şeffaletli renk) sıkıştırılmamış TIFF biçiminde kaydetmeye özgü olarak ayarlama.

Aşağıdaki kod parçası, TiffOptions sınıfının bir örneğinin oluşturulurken TiffExpectedFormat alanlarının kullanımını açıklar.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Deflate ve Adobe Deflate Sıkıştırma Desteği**
TIFF (Etiketli Görüntü Dosyası Biçimi) dosya biçimi, sıkıştırma türlerini destekler, sıkıştırma türü dosyada bir etiket (bir tamsayı değeri) olarak saklanır. Bu tür sıkıştırma yöntemlerinden biri Adobe Deflate'dir (önceki adıyla Deflate). Aspose.PSD for Java API, TIFF görüntülerinin dışa aktarımı ve oluşturulması için bu sıkıştırma yöntemini destekler.
### **Deflate Sıkıştırmalı TIFF Görüntüsünü Kaydetme**
Yüklenen görüntüleri Deflate/Adobe Deflate sıkıştırmalı TIFF biçimine dönüştürmek kolaydır. Aşağıdaki gibi.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Adobe Deflate Sıkıştırmalı TiffImage Oluşturma**
Aşağıda sunulan örnek, Aspose.PSD for Java API'nın, Adobe Deflate sıkıştırma yöntemini kullanarak sıfırdan bir görüntü oluşturmak için nasıl kullanılabileceğini göstermektedir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **TIFF Görüntülerinin Sıkıştırılması**
Aspose.PSD for Java API, PSD görüntülerini TIFF görüntü biçimine dönüştürmek ve oluşan TIFF görüntüsünün sıkıştırmasını değiştirmek için kullanılabilir. API ayrıca görüntüleri TIFF görüntüsünde arşivleme amacıyla farklı çerçevelerde depolamak için de kullanılabilirken görüntülerin veri boyutunu en aza indirerek sıkıştırmalıdır. En iyi sıkıştırma oranını elde etmek için endeksli renk uzayları kullanılabilir. Aşağıdaki kod parçası, en iyi sıkıştırma sağlamak için 16 endeksli renk kullanarak ve LZW sıkıştırma algoritmasını kullanarak en iyi sıkıştırmayı gerçekleştirir ancak kaynak renkler hafifçe titrek olabilir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}

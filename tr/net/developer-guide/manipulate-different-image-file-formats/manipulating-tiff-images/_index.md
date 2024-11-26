---
title: TIFF Görüntülerini Manipüle Etmek
type: docs
weight: 50
url: /tr/net/tiff-goruntulerini-manipule-etme/
---

## **Farklı Ayarlarla Kareler Ekleme**
TIFF çok esnek bir formattır ve farklı karelerin farklı boyutlarda, sıkıştırma ve diğer ayarlarla eklenmesine olanak tanır. Aspose.PSD API'leri istediğiniz boyuttaki herhangi bir TIFF karesini eklemenize olanak sağlar ve karmaşık belgeler oluşturmanıza yardımcı olur. Tüm kareleri eşit yapmak için eklem işlemi sırasında kareleri ayarlama gereksinimi varsa, aşağıdaki adımları uygulayın:

- İstenen seçeneklerle yeni boş bir kare oluşturun veya CreateFrameFrom yöntemini kullanarak belirtilen çıktı seçeneklerini içeren kaynak kareyi kopyalayın.
- Kaynak çerçeve/görüntüyü istenen boyutlara yeniden boyutlandırın.
- Kaynak karenin/görüntünün piksellerini yeni çerçeveye ekleyin.
- Yeni çerçeveyi çıktı TIFF görüntüsüne ekleyin.
## **PSD Görüntüsünden Katmanları Çoklu Sayfalı Tiff Dosya Biçimine Aktarma**
Bazen PSD görüntü katmanlarını çoklu sayfalı TIFF dosya biçimine aktarmanız gerekebilir. Bu makalede, Aspose.PSD for .NET API'sını kullanarak bu görevi nasıl gerçekleştirebileceğimizi göstereceğiz. İlk olarak, diskten PSD görüntüsünü yükleyeceğiz. Daha sonra PSD görüntü katmanları üzerinde işlem yapacak ve ilgili katmanlardan TiffFrame oluşturacağız. Son olarak, elde edilen Tiff görüntüsünü diske tek bir dosyada kaydedeceğiz.


## **TiffOptions Yapılandırması**

Geliştiriciler, [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) sınıfının farklı özelliklerini ayarlayabilirler ve istenen sonuçları alabilirler. Bu belgede, sonuç görüntü özelliklerini kontrol eden 4 ana özelliğe odaklanacağız.

Bu özellikler aşağıda listelenmiştir.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Boş bir TiffOptions yapısı başlattığımızda, her seçenek varsayılan değerine ayarlanır, örneğin sıkıştırma None olarak ayarlanır, BitsPerSample 1 olarak ayarlanır ve Fotometrik MinIsWhite olarak ayarlanır. Bu formata kaydetmek, son görüntüyü siyah beyaz yapar ve bu, böyle seçenekler kombinasyonu için beklenen davranıştır. Renkli sonuçları elde etmek için yukarıdaki tüm özellikleri istenen renk uzayına karşılık gelen değerlere ayarlamanız veya TiffOptions yapısını bu makalede daha sonra tartışılan önceden tanımlanmış ayarlarla başlatmanız gerekir. İstenen sonuçları elde etmek için ayarlayabileceğiniz beklenen parametre değerlerini açıklayan aşağıdaki tabloyu sağlanmıştır. Lütfen dikkat edin, herhangi bir yüklenen/oluşturulan görüntüyü TIFF dosya biçimine kaydetmek için TiffOptions üzerinden 4 sütunu da ayarlamanız gerektiğini unutmayın.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palet|LZW/Sıkıştırılmamış|1/4/8/16 (palet, renk modu) yalnızca tek kanal|Yok|
|MinIsWhite/MinIsBlack|LZW/Sıkıştırılmamış|1/4/8/16 (gri ölçek modu) yalnızca tek kanal|Yok|
|Palet|LZW/Sıkıştırılmamış|8 (palet, renk modu) yalnızca tek kanal|Horizontal (aynı desenler için LZW için daha fazla sıkıştırma sağlanır)|
|MinIsWhite/MinIsBlack|LZW/Sıkıştırılmamış|8 (gri ölçek modu) yalnızca tek kanal|Horizontal (aynı desenler için LZW için daha fazla sıkıştırma sağlanır)|
|RGB|LZW/Sıkıştırılmamış|[8,8,8] (3 RGB kanalı)|Yok/Horizontal|
|RGB|LZW/Sıkıştırılmamış|[8,8,8,8] (3 RGB kanalı ve TiffOptions.AlphaStorage aracılığıyla ek bir alfa kanalı ayarlanabilir) Aslında herhangi bir ek kanal sayısı desteklenir ancak her kanalın 8 bit boyutunda olması gerekmektedir [8,8,8,8,8,8]|Yok/Horizontal|
Tüm 4 özellik de TiffOptions üzerinden ayarlanmalıdır, herhangi bir görüntü biçimini Tiff biçimine kaydetmek için. Farklı kombinasyonlar kullanırken bazı görüntüleyiciler (Windows Fotoğraf Görüntüleyici de dahil olmak üzere) sınırlı destek sunmaları nedeniyle sonuç görüntüyü işlemeyi reddedebilir. Bu durumda testleriniz için farklı bir görüntüleyici seçmelisiniz.

### **TiffOptions Sınıfı için Önceden Tanımlı Ayarlar**
Kullanıcıların işini kolaylaştırmak ve TiffOptions örneğinin yanlış yapılandırılmasını engellemek için Aspose.PSD for .NET API'si, TiffOptions örneğinin istenen sonuçları üretmek için TiffExpectedFormat türünde bir parametre kabul eden başka bir yapılandırıcı açıklamıştır. TiffExpectedFormat numaralandırmasından seçilen değere dayanarak, API aracı, istenen sonuçları üretmek için TiffOptions örneği için tüm zorunlu özellikleri otomatik olarak yapılandırır. Örneğin, örnek kodlara geçmeden önce, kullanımın daha iyi anlaşılması için TiffExpectedFormat alanlarının listesi ve ayrıntıları aşağıda sağlanmıştır.



- TiffExpectedFormat.Default: Alanı Default olarak ayarlamak, istenen sonuçlara göre manuel olarak diğer belirli format özelliklerinin ayarlanması gerektiğinde TiffOptions sınıfının varsayılan yapısının bir yapılandırıcısı gibi davranır.
- TiffExpectedFormat.TiffCcitRle: Sonucu 1 BitsPerPixel (siyah beyaz) TIFF formatında kaydederken RLE kodlamasına özgüdür.
- TiffExpectedFormat.TiffCcittFax3: Sonucu 1 BitsPerPixel (siyah beyaz) TIFF formatında CCITT Fax3 kodlamasına özgüdür.
- TiffExpectedFormat.TiffCcittFax4: Sonucu 1 BitsPerPixel (siyah beyaz) TIFF formatında CCITT Fax4 kodlamasına özgüdür.
- TiffExpectedFormat.TiffDeflateBW: Sonucu 1 BitsPerPixel (siyah beyaz) TIFF formatında Deflate sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffDeflateRGB: Sonucu RGB (renkli) TIFF formatında Deflate sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffJpegRGB: Sonucu RGB (renkli) TIFF formatında Jpeg sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffJpegYCBCR: Sonucu YCBCR (renkli) TIFF formatında Deflate sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffLzwBW: Sonucu 1 BitsPerPixel (siyah beyaz) TIFF formatında LZW sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffLzwRGB: Sonucu RGB (renkli) TIFF formatında LZW sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffLzwRGBA: Sonucu RGBA (şeffaletli renk) TIFF formatında LZW sıkıştırmasıyla kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffNoCompressionBW: Sonucu 1 BitsPerPixel (siyah beyaz) için sıkıştırmasız TIFF formatında kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffNoCompressionRGB: Sonucu renkli için sıkıştırmasız TIFF formatında kaydetme işlemine özgüdür.
- TiffExpectedFormat.TiffNoCompressionRGBA: Sonucu şeffaletli olan renkli için sıkıştırmasız TIFF formatında kaydetme işlemine özgüdür.



Aşağıdaki kod parçacığı, TiffOptions sınıfının bir örneğini oluştururken TiffExpectedFormat alanlarının kullanımını ayrıntılı olarak açıklar.

## **Deflate ve Adobe Deflate Sıkıştırmasını Destekleme**
TIFF (Etiketli Görüntü Dosya Biçimi) dosya biçimi çeşitli sıkıştırma türlerini desteklerken sıkıştırma türü, dosyadaki bir etiket (bir tamsayı değeri) olarak saklanır. Bu sıkıştırma yöntemlerinden biri Adobe Deflate (önceden Deflate olarak bilinir). Aspose.PSD for .NET API, TIFF görüntülerinin dışa aktarımını ve oluşturulmasını desteklerken bu sıkıştırma yöntemini destekler.
### **Görüntüyü Deflate Sıkıştırma ile TIFF Dosyasına Kaydetme**
Yüklenen görüntüleri TIFF formatına Deflate/Adobe Deflate sıkıştırmasıyla dönüştürmek kolaydır.


### **Adobe Deflate Sıkıştırmasıyla TiffImage Oluşturma**
Aşağıdaki örnek, Aspose.PSD for .NET API'sının Adobe Deflate sıkıştırma yöntemini kullanarak scratch'ten görüntü oluşturmak için nasıl kullanılabileceğini göstermektedir.


### **TIFF Görüntülerinin Sıkıştırılması**
Aspose.PSD for .NET API, PSD görüntülerini TIFF görüntü biçimine dönüştürmek ve sonuç TIFF görüntüsünün sıkıştırmasını değiştirmek için kullanılabilir. API ayrıca, görüntü sıkıştırmasını en düşük veri boyutuna sıkıştırarak arşivleme amaçlı farklı görüntüleri TIFF görüntüsüne kare olarak saklayabilir. Görüntü sıkıştırma, kullanılan sıkıştırma algoritması ne olursa olsun kaynak veri boyutunu azaltarak gerçekleştirilmelidir. En iyi sıkıştırma oranını elde etmek için indeksli renk uzayları kullanabiliriz. Aşağıdaki kod parçacığı, 16 dizinli renk kullanarak ve LZW sıkıştırma algoritması kullanarak en iyi sıkıştırmayı gerçekleştirir, ancak kaynak renkler biraz titrek olabilir.

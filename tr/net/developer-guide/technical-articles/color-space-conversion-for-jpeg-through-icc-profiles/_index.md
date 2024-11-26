---
title: JPEG için ICC Profilleri Aracılığıyla Renk Uzayı Dönüşümü
type: docs
weight: 60
url:/tr/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **JPEG Formatı için Renk Yönetimi**


Bu makale, Aspose.PSD API'leriyle JPEG formatını işlerken renk uzayı yönetimini gerçekleştirmek için ICC profillerinin kullanımını tartışmaktadır. JPEG'in iç renk uzayı YCbCr iken bu [format](https://reference.aspose.com/psd/net/aspose.psd/pixelformat), görüntünün meta verilerini saklamak için Grayscale, RGB, CMYK ve YCCK renk uzaylarını da içerebilir. Aspose.PSD API'leri genellikle RGB uzayında çalışır bu yüzden API'nin JPEG dosyalarını uygun şekilde işlemesi için renk uzayı dönüşümü gerçekleştirmesi gerekir. Grayscale'den RGB'ye ve YCbCr'den RGB'ye dönüşümler matematiksel dönüşümlerle yapılabilir ancak CMYK ve YCCK uzayları kolayca RGB uzayına dönüştürülemez.

Aspose.PSD API'leri, CMYK renk uzayına sahip JPEG görüntüler için doğrudan RGB'den CMYK renk dönüşümü gerçekleştirmek zorundadır. Öte yandan, YCCK renk uzayına sahip görüntüler, RGB'den CMYK'ye YCCK renk dönüşümü gerektirir. CMYK'ten YCCK dönüşümü, ilk üç kanal için uygulanan [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) dönüşümünü kullanırken k-kanalı dokunulmamış bırakır. Kısacası, Aspose.PSD API'leri, hem CMYK hem de YCCK görüntüler için RGB ve CMYK renk uzayları arasında değiştirme yapmak zorundadır ve bu tür dönüşümler, bir rengin özelliklerini tanımlayan ve renk dönüşümlerine yardımcı olan tablo görünümünde olan ICC profilleri yardımıyla gerçekleştirilir.


## **ICC Profilleri**
ICC dönüşüm mekanizması, kaynak renk uzayını cihaza bağımsız olarak CIELAB veya CIEXYZ renk uzaylarına eşleyen "Profiller" kullanır. Aspose.PSD, gerektiğinde veriyi bu iki renk uzayı ile birlikte ek profiller kullanarak renk uzayına dönüştürebilir. Bu nedenle, ICC dönüşümü için kullanıcı, iç CIE renk uzayına ulaşmak için bir RGB profil ve CMYK renk özelliklerini almak için bir CMYK profil olmak üzere iki profil sağlamalıdır. CMYK'den RGB'ye dönüşümü başarmak için profil değişimine ihtiyaç vardır, yani; CMYK profili kaynak profil olarak kullanılır ve RGB profili hedef profil olarak kullanılır.
## **ICC Profilleri Aracılığıyla JPEG için Renk Dönüşümü**
Aspose.PSD API'leri detayları gizler ve ICC profillerini [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions) sınıfı aracılığıyla belirtmek için kullanımı kolay bir mekanizma sunar. Ayrıca, Aspose.PSD, SWOP, CMYK ve sRGB örnek profillerini çekirdeğine gömülü kullandığından bu nedenle, yaygın kullanım durumlarında, kullanıcının herhangi belirli profiller aramasına gerek yoktur. Bu tür düzeltmelerin dezavantajı vardır, yani; RGB'den CMYK'ye ve tekrar RGB'ye dönüşüm sonrasında aynı rengi almayı bekleyemeyiz çünkü uyumsuz renk uzayları ve farklı renk profillerinden dolayı. Aşağıdaki kod parçacığı, Aspose.PSD'nin .NET API'sini kullanarak RGB ve CMYK renk profillerini YCCK JPEG görüntüsü için belirleme kullanımını göstermektedir. Aşağıdaki örnekte RGB ve CMYK renk profilleri değiştirilir ve görüntü YCCK renk uzayına kaydedilir. Lütfen [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) ve [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) özelliklerinin YCCK renk uzayı için piksel verilerini değiştirmek için çalışacağını unutun. Diğer tüm renk uzayları renk verilerini güncelleme için renk profillerini getirmez.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


Profil ayarlanmazsa Aspose.PSD .NET API'si varsayılan profilleri kullanacaktır. Aşağıdaki örnek, çoğu JPEG görüntüsü için hedef profiller özelliklerini kullanır.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}


---
title: PSD Farklı Renk Modları Arasında Dönüştürme
type: docs
weight: 50
url: /tr/net/psd-convert-between-different-color-modes/
---

Aspose.PSD'nin desteklediği renk modlarını bu makaleden öğrenebilirsiniz.

Aspose.PSD örneğin, 8 bitlikten 16 bite ve tam tersine dönüşümü destekler. CMYK ICC-Profil dönüşümleri ve diğer tür bit derinliğinden diğerine dönüştürmeleri destekler. Burada PSD Dosyasında Grayscale'a dönüştürmenin nasıl yapıldığını görebilirsiniz.
## **CMYK, RGB, Grayscale'den Grayscale Renk Moduna Dönüştürme**
Aşağıda verilen örnek kod, Photoshop olmadan CMYK, RGB veya Grayscale dönüşümü nasıl yapılacağını göstermektedir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **16-bit photoshop görüntüsünü 8-bit grayscale moda dönüştürme**
Ancak 16-bit Grayscale Photoshop görüntüsünü 8-bit grayscale moda dönüştürmek isterseniz ne yapmalısınız? Aşağıdaki kod parçasını kullanmanız gerekir. 8 bit, PSD Dosyalarında yaygın bir bit derinliğidir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **Grayscale'ı RGB'ye Dönüştürme**
Başka bir karmaşık durum, Grayscale PSD Görüntüsünü RGB Görüntüsüne dönüştürmeniz gerektiğinde oluşur.

Grayscale görüntüler yalnızca bir kanala sahiptir, ancak RGB görüntülerin 3 kanalı vardır: R - kırmızı, G - yeşil, B - mavi. Aspose.PSD Grayscale'ı RGB'ye dönüştürebilir.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}

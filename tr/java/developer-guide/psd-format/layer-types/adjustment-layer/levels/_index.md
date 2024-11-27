---
title: Photoshop Seviyeleri Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/levels/
---

## Java'da Photoshop Seviyeler Ayarlama Katmanı İle Çalışmak

Bu makalede, Java'da [PSD dosya formatında](/psd/tr/java/psd-format/) bir fotoğrafın tonal aralığını ve renk dengesini programatik olarak nasıl ayarlayacağımızı öğreneceğiz. Adobe® Photoshop® fotoğraf düzenleyicisini kendisi olarak kullanmıyoruz. Bunun yerine Photoshop belgesini manipüle etmek için kendi başına çalışan Aspose.PSD kütüphanesini kullanıyoruz.

Aspose.PSD for Java'da fotoğrafı istediğimiz gibi düzenlemek için yeterli sayıda [aracı desteklese de](/psd/tr/java/manipulating-images/), **Seviyeler ayarlama katmanı API'sıyla devam edelim** ki bu çalışmanın en basit ve en hızlı yollarından biridir.

## API genel bakış

Şu anki implementasyon (yazıldığı an itibarıyla 20.6) Seviyeler ayarlama katmanı API'sının **Photoshop Seviyelerinin tüm temel özelliklerini desteklemektedir** , yani, RGB bileşik kanalı için giriş ve çıkış Seviyelerini ve her birincil renkli kanal için (kırmızı, yeşil ve mavi) ayarlama yapmaktadır.

Seviyeler ayarlama katmanı API'sı açıktır. [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) sınıfı Seviyeler ayarlamaya giriş noktasıdır. Renk kanallarına erişmek için birkaç yöntem içermektedir: getMasterChannel ve getChannel(int). Her iki yöntem de giriş ve çıkış Seviyelerinin manipülasyonu için karşılık gelen özelliklere sahip olan [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) döndürür. Fark şudur ki getMasterChannel, bileşik renk kanalını (RGB) ayarlamak için hizmet verirken, getChannel, belirli bir renk kanalına (kırmızı, yeşil veya mavi) (endeksine göre) erişir.

## Renk modları ile uyumluluk

Değerlidir ki Seviyeler ayarlama katmanı **Photoshop Seviyelerine göre çoğu renk modu ile uyumludur**. Bu nedenle, Grayscale (grinin kanal), RGB (RGB, kırmızı, yeşil ve mavi kanallar), CMYK (CMYK, cyan, magenta, sarı ve siyah kanallar), Duotone (tek tonlu kanal) ve LAB (ışıklılık, a ve b kanalları) renk modlarındaki görüntülerin Seviyelerini ayarlamak mümkündür.

## Tonal aralığı ayarla

Basitçe ifade etmek gerekirse, tonal düzeltme bir resme gölge ve ışık alanlarını tekrar haritalamak ve orta tonların daha iyi dağılımını sağlamak için uygulanır. Genellikle **resmi daha kontrast gösterir** , doğru şekilde yapılırsa. Örneğin, bir köpeğin fotoğrafını (b) alalım ve tonal aralığını ayarlayarak (a – ekran görüntüsü, fotoğrafın daha kontrast görünmesi için Photoshop Seviyeler penceresinden elde edilmiştir) fotoğrafın daha kontrast (c) görünmesini sağlayalım.

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Seviyeler Katmanı Şekil 1](levels-adjustment-figure-1.png)|

Bir görüntünün **genel tonal aralığını ayarlamak** için, ana kanalın giriş Seviyeleri ayarlanmalıdır:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Gölge için giriş Seviyelerinin 0 ila 253 arasında, orta tonlar için 9.99 ila 0.01 arasında ve ışık alanı için 2 ila 255 arasında olması gerektiği unutulmamalıdır. Çıkış Seviyelerinin aralığı, 0 ila 255 arasında olmalıdır.

Daha fazla örnek mi gerekiyor? Onları [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) ve [bilgi tabanında](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers) bulabilirsiniz.

## Sonuç

Özetlemek gerekirse, Java için Aspose.PSD, hemen hemen tüm renk modlarıyla uyumlu olan bir görüntünün tonal aralığını ve renk dengesini değiştirmek için kullanışlı ve basit bir API'ye sahiptir. Kütüphanenin Seviyeler ayarlama katmanı API'sı Photoshop Seviyelerine benzer görünüyor, bu nedenle, kütüphaneyle daha önce çalışmamış olsanız bile başlamak kolaydır.

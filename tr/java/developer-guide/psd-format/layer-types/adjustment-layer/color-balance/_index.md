---
title: Renk Denge Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/color-balance/
---

# Photoshop'ta Renk Denge Ayarlama Katmanı ile Çalışma

Bu makalede, Java'da PSD dosya formatındaki resmin **renk dengesini ayarlamayı** ele alacağız. Bu işlem için Photoshop belgelerinin işlenmesi için bir araç kutusu olan Aspose.PSD for Java adlı özel bir kütüphaneyi kullanacağız.

Kütüphane PSD dosya formatıyla çalıştığı için, içinde Photoshop düzenleyicisinde bulunan neredeyse [tüm özellikleri](https://docs.aspose.com/psd/java/features/) içerir ve **Renk Denge Ayarlama Katmanı** da bu görev için oldukça uygundur.

Renk Denge Ayarlama Katmanı, gölgeler, orta tonlar ve vurgular için temel (RGB) ve çıkarma (CMY) renkler arasındaki dengeyi basit ve hızlı bir şekilde değiştirmeyi mümkün kılar.

## Renk Denge Ayarlaması

Daha önce de belirtildiği gibi, Aspose.PSD for Java'daki Renk Denge Ayarlama Katmanı, **temel ve çıkarma renkler arasında bir dengeleyici**dir. Bu, her renk çifti için üç ölçek olduğu anlamına gelir (siyah/kırmızı, macenta/yeşil, sarı/mavi). Değeri ona doğru hareket ettikçe ve aksi takdirde belirli bir rengin yoğunluğu artar. Dahası, bu üç çift, tonal aralığın her alanına (gölgeler, orta tonlar ve vurgular) özgüdür ve bu tür ayarlamanın esnekliğini artırır.

Bu bilgiyi uygulamada kullanalım. Örneğin, bayanın yüzünün kırmızımsı olduğu bir fotoğrafı seçtik (b). Yüz çok kırmızımsı ve bunu düzeltmek için kırmızıyı azaltacak ve temelde maviyi artıracak olan **Renk Denge Ayarlama Katmanını ekleyeceğiz** (a) ve daha doğal görünen bir yüz elde etmek için (c). Yine de bu görüntüyle yapılacak çok iş var, ancak bu makalede yapacaklarımız bu kadar.

![Renk Denge Ayarlama Katmanı örneği](color-balance-adjustment-layer-example-figure-1.png) Renk Denge Ayarlama Katmanı API'sinin düz bir tasarımı vardır. Bu nedenle, ihtiyacınız olan tek şey olan [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) sınıfını kullanmalısınız. İlk olarak, varsayılan olarak devre dışı bırakılmış olan aydınlığı koruyun. Ardından, gölgeler için biraz yeşil ve biraz daha fazla sarı ekleyin (adları belirli tonal aralık alanı adı ve renk çiftindeki renklerden oluşan metodlar). Daha sonra orta tonlar için daha fazla mavi ekleyin ve biraz pembe ekleyin:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Şimdi istediğimiz resme sahibiz! Gerçekten basit değil mi?

_Dikkat edin ki_ _her renk çiftinin değeri -100 ila 100 aralığında olmalıdır_, yani çıkarma renkleri için negatif değerler ve sırasıyla temel renkler için pozitif değerlerdir, tam olarak Photoshop düzenleyicisinde olduğu gibi.

Teknik ayrıntılar hakkında daha fazla bilgi edinmek için [Renk Denge Ayarlama Katmanı API referansına](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) başvurun.

## Sonuç

Bu makalede, Aspose.PSD for Java kütüphanesini kullanarak Java'da resmin Renk Denge ayarını nasıl programlı olarak yapıacağımızı ele aldık. Kütüphane, Photoshop belgelerinde Renk Denge ayarlama katmanları ile çalışmak için tam özellikli bir API içerir.

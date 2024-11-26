---
title: Kanal Karıştırıcı Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/channel-mixer/
---

# Java'da Photoshop Kanal Karıştırıcı Ayarlama Katmanı ile Çalışmak

Bugün, Photoshop belgelerinde renk kanallarını nasıl programlı olarak karıştıracağımıza bakacağız. Bu işlemi gerçekleştirmek için Photoshop düzenleyici Java komut dosyalarını desteklemediğinden, Java için Aspose.PSD adlı özel PSD dosya biçimi işleme kütüphanesini kullanacağız.

Kütüphane, **renk kanalları ile çalışma API'sı** içerir. Renkleri karıştırmanın çeşitli yolları vardır ancak bu makalede Kanal Karıştırıcı ayarlama katmanına odaklanacağız.

Kanal Karıştırıcı ayarlama katmanı API'sı, **renk kanallarıyla oynamaya izin verir** ve titiz görüntüler oluşturmak veya farklı yaratıcı renk efektleri oluşturmak veya hatta görüntüyü siyah beyaz yapmak için kullanılabilir. Bundan sonra, Aspose.PSD'nin Java için mevcut olan Photoshop belgesine Kanal Karıştırıcı ayarlama katmanı uygulama şeklini ele alacağız ancak önce genel API özellikleri hakkında konuşmamız gerekiyor.

## API genel bakış

Kanal Karıştırıcı ayarlama katmanı oluşturmada özel bir şey yoktur. [Varsayılan fabrika yöntemi](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) aracılığıyla eklenebilir ve KanalMixerLayer sınıfının bir örneğini döndürür. Bu sınıf, Tek Renk seçeneği gibi genel işlevselliği içerir ve bir çıktı kanalını almak için bir yönteme sahiptir. Belirli çıktı kanalı iki türden biri olabilir: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) veya [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel)'ın türü, görüntünün [renk moduna](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) bağlıdır.

## Görüntüyü tek renkli yapma

Şimdi, mevcut bir Photoshop belgesine Kanal Karıştırıcı ayarlama katmanı uygulama örneğini ele alalım. Bu tür ayarlama katmanı henüz önceden ayarları desteklemediğinden, **Siyah &amp; Beyaz Kızılötesi (RGB) Photoshop önceden ayarını yeniden oluşturacağız** (a). Ön ayar, bir çiçeklenen ağacın görüntüsüne (b) uygulanacaktır. Sonuç olarak, kızılötesi fotoğrafçılığı efektini elde etmek istiyoruz (c).

![Kanal Karıştırıcı Ayarlama Katmanı Örneği](channel-mixer-adjustment-psd-layer-figure-1.png) İlk olarak, Siyah &amp; Beyaz Kızılötesi (RGB) Photoshop önceden ayarlarını yeniden oluşturmak için monokrom bayrağını etkinleştirmek ve Gri çıktı kanalı için her renk için uygun ham değerleri ayarlamak gerekir:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

Kodun işlemesi için görüntünün RGB renk modunda olması gerekmektedir (RbgMixerChannel sınıfına dönüştürme nedeniyle). CMYK renk modu da desteklenmektedir ancak yalnızca ilgili renk moduna sahip görüntüler için.

Her bir rengin değeri ile Constant özelliğinin -200 ila 200 aralığında olması gerektiğini unutmayın.

## Sonuç

Bu makalede, Aspose.PSD'nin Java için Kanal Karıştırıcı API'sı ile renk kanallarındaki renkleri ayarlamayı ve görüntüyü siyah beyaza çevirmeyi ele aldık.

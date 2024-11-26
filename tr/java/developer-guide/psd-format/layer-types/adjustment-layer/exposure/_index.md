---
title: Pozlama Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/exposure/
---

# Java'da Photoshop Pozlama Ayarlama Katmanı ile Çalışmak

Bu makalede, Aspose.PSD for Java - PSD dosya biçimi işleme kütüphanesini kullanarak Adobe® Photoshop® belgesine Pozlama ayarlama katmanı ekleyeceğiz. Kütüphane, kendi görüntü işleme algoritmalarını kullandığı için yüklü Photoshop düzenleyicisi olmadan çalışır. Ayrıca, kütüphane pozlama ayarlama API'si ile ilgili bazı ayrıntıları da öğrendik.

## API Genel Bakış

Pozlama ayarlama katmanı, pozlama ayarları ile çalışmak için aşağıdaki özellikleri içeren [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) sınıfı aracılığıyla yapılandırılır:

- Bir fotoğrafın kaç ışık taşıdığını, tüm histogramı siyahlarla ilişkilendirerek sıkıştırarak veya uzatarak tanımlar. Bu nedenle öncelikle vurguları etkiler.
- Pozlama ofseti, gölgeleri daha çok etkiler.
- Gama düzeltmesi. Görüntü parlaklığını düzeltir.

## Doğru pozlama

Pozlamayı doğrulamak ve ilgili özellikleri değiştirmek, sınıfın birkaç özelliğini değiştirmek kadar basittir. Bir kütüphanenin bir kitaplığın alt pozlanmış fotoğrafına (b) insan gözüne algılanabilir hale getirmek için bazı pozlama ayarları (a) uygulayalım.

![Pozlama Ayarlama Katmanı Örneği](exposure-adjustment-layer-figure-1.png)

Tüm ayar, genellikle gama düzeltmesi kullanılarak yapılır. Bununla birlikte, pozlama ve ofset de biraz ayarlanır. Yapmanız gereken tek şey, zaten belirtilen özelliklere uygun değerler ayarlamaktır:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Pozlamanın -20,0 ila 20,0 aralığında, ofset değerinin -0,5 ila 0,5 aralığında olması ve gama düzeltilmesi değer aralığının 9,99 ila 0,01 arasında olması gerektiğine dikkat edin.

Daha fazla ayrıntı için [Pozlama ayarlama katmanı API referansına](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) başvurun.

## Sonuç

Bu makalede, bir PSD dosyasına Pozlama ayarlama katmanı eklemeyi ve görüntüyü aydınlatmayı öğrendik ve bazı API ayrıntılarını ele aldık.

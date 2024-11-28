---
title: Invert Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/invert/
---

# Java'da Photoshop Ters Çevirme Ayarlama Katmanı ile Çalışmak

Bu makalede, Java'da programlı olarak bir Photoshop belgesindeki görüntüyü negatif hale getirmenin nasıl yapılacağını göstereceğiz. Bu amaçla, Aspose.PSD for Java olarak adlandırılan PSD dosya biçimi manipülasyonu kütüphanesini kullanacağız.

Renk ters çevirme API'si, bir görüntüye **negatif bir etki eklemeyi** sağlar. Muhtemelen daha önce [Curves ayarlama katmanı kullanarak görüntü renklerini ters çevirme](/psd/tr/java/layer-types/adjustment-layer/curves/) işlemini nasıl gerçekleştireceğinizi görmüşsünüzdür. Ancak, bugün işi hızlı ve kolay bir şekilde yapabilmenin yollarından biri olan Invert ayarlama katmanını ele alacağız.

## API genel bakış

**Invert ayarlama katmanı API'si**, kendi başına bir katman sınıfı olan [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer) ile oluşur. Bu sınıf, kendi genel üyelerine sahip değildir çünkü üst sınıfından ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)) tüm genel üyeleri devralmaktadır. Bu durum, kullanımını basitleştirir çünkü yapmanız gereken tek şey bu katmanı bir PSD dosyasına eklemek ve görüntünün negatif hale gelmesini sağlamaktır.

## Görüntü renklerini ters çevirme

Bu nedenle, açık olmasa da netlik için bir astronotun (a) görüntüsü için negatif etki yapmak üzere **Invert ayarlama katmanını uygulamanın** nasıl olduğunu gösterelim.

![Ters Çevirme Ayarlama Katmanı Örneği Öncesinde ve Sonrasında](invert-adjustment-layer-figure-1.png)

Görüntünün renklerini **ters çevirmek** için, sadece bir Invert ayarlama katmanı PSD'ye ekleyin:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

Bu kadar! Bu tür ayarlama katmanı için yapılandırılması gereken özel özellikler bulunmamaktadır.

## Sonuç

Bu makalede, Aspose.PSD for Java'nın Invert ayarlama katmanı API'si hakkında öğrendik. Bu ayarlama katmanının API'sı herhangi bir genel üye bildirmediği için negatif görüntüler elde etmek için pratik bir araçtır.

---
title: Parlaklık Kontrast Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/brightness-contrast/
---

# Java'da Photoshop Parlaklık/Kontrast Ayarlama Katmanı ile Çalışmak

Bu makalede, Aspose.PSD for Java® kütüphanesini kullanarak Bir Adobe® Photoshop® belgesine Parlaklık/Kontrast ayarlaması uygulayacağız. Ayrıca, bu tür ayarlama katmanı ile ilgili kütüphane özelliklerini daha fazla öğreneceğiz.

Ancak önce biraz teori.

Parlaklık/Kontrast ayarlama katmanı, görüntünün parlaklık ve kontrastını değiştirir. Peki bu aslında ne anlama geliyor? Parlaklığı artırma, renk değerini beyaz'a kadar açıklar ve parlaklığı azaltma, renk değerini siyah'a kadar karartır. Kontrastı artırma ise açık ve koyu renkler arasındaki farkı artıracak ve kontrastı azaltma ise o farkı azaltacaktır; yani açık renkler daha açık ve koyu renkler daha koyu hale gelir.

## Renk modu desteği

Kütüphane, RGB, CMYK veya Lab renk modundaki görüntülere Parlaklık/Kontrast ayarlama katmanı eklemeye izin verir.

## Mevcut ve eski davranış

Mevcut kütüphane uygulaması (yazıldığı sırada v20.6) varsayılan Photoshop algoritmasını kullanır; gölgeden ışıklara kadar tam tonal aralığı korur ancak henüz eski davranışı desteklemez. Bu, kütüphanenin Parlaklık/Kontrast ayarlama katmanını (CS4 ve daha yeni) en son Photoshop sürümlerinde yapılmış belgelerde desteklediği anlamına gelir. Ancak, ihtiyacınız varsa Parlaklık/Kontrast ayarlama katmanının eski uygulamasını [forumumuzda isteyebilirsiniz](https://forum.aspose.com/c/psd).

## Parlaklık ve kontrastı ayarlayın

Şimdi, Parlaklık/Kontrast ayarlama katmanı yüksek seviye API'sının nasıl çalıştığını açıklayalım (ilere bakarsak, API açıktır). PsdImage sınıfı, ParlaklıkKontrastKatmanı sınıfına erişim sağlayan parlaklık ve kontrast ayarlaması için bir fabrika yöntemi (addBrightnessContrastAdjustmentLayer) içerir. ParlaklıkKontrastKatmanı sınıfı, parlaklık ve kontrast özelliklerine erişmek için bir çift getirici ve ayarlayıcı içerir ve değerlerini değiştirmek için kullanılır.

![|PSD'de Parlaklık/Kontrast Ayarlama Katmanı Örneği](brightness-contrast-psd-adjustment-layer-figure-1.png)

Yani, sadece fabrika yöntemiyle uygun argümanlarla bir köpek resminin parlaklığını1 ve kontrastını2 ayarlamak için bir örnek resme (c) ulaşmak için:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Notlar:

1. Parlaklık değeri -150 ila 150 aralığında olmalıdır.
2. Kontrast değeri -50 ila 100 aralığında olmalıdır.

Daha fazla ayrıntı için [ParlaklıkKontrastKatmanı](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) belgelendirme sayfasına bakınız.

## Sonuç

Bu makalede, Parlaklık/Kontrast ayarlama katmanı hakkında kısa bir genel bakış yaptık ve fabrika yöntemiyle görüntünün parlaklık ve kontrastını nasıl ayarlayacağımızı öğrendik.

Daha fazla bilgi edinmek için Aspose.PSD for Java'da [ayar katmanı API'lerine ilişkin makale serimize](/tr/java/layer-types/adjustment-layer/) başvurun.

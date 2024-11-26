---
title: Java Fotoğraf Filtresi Ayarlama Katmanı
type: docs
weight: 30
url: /tr/java/layer-types/adjustment-layer/photo-filter/
---

# Java'da Photoshop Fotoğraf Filtresi Ayarlama Katmanı ile Çalışmak

Bugün, Aspose.PSD for Java kullanarak var olan bir Photoshop belgesine Fotoğraf Filtresi ayarlama katmanı nasıl uygulanır göreceğiz. Bu kütüphane, PSD dosya biçimini manipüle etmek için kullanılan bir kütüphanedir.

**Fotoğraf Filtresi ayarlama katmanı API'si**, renk dengelemesini renklendirme kullanarak değiştirir. Sonuçta elde edilen görüntü, gerçek bir kamera filtresi kullanıldıktan sonra aynı görünecektir. Kütüphanenin Fotoğraf Filtresi ayarlama katmanı API'si, henüz önceden tanımlanmış filtreler olmadığı için Photoshop'tan biraz farklılık gösterir. Ancak diğer tüm yöntemlerde aynıdır. Bu durum, bir renk belirleyebileceğiniz, yoğunluğunu değiştirebileceğiniz ve Işığın Korunumu seçeneğini kullanabileceğiniz anlamına gelir.

## API genel bakış

Fotoğraf Filtresi ayarlama katmanı API'si oldukça basit bir şekilde kullanılır. Bu ayarlama katmanına giriş noktası olan ve sadece renk, yoğunluk ve ışığın korunmasını içeren üç genel özelliğe sahip olan ana [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) sınıfı bulunur.

## Renk dengesini ayarlayın

Çok fazla konuşacak bir şey olmadığından, hemen Fotoğraf Filtresi kullanarak **renk dengesi ayarlama örneğini** düşünelim. Bir geyik heykeli resmi için daha sıcak tonlar elde etmek amacıyla bir ısıtma filtresi (a) manuel olarak ekleyeceğiz ki (b) daha hoş görünümlü olan (c) bir görüntü elde edelim.

![Fotoğraf Filtresi Ayarlama Katmanı Örneği](photo-filter-adjustment-layer-figure-1.png)

Öncelikle, yüklü Photoshop belgesine Fotoğraf Filtresi ayarlama katmanı eklemek için [fabrika yönteminin](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) diğer ayarlama katmanları için olanlardan farklı olduğunu fark edin çünkü varsayılan yöntem (bağımsız değişken olmadan) yoktur. Dolayısıyla, ısıtıcı filtre etkisini yeniden oluşturmak için fabrika yöntemine tek bir argüman gereklidir, yani [renk](https://reference.aspose.com/psd/java/com.aspose.psd/Color) olarak turuncu rengi aktarın, ardından uygun setter'ları kullanarak yoğunluğu ayarlayın:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Dikkate değer bir husus, Yoğunluk özelliğinin varsayılan değeri olan 100'dür ve Işığın Korunması özelliği için doğru varsayılan değerdir (bu nedenle bu seçeneği açıkça etkinleştirmiyoruz).

## Sonuç

Bu makalede, Aspose.PSD for Java'nın Fotoğraf Filtresi ayarlama katmanı API'sinin kullanımını ele aldık. Bu araç kullanımı kolaydır ve değişken yoğunluğa sahip bir görüntüye bir renk eklemeyi sağlar. Tüm görüntünün renk dengesini hızlı bir şekilde ayarlamak için hızlı bir yoldur.

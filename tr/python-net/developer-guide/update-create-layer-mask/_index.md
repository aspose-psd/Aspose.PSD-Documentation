---
title: Aspose.PSD için Python'da maskelerle çalışma
weight: 100
type: docs
description: PSD Dosyası içinde Kırpma, Raster ve Vektör Maskeleri ile nasıl çalışılacağına dair örnekler
keywords: [maskeler, katman maskesi, vektör maske, kırpma maske, psd, psd api, python, kod örneği]
url: /tr/python-net/guncelle-olustur-katman-masksi/
---

## **Genel Bakış**

**Genel Bakış**

    PSD dosyalarında 3 tür maske bulunur:
    1. Kırpma Maskeleri
    2. Raster Maskeleri
    3. Vektör Maskeleri
    
    Bu makale tüm 3 türü ele almaktadır.


**Kırpma Maskeleri**

Kırpma maskeleri, grafik tasarımı ve görüntü düzenleme yazılımlarında güçlü bir özelliktir. Başka bir katmanın şekline ve içeriğine bağlı olarak bir katmanın görünürlüğünü kontrol etmenizi sağlar. Diğer bir deyişle, bir kırpma maskesi, bir katmanın görünürlüğünü yalnızca altındaki başka bir katmanın şekliyle sınırlandırır.

Bir kırpma maskesi oluşturmak için öncelikle iki katmana ihtiyacınız vardır: ana katman ve kırpılmasını istediğiniz katman. Ana katman, görünür olacak şekli veya alanı tanımlar, kırpılmasını istediğiniz katman ise bu şekle kırpılacak içeriği içerir.

Bir kırpma maskesi uyguladığınızda, kırpılan katmanın içeriği yalnızca ana katmanın sınırları içinde görünür. Ana katmanın sınırları dışındaki herhangi bir içerik gizlenir veya kırpılır.

Kırpma maskeleri, belirli bir görüntü veya tasarım alanına bir efekt uygulamak istediğinizde özellikle kullanışlıdır. Bir kırpma maskesi kullanarak, etkiyi görüntünün geri kalanını etkilemeden istenen alana sınırlayabilirsiniz.

Lütfen sayfanın sonundaki örneği kontrol edin

**Raster Maskeleri**

PSD dosyalarındaki raster maskeler, bir katmanın belirli alanlarının görünürlüğünü kontrol etmek için kullanılır. Vektör maskelerin aksine, maskelenmiş alanları tanımlamak için matematiksel şekiller kullanan vektör maskelerin aksine, raster maskeler piksel tabanlı bilgi kullanarak bir katmandaki hangi kısımların görünür veya gizli olduğunu belirler.

Bir raster maskesi, bir katmana uygulanan bir gri tonlama içerir. Maskenin beyaz alanları görünür bölümleri temsil ederken, siyah alanlar gizli bölümleri temsil eder. Aradaki gri tonlar kısmi şeffaflık veya kısmen görünür alanlar oluşturmak için kullanılabilir.

Lütfen sayfanın sonundaki örneği kontrol edin

**Vektör Maskeleri**

PSD dosyalarındaki vektör maskeleri, matematiksel şekillere dayalı belirli alanların görünürlüğünü tanımlamak için kullanılan esnek bir araçtır. Piksel tabanlı bilgi kullanan raster maskelerin aksine, vektör maskeler yol ve eğrileri kullanarak sorunsuz ve ölçeklenebilir maskeli alanlar oluşturur.

Bir vektör maskesi, bir katmana uygulanan bir yolun temelinde bir maske şeklidir. Yolun şekli, katmandaki görünür ve gizli bölümleri belirler. Yolun kontrol noktaları ve eğrilerini manipüle ederek, hassas ve karmaşık maskeli alanlar oluşturabilirsiniz.

Lütfen vektör maskelerinin nasıl eklenebileceği hakkında bilgi almak için [Vektör Maskeleri sayfasını](psd/tr/net/layer-vector-mask/) kontrol edin.


## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Dokümantasyon-Python-Aspose-psd-guncelle-olustur-katman-masksi.py" >}}

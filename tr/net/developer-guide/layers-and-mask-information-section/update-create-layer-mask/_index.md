---
title: Aspose.PSD ile maskelerle çalışma
weight: 100
type: docs
description: PSD Dosyası içinde Kırpma, Raster ve Vektör Maskeleri nasıl kullanılacağına dair örnekler
keywords: [maskeler, katman maskesi, vektör maske, kırpma maskesi, psd, psd api, C#, csharp, kod örneği]
url: tr/net/update-create-layer-mask/
---

## Genel Bakış

PSD dosyalarında üç tür maske bulunmaktadır:
1. Kırpma Maskeleri
2. Raster Maskeler
3. Vektör Maskeler

Bu makale üç türü de ele almaktadır.

### Kırpma Maskeleri

Kırpma maskeleri, grafik tasarım ve resim düzenleme yazılımlarında görünürlüğü başka bir katmandaki şekil ve içeriğe bağlı olarak kontrol etmenizi sağlayan güçlü bir özelliktir. Temelde, bir kırpma maskesi, bir katmanın görünürlüğünü başka bir katmanın altında tanımlanan şekille sınırlar.

Bir kırpma maskesi oluşturmak için iki katmana ihtiyacınız vardır: temel katman ve kırpma katmanı. Temel katman, görünür alanı tanımlar iken, kırpma katmanı, temel katmanın şekline sıkıştırılacak içeriği içerir.

Bir kırpma maskesi uyguladığınızda, kırpma katmanının içeriği, yalnızca temel katmanın sınırları içinde görünür hale gelir. Temel katmanın sınırlarının dışındaki içerik gizlenir veya kırpılır.

Kırpma maskeleri, özellikle belirli bir görüntü veya sanat eserinin belirli alanlarına dokular veya desenler gibi etkiler uygulamak için kullanışlıdır. Bir kırpma maskesi kullanarak, etkinin görüntünün geri kalanını etkilemeden istenen alanla sınırlı olduğundan emin olabilirsiniz.

### Raster Maskeler

PSD dosyalarında raster maskeler, bir katman içinde belirli alanların görünürlüğünü kontrol etmek için gereklidir. Vektör maskelerin aksine, piksel tabanlı bilgi kullanarak bir katmanın hangi kısımlarının görünür veya gizli olduğunu belirleyen raster maskeler kullanır.

Bir raster maskesi, bir katmana uygulanan bir tonlamalı görüntüden oluşur. Maskenin beyaz bölgeleri görünür bölümleri temsil ederken, siyah bölgeler gizli bölümleri temsil eder. Gri tonlar arasındaki alanlar kısmi şeffaflık veya yarı görünür alanlar oluşturur.

Raster maskeleri kullanarak karmaşık maskeleme efektleri elde edebilir, piksel düzeyinde ayrıntılara dayalı olarak katman görünürlüğü üzerinde hassas kontrol sağlayabilirsiniz. Bu özellik özellikle ayrıntılı düzenleme ve karışım gerektiren görevler için kullanışlıdır.

### Vektör Maskeler

PSD dosyalarındaki vektör maskeler, matematiksel şekillere dayalı olarak bir katman içinde belirli alanların görünürlüğünü tanımlamak için kullanılan çok yönlü bir araçtır. Piksel tabanlı bilgi kullanan raster maskelerin aksine, vektör maskeler yolları ve eğrileri kullanarak düzgün ve ölçeklenebilir maskeleme alanları oluşturur.

Bir vektör maske temelde bir katmana uygulanan bir yoldur. Yolun şekli, katmanın hangi bölümlerinin görünür ve hangilerinin gizli olduğunu belirler. Yolu kontrol noktalarını ve eğrilerini manipüle ederek, kesin ve karmaşık maskeleme alanları oluşturabilirsiniz.

Vektör maskeler, kayıpsız kalite kaybı olmadan kolayca ayarlanabilen temiz, ölçeklenebilir maskeler oluşturmak için özellikle kullanışlıdır. Bu özellik, bir katman içinde görünür alanları tanımlarken yüksek hassasiyet ve esneklik gerektiren görevler için idealdir.

Daha fazla bilgi için vektör maskeler eklemek ziyaret edin, lütfen [Vektör Maskeler sayfasına](psd/tr/layer-vector-mask/) gidin.

## Örnek
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Daha detaylı bilgi ve örnekler için, lütfen [Aspose.PSD için C# belgelerine](https://docs.aspose.com/psd/tr/) gidin.

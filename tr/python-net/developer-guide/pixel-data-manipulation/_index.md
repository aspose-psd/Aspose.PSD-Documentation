---
title: Pixel Verilerinin Aspose.PSD Kullanarak Python İle Manipülasyonu
weight: 100
type: docs
description: PSD Python API kullanarak ham piksel verilerini doğrudan ve hızlı bir şekilde güncelleme örneği
keywords: [pikselleri düzenleme, psd düzenleme, katman düzenleme, ham veri manipülasyonu, psd verisi düzenleme, psd api, python, kod örneği]
url: tr/python-net/pixel-verileri-manipulasyonu/
---

## **Giriş**
Aspose.PSD Adobe Photoshop dosyaları (PSD) ile çalışmanıza izin veren güçlü bir kütüphanedir. Bu makalede, Aspose.PSD kullanarak bir PSD dosyasındaki piksel verilerini nasıl manipüle edeceğimizi keşfedeceğiz.

## **Genel Bakış**
Sağlanan kod, bir PSD dosyası oluşturmayı, onun için yeni bir katman eklemeyi ve ardından piksel verilerini doğrudan manipüle etmeyi ve değiştirilmiş resmi kaydetmeyi nasıl gösterdiğini göstermektedir.

Gerekli Modülleri İçe Aktarma: İlk adım olarak gerekli modülleri içe aktarmaktır. Gerekli modülleri io kütüphanesinden BytesIO modülünü ve aspose.psd.fileformats.psd ve aspose.psd.fileformats.psd.layers modüllerinden PsdImage ve Layer sınıflarını içe aktarırız.

Daha sonra, giriş ve çıkış dosya yollarını tanımlarız.

Giriş Dosyasını Bir Akım Olarak Açma: "rb" modunu kullanarak giriş dosyasını bir akım olarak açarız. Arabellek argümanını devre dışı bırakmak için buffering argümanını 0 olarak ayarlarız. Dosya içeriği BytesIO akışına okunur ve akış stream.seek(0) ile başlangıca ayarlanır.

Bir PSD katmanı nesnesi oluştururuz ve bu katmanı Layer sınıf yapıcısına ileterek akışı geçiririz.

PsdImage sınıf yapıcısını kullanarak yeni bir PSD görüntüsü oluştururuz ve katmanın genişliği ve yüksekliğini argüman olarak veririz.

Katmanı, atama operatörü (=) kullanarak PSD görüntüsünün layers özelliğine atarız.

Piksel verilerini manipüle etmek için, ilk olarak ARGB32 piksellerini katmandan load_argb_32_pixels yöntemini kullanarak yükleriz. Sonucu pikseline depolarız.

Daha sonra, pikseller dizisinin uzunluğuna dayalı bir endeks aralığı (pixelsRange) tanımlarız. Endeksler üzerinde döneriz ve bir endeksin 5'e bölünebilir olup olmadığını kontrol ederiz. Eğer öyleyse, o endeksteki piksel değerini 500000 olarak ayarlarız. Yani, yalnızca tekrar eden bir desen oluşturmak istiyoruz. Pikselleri istediğiniz şekilde değiştirebilirsiniz.

Sonra, değiştirilmiş piksel verilerini save_argb_32_pixels yöntemini kullanarak tekrar katmana kaydederiz.

Son olarak, PSD görüntüsünü kaydederek değiştirilmiş görüntüyü çıkış dosyasına kaydederiz.

Bu makalede, Aspose.PSD kullanarak Python'da bir PSD dosyasındaki piksel verilerini manipüle etmenin nasıl yapıldığını inceledik. Sağlanan kodu anlayarak, belirli koşullara dayalı olarak pikselleri değiştirme gibi çeşitli piksel düzeyi işlemleri yapabilirsiniz. Aspose.PSD, PSD dosyalarıyla programatik olarak çalışmak için kapsamlı bir özellik seti sunar, bu da Python'da görüntü manipülasyon görevleri için değerli bir araç yapmaktadir.

Lütfen sağlanan kodun, Aspose.PSD kütüphanesini ve bağımlılıklarını kurduğunuz varsayıldığını unutmayın. Aspose.PSD'nin Python için nasıl kurulacağı ve kullanılacağı hakkında daha fazla bilgiyi resmi belgelerde bulabilirsiniz.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Belgeleme-Python-Aspose-pixel-veri-manipulasyonu.py" >}}

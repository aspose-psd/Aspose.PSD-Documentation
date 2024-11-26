---
title: Pixel Verilerinin Aspose.PSD Kullanarak Manipülasyonu C# için
weight: 100
type: docs
description: Aspose.PSD'yi kullanarak PSD C# API'sını kullanarak doğrudan ve hızlı bir şekilde ham piksel verilerini güncelleme örneği
keywords: [pikselleri düzenle, psd düzenle, katmanı düzenle, ham veri manipülasyonu, psd verisini düzenle, psd api, C#, csharp, kod örneği]
url: tr/net/pixel-data-manipulation/
---

## Tanıtım

Aspose.PSD, Adobe Photoshop dosyaları (PSD) ile C# dilinde çalışmanıza olanak sağlayan güçlü bir kütüphanedir. Bu makalede, Aspose.PSD'yi kullanarak bir PSD dosyasındaki piksel verilerini nasıl manipüle edebileceğimizi keşfedeceğiz.

## Genel Bakış

Sağlanan kod, bir PSD dosyası oluşturmayı, yeni bir katman eklemeyi, piksel verilerini doğrudan manipüle etmeyi ve değiştirilmiş resmi kaydetmeyi nasıl gösterdiği konusunda bilgi verir.

### Piksel Verilerini Manipüle Etmek İçin Adımlar

1. **Gerekli Modülleri İçe Aktarma**:
   Gerekli modülleri içe aktarın. Aspose.PSD kütüphanesinden `PsdImage` ve `Layer` sınıflarını içe aktarmanız gerekmektedir.

2. **Giriş ve Çıkış Dosya Yollarını Tanımlama**:
   Giriş ve çıkış dosya yollarını belirtin.

3. **Giriş Dosyasını Akış Olarak Açma**:
   Okuma modunda `FileStream` sınıfını kullanarak giriş dosyasını bir akış olarak açın. Akışı yükleyerek bir `PsdImage` nesnesi oluşturun.

4. **Yeni Bir PSD Görüntüsü Oluşturma**:
   `PsdImage` kurucusunu kullanarak ve katmanın genişliği ve yüksekliğini argümanlar olarak sağlayarak yeni bir PSD görüntüsü oluşturun.

5. **Katmanı PSD Görüntüsüne Atama**:
   Katmanı PSD görüntüsünün `Layers` özelliğine atayın.

6. **Piksel Verilerini Manipüle Etmek**:
   Katmandan ARGB32 piksellerini `LoadArgb32Pixels` yöntemini kullanarak yükleyin. Pikseller dizisinin uzunluğuna dayalı bir indeks aralığı tanımlayın ve gerektiğinde piksel değerlerini değiştirin.

7. **Değiştirilmiş Piksel Verilerini Kaydetme**:
   Değiştirilmiş piksel verilerini `SaveArgb32Pixels` yöntemini kullanarak geri katmana kaydedin.

8. **PSD Görüntüsünü Kaydetme**:
   PSD görüntüsünü `Save` yöntemini kullanarak çıkış dosyasına kaydedin.

### Örnek

Aşağıda, Aspose.PSD'yi kullanarak C# için piksel verilerini nasıl manipüle edeceğinizi gösteren bir kod örneği bulunmaktadır:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### Özet

Aspose.PSD, PSD dosyalarındaki piksel verilerini manipüle etmek için güçlü bir özellik seti sunar. Belirli koşullara dayalı olarak pikselleri değiştirmeniz gerekiyorsa veya karmaşık desenler oluşturmanız gerekiyorsa, Aspose.PSD bu görevleri kolay ve verimli hale getirir.

Daha detaylı bilgi ve örnekler için lütfen [Aspose.PSD için C# belgelerine](https://docs.aspose.com/psd/net/) ziyaret edin.

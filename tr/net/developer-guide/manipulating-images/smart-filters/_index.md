---
title: С# için Aspose.PSD'de Akıllı Filtreleri Manipüle Etme
weight: 100
type: docs
description: PSD Dosyasında Akıllı Filtreleri Kullanım Örnekleri
keywords: [akıllı filtre, gürültü ekleme, gauss bulanıklığı, keskin, filtre, psd filtresi, psd api, C#, csharp, kod örneği]
url: tr/net/akilli-filtreler/
---

## Genel Bakış

Aspose.PSD'de C# için akıllı filtreleri uygulamanın üç yolu vardır.

### Doğrudan Filtre Uygulama

Bu örnek, Aspose.PSD'de C# için akıllı filtreleri doğrudan nasıl uygulayacağınızı gösterir.

İlk olarak, kaynak PSD dosyasını, orijinal görüntü için çıktı dosyasını ve güncellenmiş görüntü için çıktı dosyasını belirtin.

Daha sonra, PSD görüntüsünü `Image.Load` yöntemini kullanarak yükleyin ve bir `PsdImage` nesnesine dönüştürün.

Orijinal görüntüyü, belirtilen çıktı dosya adıyla kaydedin.

Uygulanacak akıllı filtreyi temsil eden bir `SharpenSmartFilter` nesnesi oluşturun.

PSD görüntüsünden düzenli katmanı `psdImage.Layers[1]` kullanarak alın.

Düzenli katmana `sharpenFilter`'ı bir döngü içinde üç kez uygulayın.

Son olarak, güncellenmiş görüntüyü, belirtilen çıktı dosya adıyla kaydedin.

Bu kod, Aspose.PSD'de C# için akıllı filtreleri doğrudan uygulamanın nasıl yapıldığını gösterir. Uygun filtre nesnelerini kullanarak ve bunları istenen katmanlara uygulayarak görüntülerinizde istediğiniz efektleri elde edebilirsiniz.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Akıllı Filtreleri Akıllı Nesneler İçinde Manipüle Etme

Bu örnek, akıllı nesneler içinde akıllı filtreleri nasıl manipüle edeceğinizi gösterir.

İlk olarak, kaynak PSD dosyasını, orijinal görüntü için çıktı dosyasını ve güncellenmiş görüntü için çıktı dosyasını belirtin.

PSD görüntüsünü `Image.Load` yöntemini kullanarak yükleyin ve bir `PsdImage` nesnesine dönüştürün.

Orijinal görüntüyü, belirtilen çıktı dosya adıyla kaydedin.

PSD görüntüsünün ikinci katmanını bir `SmartObjectLayer` nesnesine dönüştürün.

Akıllı filtreleri düzenleyin. Bu örnek, `GaussianBlurSmartFilter` ve `AddNoiseSmartFilter` ile çalışmayı gösterir.

`GaussianBlurSmartFilter` için, yarıçap, karışım modu, opaklık ve etkin durum dahil filtreyi güncelleyin.

`AddNoiseSmartFilter` için, gürültü dağılımını `NoiseDistribution.UNIFORM` olarak ayarlayın.

Akıllı nesne katmanına yeni filtre öğeleri ekleyin: başka bir `GaussianBlurSmartFilter` ve `AddNoiseSmartFilter`.

Değişiklikleri `UpdateResourceValues` yöntemini kullanarak uygulayın.

Filtreleri, doğrudan katmana ve katman maskesine `Apply` ve sırasıyla `ApplyToMask` yöntemlerini kullanarak uygulayın.

Güncellenmiş görüntüyü, belirtilen çıktı dosya adıyla kaydedin.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Katman Maskesine Akıllı Filtreler Uygulama

Akıllı filtreler, çeşitli filtreleri ve efektleri uygulamak için kullanıcıların güçlü bir görüntü düzenleme aracıdır. Bu araçlardan biri, filtreleri maskelere uygulamaktır ve bu, filtrenin etkilediği alanları hassas bir şekilde kontrol etmeyi sağlar.

Bir maske, belirli görüntü alanlarının şeffaflığını belirleyen, filtreleri, ayarları veya efektleri seçici olarak uygulayan bir gri tonlu bir görüntüdür.

Maskelere akıllı filtreler uygulanırken, filtreler sadece maskenin belirtilen alanlarına uygulanır. Bu hassas kontrol, filtre yoğunluğunun ve kapsamının manipülasyonuna olanak tanır.

Daha ayrıntılı bilgi ve örnekler için [Aspose.PSD için C# belgelerine](https://docs.aspose.com/psd/net/) başvurun.

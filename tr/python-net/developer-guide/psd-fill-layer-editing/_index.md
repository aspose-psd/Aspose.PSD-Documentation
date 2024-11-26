---
title: Python ile PSD Dolgu Katmanı Güncelleme
weight: 100
type: docs
description: Renk Dolgu, Gradyan Dolgu ve Desen Dolgu dahil tüm ayar katmanı türlerini kullanma örnekleri
keywords: [dolgu katmanı, Renk Dolgu, Gradyan Dolgu, Desen Dolgu, psd api, python, kod örneği]
url: tr/python-net/psd-dolgu-katmani-duzenleme/
---

## **Genel Bakış**

Düzenli bir katman oluşturmak için, katmanın konumunu ve boyutunu tanımlamak için sol, üst, genişlik ve yükseklik parametrelerini kullanan sağlanan kod içindeki create_regular_layer fonksiyonunu kullanabilirsiniz. Yeni bir katman oluşturur, sınırlarını ayarlar ve belirtilen renkle doldurur.

Renk dolgu katmanı oluşturmak için, FillType.COLOR parametresi ile FillLayer.create_instance yöntemini kullanabilirsiniz. Dolgu katmanını oluşturduktan sonra, doldurma ayarlarına fill_settings özelliği üzerinden erişebilir ve ColorFillSettings sınıfının color özelliğini kullanarak rengi ayarlayabilirsiniz. Sağlanan kodda renk Color.coral olarak ayarlanmıştır. Dolgu katmanının clipping özelliği 1 olarak ayarlanmıştır; bu, katmanın kırpma maskesi olarak hareket etmesini sağlar.

Gradyan dolgu katmanı oluşturmak için, FillType.GRADIENT parametresi ile FillLayer.create_instance yöntemini kullanabilirsiniz. Renk dolgu katmanına benzer şekilde, doldurma ayarlarına fill_settings özelliği üzerinden erişebilir ve gradyan renk noktalarını ve şeffaflık noktalarını ayarlayabilirsiniz. Sağlanan kodda, gradyan renk noktaları GradientColorPoint sınıfı kullanılarak tanımlanır ve şeffaflık noktaları GradientTransparencyPoint sınıfı kullanılarak tanımlanır. Dolgu katmanının clipping özelliği de 1 olarak ayarlanır.

Desen dolgu katmanı oluşturmak için, FillType.PATTERN parametresi ile FillLayer.create_instance yöntemini kullanabilirsiniz. Yine, doldurma ayarlarına fill_settings özelliği üzerinden erişebilir ve desen verisini ve diğer özellikleri ayarlayabilirsiniz. Sağlanan kodda, desen verisi PatternFillSettings sınıfı kullanılarak tanımlanır ve kırpma özelliği 1 olarak ayarlanır.

Dolgu katmanlarını oluşturduktan sonra, add_layer yöntemini kullanarak onları PSD görüntüsüne ekleyebilirsiniz. Ayrıca, her dolgu katmanı için görüntü adı ve diğer özellikleri de belirtebilirsiniz.

Son olarak, sağlanan kodu kullanarak PSD görüntüsünü ve karşılık gelen PNG görüntüsünü kaydedebilirsiniz. PNG seçenekleri, şeffaflık için alpha ile truecolor kullanacak şekilde ayarlanmıştır.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Belgeleme-Python-Aspose-psd-dolgu-katmani-duzenleme.py" >}}

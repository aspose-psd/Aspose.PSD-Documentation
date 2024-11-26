---
title: Java ile PSD Dolgu Katmanı Güncelleme
weight: 100
type: docs
description: Renk Doldurma, Gradyan Doldurma ve Desen Doldurma dahil olmak üzere tüm ayar katmanı tiplerinin kullanım örnekleri
keywords: [dolgu katmanı, Renk Doldurma, Gradyan Doldurma, Desen Doldurma, psd api, java, kod örneği]
url: tr/java/psd-dolgu-katmani-duzenleme/
---

## **Genel Bakış**

Normal bir katman oluşturmak, katmanın konumunu ve boyutunu tanımlayan parametrelere ihtiyaç duyan createRegularLayer işlevinin kullanılmasını gerektirir. Bu işlev yeni bir katman oluşturur, sınırlarını belirler ve belirli bir renk ile doldurur.

Renk doldurma katmanı için, FillType.Color parametresiyle FillLayer.createInstance yöntemini kullanırsınız. Doldurma katmanı oluşturulduktan sonra, fill_settings özelliğine erişilir ve ColorFillSettings sınıfının color özelliğini kullanarak istenilen rengi ayarlarsınız. Bu bağlamda, renk Color.getCoral()'a ayarlanmıştır. Ayrıca, doldurma katmanının clipping özelliği 1 olarak ayarlanmıştır, böylece bir klipleme maskesi olarak işlev görür.

Gradyan doldurma katmanları, FillType.Gradient parametresiyle aynı şekilde oluşturulur FillLayer.create_instance yöntemi kullanılarak oluşturulur. Renk doldurma katmanları gibi, fill_settings üzerinden doldurma ayarlarına erişir ve gradyan renk noktalarını ve saydamlık noktalarını ayarlarsınız. Bu örnekte, gradyan renk noktaları GradientColorPoint sınıfı ile tanımlanır ve saydamlık noktaları GradientTransparencyPoint sınıfı ile belirlenir. Doldurma katmanının klip özelliği de 1 olarak ayarlanmıştır.

Desen doldurma katmanları, FillType.Pattern parametresiyle FillLayer.createInstance kullanılarak oluşturulur. Tekrar, fill_settings üzerinden doldurma ayarlarına erişilir ve desen verileri ve diğer özellikler ayarlanır. Bu kodda, desen verisi PatternFillSettings sınıfı kullanılarak tanımlanır ve klip özelliği 1 olarak ayarlanır.

Doldurma katmanları oluşturulduktan sonra, her doldurma katmanı için görüntü adını ve diğer özelliklerini belirterek addLayer yöntemi kullanılarak PSD görüntüsüne eklenir.

Son olarak, PSD görüntüsü ve ilgili PNG görüntüsü kaydedilir. PNG seçenekleri, saydamlık için ALPHA ile gerçek renk kullanacak şekilde yapılandırılmıştır.

Daha fazla ayrıntı için tam örneğe başvurun.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Belgeleme-Java-Aspose-psd-dolgu-katmani-duzenleme.java" >}}

---
title: Renk Katmanlarının Desteği
type: docs
weight: 50
url: /tr/java/renk-katmanlarinin-destegi/
---


## **Renk Doldurmalı Katmanların Desteği**
Bu makale, PSD katmanını Renk ile doldurmanın nasıl yapılacağını göstermektedir. Lütfen Renk katmanı eklemek için Aspose.PSD.FileFormats.Psd.Layers.FillLayer'ı kullanın. Aşağıdaki kod parçaları bir PSD dosyası yükler, FillLayer sınıfına erişir ve rengi FillLayer.FillSettings özelliğini kullanarak ayarlar.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Renk Geçişli Doldurmaların Desteği**
Bu makale, PSD katmanını doldurmak için Renk geçişini kullanmanın nasıl yapıldığını göstermektedir. Aspose.PSD API'leri, bu hedefe ulaşmak için verimli ve kullanımı kolay yöntemler sunmaktadır. Aspose.PSD, GradientColorPoint ve GradientTransparencyPoint sınıflarını bir katmana Gradient efekti eklemek için açıklamıştır.

PSD katmanını Gradient doldurmak için adımlar aşağıdaki gibidir:

- Resim sınıfı tarafından sağlanan fabrika yöntemi Load kullanarak bir PSD dosyasını yükleyin.
- FillLayer nesnesinin ayarlar özelliklerini ayarlayın.
- Gerekli renkleri ve renk konumunu içeren bir ColorPoint'ler listesi oluşturun.
- Gerekli opaklık ve opaklık noktası konumunu içeren bir transparencyPoints listesi oluşturun.
- FillLayer.Update yöntemini çağırın.
- Sonuçları kaydedin.

Aşağıdaki kod parçacığı, PSD katmanına Gradient doldurma eklemeyi nasıl yapacağınızı gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Renk Dolumu ile Çizgi Efekti**
Bu makale, renk dolumu ile çizgi efektinin nasıl yapılacağını göstermektedir. Stroke efekti, katmanlara ve şekillere vuruşlar ve sınırlar eklemek için kullanılır. Tek renkli çizgiler, renkli geçişler ve desenli sınırlar oluşturmak için kullanılabilir.

Renk dolumu ile Stroke efekti oluşturmanın adımları aşağıdaki gibidir:

- **LoadEffectsResource** özelliğini ayarlayın.
- PsdLoadOptions'i tanımlayarak, Image sınıfı tarafından sağlanan Load fabrika yöntemini kullanarak bir PSD dosyasını yükleyin.
- **ColorFillSetting** özelliklerini ayarlayın.
- Sonuçları kaydedin.

Aşağıdaki kod parçacığı, renk dolumu ile Stroke efektini nasıl oluşturacağınızı gösterir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




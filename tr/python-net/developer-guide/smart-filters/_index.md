---
title: Aspose.PSD for Python'da Akıllı Filtre Manipülasyonu
weight: 100
type: docs
description: PSD Dosyasında Akıllı Filtrelerin Nasıl Kullanılacağı ile İlgili Örnekler
keywords: [akıllı filtre, gürültü ekleme, gauss bulanıklığı, keskinleştirme, filtre, psd filtresi, psd api, python, kod örneği]
url: tr/python-net/akilli-filtreler/
---

## **Genel Bakış**

Aspose.PSD for Python'da akıllı filtreler uygulamanın 3 farklı yolu bulunmaktadır.

## **Doğrudan Filtre Uygulama**
Bu kod örneğinde, Aspose.PSD for Python'da akıllı filtreleri doğrudan nasıl uygulayacağımızı görebiliriz.

İlk olarak, kod kaynak PSD dosyasını, orijinal görüntü için çıkış dosyasını ve güncellenmiş görüntü için çıkış dosyasını belirtmektedir.

Ardından, kod Image.load() yöntemini kullanarak PSD görüntüsünü yükler ve PsdImage nesnesine dönüştürür.

Orijinal görüntü, çıkış dosya adı belirtilerek kaydedilir.

Uygulanacak akıllı filtreyi temsil eden SharpenSmartFilter nesnesi oluşturulur.

Kod daha sonra genel katmanı im.layers[1] kullanarak PSD görüntüsünden alır.

Bir döngü, keskinleştirme filtresinin genel katmana üç kez uygulanmasını sağlar.

Son olarak, güncellenmiş görüntü, kaydedilerek çıkış dosya adı belirtilir. 

Bu kod, Aspose.PSD for Python'da akıllı filtreleri doğrudan nasıl uygulayacağınızı göstermektedir. Uygun filtre nesnelerini kullanarak ve bunları istenen katmanlara uygulayarak görüntüleriniz üzerinde istediğiniz etkileri elde edebilirsiniz.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Belgeleme-Python-Aspose-psd-akilli-filtre-dogrudan-uygula.py" >}}

## **Akıllı Filtreleri Akıllı Nesnelere Uygulama**

İlk olarak, kod kaynak PSD dosyasını, orijinal görüntü için çıkış dosyasını ve güncellenmiş görüntü için çıkış dosyasını belirtmektedir.

PSD görüntüsü, Image.load() yöntemi kullanılarak yüklenir ve ardından PsdImage nesnesine dönüştürülür.

Orijinal görüntü, çıkış dosya adı belirtilerek kaydedilir.

Kod daha sonra PSD görüntüsündeki ikinci katmanı SmartObjectLayer nesnesine dönüştürür, akıllı nesne katmanını temsil eder.

Kod ardından akıllı filtreleri düzenlemeye devam eder. Bu örnekte, GaussianBlurSmartFilter ve AddNoiseSmartFilter olmak üzere iki tür akıllı filtreyle çalışmayı gösterir.

GaussianBlurSmartFilter için, kod yarıçapı, karışım modu, opaklık ve etkin olup olmadığı dahil olmak üzere filtre değerlerini günceller.

AddNoiseSmartFilter için, kod gürültü dağılımını NoiseDistribution.UNIFORM olarak ayarlar.

Sonrasında, kod akıllı nesne katmanına iki yeni filtre öğesi ekler: başka bir GaussianBlurSmartFilter ve bir AddNoiseSmartFilter.

Yeni filtreler ekledikten sonra, değişiklikleri update_resource_values() yöntemi kullanılarak uygular.

Son olarak, kod katmana ve katman maskesine filtreleri doğrudan uygulamanın ve apply() ve apply_to_mask() yöntemlerini kullanmanın nasıl yapıldığını gösterir.

Güncellenmiş görüntü, kaydedilerek çıkış dosya adı belirtilir.

Bu kod örneğini izleyerek, Aspose.PSD for Python'da akıllı filtrelerle nasıl çalışılacağını öğrenebilirsiniz. Kütüphane geniş bir akıllı filtre yelpazesi sunar, her biri görüntüleriniz üzerinde istenen etkileri elde etmek için özelleştirilebilecek kendi özelliklerine ve yöntemlerine sahiptir.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Belgeleme-Python-Aspose-psd-akilli-filtre-ozellikleri.py" >}}

## **Akıllı Filtreleri Katman Maskesine Uygulama**

Maskelere Akıllı Filtreler Uygulama: Güçlü Bir Görüntü Düzenleme Tekniği

Akıllı filtreler, kullanıcılara görüntülerine çeşitli filtreler ve efektler uygulama olanağı sunan bir popüler özelliktir. Akıllı filtreler kullanılarak elde edilebilecek ilginç bir teknik, filtreleri maskelere uygulamaktır. Bu makalede, maskelere akıllı filtreler uygulamanın nasıl gerçekleştirileceğini keşfedeceğiz ve görüntü düzenleme dünyasında kullanımlarını tartışacağız.

Maske Nedir? Maskelere akıllı filtreler uygularken, filtreler maskelerde belirtilen alanlara yalnızca uygulanır. Bu, görüntünün hangi bölümlerinin filtreden etkileneceği konusunda hassas kontrol sağlar. Maskeleri manipüle ederek, filtre etkisinin yoğunluğunu ve yayılmasını belirleyebilirsiniz.

Lütfen önceki örneği kontrol edin ve yöntemi: [API Referansı Maskeye Akıllı Filtre Uygulama](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

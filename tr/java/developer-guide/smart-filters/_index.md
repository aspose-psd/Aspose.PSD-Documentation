---
title: Java Aspose.PSD ile Akıllı Filtre Manipülasyonu
weight: 100
type: docs
description: PSD Dosyasında Akıllı Filtrelerin Kullanımı Örnekleri
keywords: [akıllı filtre, gürültü ekleme, gauss bulanıklığı, keskinleştirme, filtre, psd filtresi, psd api, java, kod örneği]
url: /tr/java/smart-filters/
---

## **Genel Bakış**

Aspose.PSD for Java'da akıllı filtreleri uygulamanın 3 yöntemi bulunmaktadır.

## **Doğrudan Filtre Uygulama**

Bu kod örneği, Aspose.PSD for Java'da akıllı filtreleri doğrudan nasıl uygulayacağınızı göstermektedir.

Başlangıçta, kod kaynak PSD dosyasını, orijinal görüntü için çıktı dosyasını ve güncellenmiş görüntü için çıktı dosyasını tanımlar.

Ardından, kod, Image.load() yöntemini kullanarak PSD görüntüsünü yükler ve bir PsdImage nesnesine dönüştürür.

Orijinal görüntü, çıktı dosya adını belirterek save() yöntemi kullanılarak kaydedilir.

İstenen akıllı filtreyi temsil etmek üzere bir SharpenSmartFilter nesnesi örneği oluşturulur.

Daha sonra, kod, psdImage.getLayers()[1] kullanarak PSD görüntüsünden düzenli katmanı alır.

Keskinleştirme filtresini düzenli katmana üç kez uygulamak için bir döngü kullanılır.

Son olarak, güncellenmiş görüntü, çıktı dosya adı ile save() yöntemi kullanılarak kaydedilir.

Bu kod, Aspose.PSD for Java'da akıllı filtrelerin doğrudan uygulanmasını örneklemektedir. Uygun filtre nesnelerinin kullanılması ve istenen katmanlara uygulanması ile görüntüler üzerinde istenilen etkiler elde edilebilir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **Akıllı Filtreleri Akıllı Nesnelerde Manipülasyon**

Bu kod örneği, Aspose.PSD for Java'da akıllı filtreleri akıllı nesneler içinde nasıl manipüle edeceğinizi açıklar.

Başlangıçta, kod kaynak PSD dosyasını, orijinal görüntü için çıktı dosyasını ve güncellenmiş görüntü için çıktı dosyasını tanımlar.

PSD görüntüsü, Image.load() yöntemi kullanılarak yüklenir ve ardından bir PsdImage nesnesine dönüştürülür.

Orijinal görüntü, çıktı dosya adını belirterek save() yöntemi kullanılarak kaydedilir.

Kod daha sonra PSD görüntüsünün ikinci katmanını akıllı nesne katmanı temsil eden bir SmartObjectLayer nesnesine dönüştürür.

Ardından, kod, GaussianBlurSmartFilter ve AddNoiseSmartFilter olmak üzere iki türü sergileyen akıllı filtrelerin düzenlenmesini gösterir.

GaussianBlurSmartFilter için, kod yarıçap, karışım modu, opaklık ve etkinleştirme durumu gibi filtre değerlerini günceller.

AddNoiseSmartFilter için, kod gürültü dağılımını NoiseDistribution.Uniform olarak ayarlar.

Sonraki adımda, kod akıllı nesne katmanına başka bir GaussianBlurSmartFilter ve bir AddNoiseSmartFilter ekler.

Yeni filtrelerin eklenmesinin ardından, değişiklikler updateResourceValues() yöntemi kullanılarak uygulanır.

Son olarak, kod, filtreleri doğrudan katmana ve maskesine apply() ve applyToMask() yöntemlerini kullanarak uygular.

Güncellenmiş görüntü daha sonra çıktı dosya adını belirterek save() yöntemi kullanılarak kaydedilir.

Bu kod örneğini takip ederek, Aspose.PSD for Java'da akıllı filtreleri akıllı nesneler içinde nasıl manipüle edebileceğinizi anlayabilirsiniz. Kütüphane, geniş bir akıllı filtre yelpazesi sunar ve her biri görüntüler üzerinde istenilen etkileri elde etmek için özelleştirilebilecek bir dizi özellik ve yönteme sahiptir.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** Katman Maskesine Akıllı Filtre Uygulama **

Maskelere Akıllı Filtreler Uygulama: Güçlü Bir Görüntü Düzenleme Tekniği

Görüntü düzenleme yazılımlarında yaygın olarak bulunan akıllı filtreler, kullanıcıların görüntülerine çeşitli filtreler ve efektler uygulamalarını sağlar. Akıllı filtreler tarafından mümkün kılınan ilginç bir teknik, maskelere uygulanmalarıdır. Bu makale, maskelere akıllı filtreleri uygulamayı ve görüntü düzenlemenin alanında bunların kullanım yararlarını incelemektedir.

Maskelerin Anlaşılması: Maskelere akıllı filtreler uygulamadan önce, bir maske kavramını kavramak önemlidir. Görüntü düzenlemede, bir maske, görüntü içinde belirli alanların şeffaflığını belirleyen bir gri tonlamalı görüntüdür. Maskeler, filtrelerin, ayarların veya efektlerin belirli bir görüntü bölümüne seçici olarak uygulanmasını sağlar, diğerlerini etkilemeden bırakır.

Maskelere Akıllı Filtreler Uygulama: Akıllı filtreler maskelere uygulandığında, yalnızca maske tarafından belirtilen alanları etkiler, filtre etkisinin üzerinde hassas kontrol sağlar. Maskeyi manipüle ederek, kullanıcılar filtre etkisinin yoğunluğunu ve yayılma derecesini modüle edebilirler.

Lütfen önceki örneğe ve yönteme bakınız: [Maskelere Akıllı Filtre Uygulama - API Referansı](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)

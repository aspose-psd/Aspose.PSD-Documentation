---
title: Psd Karıştırma Seçenekleri Manipülasyonu
weight: 100
type: docs
description: Aspose.PSD for Java, basit bir kod örneği ile karıştırma seçeneklerini ayarlamanıza yardımcı olabilir.
keywords: [karışım seçenekleri, karıştırma, efekt ekleme, opaklığı değiştirme, gölge rengini değiştirme, gölge ekleme, psd api, java, kod örneği]
url: tr/java/blending-options/
---

## **Genel Bakış**
Aspose.PSD for Java ile PSD görüntünüz içindeki katmanların görünümünü geliştirmek için karıştırma seçeneklerini değiştirmenin olanaklarına sahip olursunuz. Aşağıda, karıştırma seçeneklerini kullanma yöntemlerini gösteren bir Java kod örneği bulunmaktadır.

İlk olarak, kod bir PSD görüntüsünü yükler ve orijinal bir PNG dosyası olarak kaydeder. Ardından, belirli katmanların opaklığını ve karıştırma modunu değiştirir. Örneğin, ikinci katmanın opaklığını %100 olarak ayarlar ve beşinci katmanın karıştırma modunu Hue olarak değiştirir.

Ayrıca, kod belirlenen katmanlara karıştırma efektleri ekler. `addDropShadow()` yöntemini kullanarak, yedinci katmana bir düşen gölge efekti ekler, 30 derece bir gölge açısı ve RGB(255, 0, 0) bir gölge rengi belirler.

Dahası, kod dokuzuncu katmanın karıştırma modunu Lighten olarak ayarlar. Ayrıca, beşinci katmana `addColorOverlay()` yöntemi aracılığıyla bir renk örtüsü efekti uygular; renk örtüsünü RGB(30, 50, 0) olarak ve %150 opaklıkla ayarlar.

Son olarak, kod değiştirilmiş görüntüyü güncellenmiş bir PNG dosyası olarak kaydeder.

Özünde, Aspose.PSD for Java, PSD görüntüleriniz içindeki katmanların görünümünü manipüle etmek için çeşitli karıştırma seçenekleri sunar. Bu seçenekler, opaklığı değiştirme, karıştırma modlarını değiştirme ve düşen gölge ve renk örtüsü gibi çeşitli karıştırma efektleri uygulama gibi özellikleri içerir.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-blending-options.java" >}}

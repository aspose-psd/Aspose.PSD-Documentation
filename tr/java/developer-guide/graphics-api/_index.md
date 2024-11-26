---
title: PSD dosyalarındaki Katmanları Düzenlemek için Grafik API'sini Kullanma
weight: 100
type: docs
description: Aspose.PSD için Java'da Grafik API'sini kullanma örneği
keywords: [katmanı güncelle, daire çiz, elips çiz, dolu daire çiz, grafik, psd api, java, kod örneği]
url: tr/java/graphics-api/
---

## **Genel Bakış**
Başlamak için, Image.load() yöntemini kullanarak PSD dosyasını yükleyin veya sıfırdan bir Psd Image oluşturun. PSD dosyanıza yolunu temsil etmesi için inputFile değişkenini kullanın ve gerekiyorsa loadOpt ile herhangi bir yükleme seçeneğini belirtin.

Ardından, PSD görüntüsünün ilk katmanına erişmek için psdImage.getLayers()[0] sözdizimini kullanarak düzenleme yapmak için katman nesnesine bir referans elde edin.

Katmanı düzenlemek için, katmanı bir parametre olarak geçirerek bir Grafik nesnesi oluşturun. Bu nesne, şekilleri çizmek ve fırçalar uygulamak için çeşitli yöntemler sağlar.

Pen nesnesi, şekillerin kenarının rengini ve kalınlığını tanımlamak için kullanılır. Benzer şekilde, LinearGradientBrush gibi fırçalar dolgu renklerini tanımlamak için kullanılır.

Katman üzerine şekiller çizmek için graphics.drawEllipse() gibi yöntemleri kullanarak şekilleri çizebilir ve graphics.fillEllipse() ile onları doldurabilirsiniz.

Katmanda istenilen değişiklikleri yaptıktan sonra, değiştirilmiş PSD görüntüsünü psdImage.save() kullanarak kaydedin.

Ayrıca, uygun seçenekleri kullanarak PNG gibi diğer formatlarda da değiştirilmiş görüntüyü kaydedebilirsiniz.

Bu kadar! Aspose.PSD'nin Java için Grafik API'sini kullanarak PSD dosyalarında katmanları düzenlemeyi başarıyla gerçekleştirdiniz. Görüntü düzenleme yeteneklerinizi artırmak için Aspose.PSD kütüphanesinin daha fazla özellik ve işlevselliğini keşfedin.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Dokümantasyon-Java-Aspose-Psd-grafik-api.java" >}}

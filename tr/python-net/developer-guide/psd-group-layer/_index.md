---
title: Aspose.PSD ile Python'da grup katmanlarının kullanımı örneği
weight: 100
type: docs
description: Python aracılığıyla PSD Dosyası Grup Katmanının Kullanımı
keywords: [katman grubu, grup katmanı, katmanı gruba ekle, psd api, python, kod örneği]
url: tr/python-net/psd-group-layer/
---

## **Genel Bakış**

Aspose.PSD ile Python'da grup katmanlarıyla çalışmak, PSD görüntüsü içinde katmanları düzenlemek ve düzenlemek için güçlü bir özelliktir. Grup katmanları aynı zamanda klasör katmanları olarak da bilinir ve birçok katmanı bir araya getirme ve tüm grubun üzerine dönüşümler veya efektler uygulama olanağı sağlar.

Bu örnekte, öncelikle PsdImage.create yöntemini kullanarak yeni bir PSD görüntüsü oluştururuz. Ardından, PsdImage nesnesinin add_layer_group yöntemini kullanarak yeni bir LayerGroup nesnesi oluştururuz. Grup katmanının adını ("Klasör"), eklenmesi gereken dizini (0) ve grup katmanının görünür olup olmayacağını belirten bir boolean bayrağı sağlarız (Doğru).

Daha sonra, iki Layer nesnesi oluşturur ve görüntü isimlerini display_name özelliğini kullanarak belirleriz. Bu katmanları add_layer yöntemini kullanarak grup katmanına ekleriz.

Son olarak, LayerGroup nesnesinin layers özelliği kullanılarak grup içindeki katmanlara erişebiliriz. Örnekte, grup içindeki ilk ve ikinci katmanların görüntü isimlerinin sırasıyla "Katman 1" ve "Katman 2" olduğunu doğrularız.

Grup katmanlarını düzenledikten sonra, değiştirilmiş PSD görüntüsünü PsdImage nesnesinin save yöntemiyle kaydedebiliriz.

Aspose.PSD ile Python'da grup katmanlarıyla çalışmaya başlamanız için temel bir örnektir. Kütüphane, PSD görüntüleri içindeki katmanları manipüle etme ve dönüştürme için daha pek çok gelişmiş özellik sağlar. Grup katmanlarıyla ve kütüphanenin diğer özellikleriyle çalışma hakkında daha fazla ayrıntı ve örnek için Aspose.PSD belgelerine başvurabilirsiniz.

Aspose.PSD ile Python'da grup katmanlarıyla çalışmak için LayerGroup sınıfını kullanabilirsiniz. Aşağıda, bir grup katmanı oluşturmayı, ona katmanlar eklemeyi ve değiştirilmiş PSD görüntüsünü kaydetmeyi gösteren örnek bir kod parçası bulunmaktadır.

Lütfen tam örneği kontrol edin.

## **Örnek**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

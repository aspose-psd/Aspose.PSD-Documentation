---
title: Aspose.PSD for Java'da grup katmanlarının kullanım örneği
weight: 100
type: docs
description: Java aracılığıyla PSD Dosyasında Grup Katmanının Kullanımı
keywords: [katman grubu, grup katmanı, katman eklemek, psd api, java, kod örneği]
url: tr/java/psd-group-layer/
---

## **Genel Bakış**

Aspose.PSD for Java'da grup katmanlarını kullanmak, PSD görüntüsü içindeki katmanları etkili bir şekilde yönetmenize ve düzenlemenize olanak tanır. Grup katmanları, aynı zamanda klasör katmanları olarak da adlandırılan, birden fazla katmanı bir araya getirerek dönüşümleri veya efektleri topluca uygulamanıza olanak sağlar.

Başlamak için, PsdImage.create() yöntemini kullanarak yeni bir PSD görüntüsü oluşturun. Daha sonra, PsdImage nesnesinin addLayerGroup yöntemi aracılığıyla yeni bir LayerGroup nesnesi başlatın. Grup katmanı için istenen adı ("Klasör") belirtin, ekleme dizinini (0) belirtin ve görünürlüğünü belirten bir boolean bayrak set edin (True).

Ardından, iki Layer nesnesi oluşturun ve setDisplayName yöntemini kullanarak bunların görüntü adlarını ayarlayın. Bu katmanları addLayer yöntemini kullanarak grup katmanına ekleyin.

Grup içindeki katmanlara erişmek için, LayerGroup nesnesinin layers özelliğini kullanın. Grubun içindeki ilk ve ikinci katmanların görüntü adlarının sırasıyla "Katman 1" ve "Katman 2" olduğunu doğrulayın.

Grup katmanlarını manipüle ettiğinizde, değiştirilmiş PSD görüntüsünü PsdImage nesnesinin save yöntemini kullanarak kaydedin.

Bu, Java için Aspose.PSD kullanarak grup katmanlarıyla çalışmanıza yardımcı olacak temel bir örnektir. Kütüphane, PSD görüntüleri içinde katman manipülasyonu ve dönüşüm için birçok gelişmiş özellik sunar. Kütüphanenin grup katmanlarından ve diğer işlevselliğinden nasıl yararlanılacağı hakkında daha fazla detay ve örnek için Aspose.PSD for Java belgelerine başvurun.

Aspose.PSD for Java'da grup katmanlarıyla çalışmak için LayerGroup sınıfını kullanın. Aşağıdaki kod parçacığı, bir grup katmanı oluşturmayı, katmanları eklemeyi ve değiştirilmiş PSD görüntüsünü kaydetmeyi göstermektedir.

Lütfen sağlanan tam örneğe başvurun.

## **Örnek**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}

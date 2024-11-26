---
title: Aspose.PSD for C# İçinde Grup Katmanlarının Kullanımı Örneği
weight: 100
type: docs
description: C# Aracılığıyla PSD Dosyasının Grup Katmanının Kullanımı
keywords: [katman grubu, grup katmanı, katmanı gruba ekleme, psd api, C#, csharp, kod örneği]
url: tr/net/psd-group-layer/
---

## Genel Bakış

Aspose.PSD for C# içinde grup katmanları, bir PSD dosyasındaki katmanların verimli bir şekilde örgütlenmesine ve manipüle edilmesine imkan tanır. Klasör katmanları kullanarak, birden fazla katmanı bir araya getirebilir ve tüm grubu transformasyonlara veya efektlere tabi tutabilirsiniz.

Bu örnek, `PsdImage.Create` ile yeni bir PSD görüntüsü oluşturmayı göstermektedir. Ardından, `PsdImage` objesinden `AddLayerGroup` kullanılarak yeni bir `LayerGroup` objesi oluşturulur. Grup katmanı "Folder" olarak adlandırılmış, 0. sıraya eklenmiş ve görünür olarak ayarlanmıştır.

Daha sonra, iki tane `Layer` objesi oluşturulur ve `DisplayName` özellikleri belirlenir. Bu katmanlar, `AddLayer` kullanılarak grup katmanına eklenir.

Grup içindeki katmanlara, `LayerGroup` objesinin `Layers` özelliği aracılığıyla erişilebilir. Örnek, grubun içindeki birinci ve ikinci katmanların isimlerinin "Layer 1" ve "Layer 2" olduğunu doğrular.

Grup katmanları değiştirildikten sonra, güncellenmiş PSD görüntüsü, `PsdImage` objesinin `Save` yöntemi ile kaydedilir.

Bu temel örnek, Aspose.PSD for C# içinde grup katmanlarıyla çalışmayı tanıtmaktadır. Kütüphane, PSD dosyalarındaki katmanları manipüle etmek ve dönüştürmek için gelişmiş özellikler sunmaktadır. Daha detaylı örnekler ve özellikler için Aspose.PSD for C# belgelerine başvurabilirsiniz.

Aşağıda, Aspose.PSD for C# içinde grup katmanı kullanımını gösteren örnek bir kod bulunmaktadır:

## Örnek

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Daha fazla detaylı bilgi ve örnekler için [Aspose.PSD for C# belgelerini](https://docs.aspose.com/psd/net/) ziyaret ediniz.

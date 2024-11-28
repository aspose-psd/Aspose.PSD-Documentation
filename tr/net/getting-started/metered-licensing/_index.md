---
title: Lisanslama Yöntemiyle Ölçülü Lisanslama
type: docs
weight: 80
url: /tr/net/lisanslama-yöntemiyle-ölçülü-lisanslama/
description: PSD Photoshop C# Kütüphanesi, geliştiricilere varolan lisanslama yöntemiyle birlikte kullanılacak olan yeni bir lisanslama mekanizması olan ölçülü anahtar uygulamasına izin verir.
---

{{% alert color="primary" %}}

Aspose.PSD, geliştiricilere ölçülü anahtar uygulamasına izin verir. Bu yeni bir lisanslama mekanizmasıdır. Yeni lisanslama mekanizması, var olan lisanslama yöntemiyle birlikte kullanılacaktır. API özelliklerinin kullanımına göre faturalandırılmak isteyen müşteriler, ölçülü lisanslamayı kullanabilirler. Daha fazla detay için [Ölçülü Lisanslama SSS](https://purchase.aspose.com/faqs/licensing/metered) bölümüne başvurun.

{{% /alert %}}
## **Ölçülü Lisanslama**
İşte Metered sınıfını kullanmanın basit adımları.

1. Metered sınıfından bir örnek oluşturun.
1. setMeteredKey yöntemine genel ve özel anahtarları iletin.
1. İşlem yapın (görevi gerçekleştirin).
1. Metered sınıfının getConsumptionQuantity yöntemini çağırın.
1. Şimdiye kadar ne kadar API isteğinin tüketildiğini döndürecektir.

Aşağıda, ölçülü genel ve özel anahtarları nasıl ayarlayacağınızı gösteren örnek kod bulunmaktadır.

{{< highlight java >}}

 // PSD Metered sınıfının bir örneğini oluşturun

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// setMeteredKey özelliğine erişin ve genel anahtarı ve özel anahtarları parametre olarak ileten

metered.SetMeteredKey("*****", "*****");



// API'yı çağırmadan önce ölçülü veri miktarını alın

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Bilgiyi göster

Console.WriteLine("Önce Tüketilen Miktar: " + amountbefore.ToString());

// API'yı çağırdıktan sonraki ölçülü veri miktarını alın

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Bilgiyi göster

Console.WriteLine("Sonra Tüketilen Miktar: " + amountafter.ToString());

{{< /highlight >}}

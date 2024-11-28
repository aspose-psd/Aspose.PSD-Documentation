---
title: Ölçümlü Lisanslama
type: docs
weight: 70
url: /tr/java/olcumlu-lisanslama/
---

{{% alert color="primary" %}} 

Aspose.PSD geliştiricilere ölçümlü anahtar uygulama olanağı tanır. Bu yeni bir lisanslama mekanizmasıdır. Yeni lisanslama mekanizması, mevcut lisanslama yöntemi ile birlikte kullanılacaktır. API özelliklerinin kullanımına göre faturalandırılmak isteyen müşteriler ölçümlü lisanslamayı kullanabilirler. Daha fazla bilgi için [Ölçümlü Lisanslama SSS](https://purchase.aspose.com/faqs/licensing/metered) bölümüne başvurun.

{{% /alert %}} 
## **Ölçümlü Lisanslama**
Metered sınıfını kullanmanın basit adımları aşağıda verilmiştir.

1. Metered sınıfından bir örnek oluşturun.
1. setMeteredKey yöntemine genel ve özel anahtarları geçirin.
1. İşlem yapın (görevi gerçekleştirin).
1. Metered sınıfın getConsumptionQuantity yöntemini çağırın.
1. Şimdiye kadar tükettiğiniz API isteklerinin miktarını/özetini alacaktır.

Aşağıda, ölçümlü genel ve özel anahtarın nasıl ayarlanacağını gösteren örnek bir kod bulunmaktadır.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

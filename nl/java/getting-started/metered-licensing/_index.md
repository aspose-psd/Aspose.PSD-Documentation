---
title: Gelicentieerde metering
type: docs
weight: 70
url: /nl/java/metered-licensing/
---

{{% alert color="primary" %}}

Aspose.PSD stelt ontwikkelaars in staat om een gemeten sleutel toe te passen. Het is een nieuw licentiemechanisme. Het nieuwe licentiemechanisme zal worden gebruikt in combinatie met de bestaande licentiemethode. Die klanten die op basis van het gebruik van de API-functies gefactureerd willen worden, kunnen gebruik maken van de meteringslicenties. Voor meer details, zie de [Veelgestelde vragen over Metered Licensing](https://purchase.aspose.com/faqs/licensing/metered) sectie.

{{% /alert %}}
## **Gelicentieerde metering**
Hier zijn de eenvoudige stappen om de Metered-klasse te gebruiken.

1. Maak een instantie van de Metered-klasse.
1. Geef openbare en geheime sleutels door aan de methode setMeteredKey.
1. Voer verwerking uit (voer taak uit).
1. Roep de methode getConsumptionQuantity van de Metered-klasse aan.
1. Het zal het bedrag/aantal API-verzoeken retourneren dat u tot nu toe hebt verbruikt.

Hieronder staat de voorbeeldcode die demonstreert hoe u een gemeten openbare en geheime sleutel instelt.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}


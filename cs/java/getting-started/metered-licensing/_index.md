---
title: Metered Licensing
type: docs
weight: 70
url: /cs/java/metered-licensing/
---

{{% alert color="primary" %}} 

Aspose.PSD umožňuje vývojářům používat měřený klíč. Jedná se o nový licenční mechanismus. Nový licenční mechanismus bude použit společně s existující metodou licencování. Ti zákazníci, kteří chtějí být fakturováni na základě využití funkcí API, mohou použít měřené licencování. Pro více informací se podívejte do sekce [Metered Licensing FAQ](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 

## **Měřené licencování**
Zde jsou jednoduché kroky k použití třídy Metered.

1. Vytvořte instanci třídy Metered.
1. Předejte veřejné a soukromé klíče metodě setMeteredKey.
1. Provádějte zpracování (vykonávejte úlohy).
1. Zavolejte metodu getConsumptionQuantity třídy Metered.
1. Vrátí množství/počet požadavků API, které jste zatím spotřebovali.

Níže je ukázkový kód, který ukazuje, jak nastavit měřený veřejný a soukromý klíč.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}

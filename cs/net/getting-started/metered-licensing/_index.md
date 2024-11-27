---
title: Metered Licensing
type: docs
weight: 80
url: /cs/net/metered-licensing/
description: Knihovna PSD Photoshop C# umožňuje vývojářům používat měřený klíč, což je nový způsob licencování, který bude používán společně s existující metodou licencování.
---

{{% alert color="primary" %}} 

Aspose.PSD umožňuje vývojářům aplikovat měřený klíč. Jedná se o nový mechanismus licencování. Nový mechanismus licencování bude použit společně s existující metodou licencování. Zákazníci, kteří chtějí být fakturováni na základě využití funkcí API, mohou využít měřené licencování. Pro více informací se podívejte na sekci [FAQ o měřeném licencování](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Měřené licencování**
Zde jsou jednoduché kroky, jak použít třídu Metered.

1. Vytvořte instanci třídy Metered.
1. Předejte veřejné a soukromé klíče metodě setMeteredKey.
1. Proveďte zpracování (vykonávejte úlohy).
1. Zavolejte metodu getConsumptionQuantity třídy Metered.
1. Vrátí množství/četnost požadavků API, které jste doposud spotřebovali.

Následuje ukázkový kód, jak nastavit veřejný a soukromý klíč pro měření.

{{< highlight java >}}

 // Vytvoření instance třídy Metered

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();
 
 // Přístup k vlastnosti setMeteredKey a předání veřejných a soukromých klíčů jako parametrů

metered.SetMeteredKey("*****", "*****");

 // Získání množství měřených dat před voláním API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();

 // Zobrazení informací

Console.WriteLine("Spotřebováno před: " + amountbefore.ToString());

 // Získání množství měřených dat po volání API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();

 // Zobrazení informací

Console.WriteLine("Spotřebováno po: " + amountafter.ToString());

{{< /highlight >}}

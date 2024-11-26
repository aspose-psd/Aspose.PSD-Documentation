---
title: Metered Licensing
type: docs
weight: 80
url: /nl/net/metered-licensing/
description: De PSD Photoshop C# Library stelt ontwikkelaars in staat om een metered key toe te passen, wat een nieuwe licentiemechanisme is en zal worden gebruikt naast de bestaande licentiemethode.
---

{{% alert color="primary" %}}

Aspose.PSD staat ontwikkelaars toe om een metered key toe te passen. Het betreft een nieuw licentiemechanisme. Dit nieuwe licentiemechanisme wordt gebruikt naast de bestaande licentiemethode. Klanten die graag op basis van het gebruik van de API-functies willen worden gefactureerd, kunnen gebruik maken van de metered licensing. Voor meer details, zie de [Veelgestelde vragen over Metered Licensing](https://purchase.aspose.com/faqs/licensing/metered) sectie.

{{% /alert %}}
## **Metered Licensing**
Hier zijn de eenvoudige stappen om de Metered class te gebruiken.

1. Maak een instantie van de Metered class.
1. Geef de openbare en prive sleutels door aan de setMeteredKey methode.
1. Voer verwerking uit (voer de taak uit).
1. Roep de methode getConsumptionQuantity van de Metered class aan.
1. Het zal de hoeveelheid/aantal API-aanvragen teruggeven die tot nu toe zijn verbruikt.

Hieronder staat de voorbeeldcode die demonstreert hoe je een metered openbare en prive sleutel instelt.

{{< highlight java >}}

 // Maak een instantie van de PSD Metered class

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Open de setMeteredKey eigenschap en geef openbare en privé sleutels door als parameters

metered.SetMeteredKey("*****", "*****");



// Ontvang de metered gegevenshoeveelheid voordat de API wordt aangeroepen

decimal hoeveelheidVoor = Aspose.PSD.Metered.GetConsumptionQuantity();



// Toon informatie

Console.WriteLine("Hoeveelheid Verbruikt Voor: " + hoeveelheidVoor.ToString());

// Ontvang de metered gegevenshoeveelheid na het aanroepen van de API

decimal hoeveelheidNa = Aspose.PSD.Metered.GetConsumptionQuantity();



// Toon informatie

Console.WriteLine("Hoeveelheid Verbruikt Na: " + hoeveelheidNa.ToString());

{{< /highlight >}}

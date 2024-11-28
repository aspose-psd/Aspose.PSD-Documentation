---
title: Abgerechnete Lizenzierung
type: docs
weight: 80
url: /de/net/abgerechnete-lizenzierung/
description: Die PSD Photoshop C#-Bibliothek ermöglicht Entwicklern die Anwendung eines abgerechneten Schlüssels, der ein neuer Lizenzierungsmechanismus ist und zusammen mit der bestehenden Lizenzierungsmethode verwendet wird.
---

{{% alert color="primary" %}} 

Aspose.PSD ermöglicht Entwicklern die Anwendung eines abgerechneten Schlüssels. Es handelt sich um einen neuen Lizenzierungsmechanismus. Dieser neue Lizenzierungsmechanismus wird zusammen mit der bestehenden Lizenzierungsmethode verwendet. Kunden, die basierend auf der API-Nutzung abgerechnet werden möchten, können die abgerechnete Lizenzierung nutzen. Für weitere Details verweisen wir auf den Abschnitt [Häufig gestellte Fragen zur abgerechneten Lizenzierung](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Abgerechnete Lizenzierung**
Hier sind die einfachen Schritte zur Verwendung der Metered-Klasse.

1. Erstellen einer Instanz der Metered-Klasse.
1. Übergeben von öffentlichen und privaten Schlüsseln an die Methode setMeteredKey.
1. Verarbeitung durchführen (Aufgabe ausführen).
1. Methode getConsumptionQuantity der Metered-Klasse aufrufen.
1. Es wird die Menge/Anzahl der API-Anfragen zurückgeben, die Sie bisher verbraucht haben.

Nachfolgend finden Sie den Beispielcode, der zeigt, wie man den abgerechneten öffentlichen und privaten Schlüssel festlegt.

{{< highlight java >}}

 // Erstellen einer Instanz der PSD Metered-Klasse

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Zugriff auf die Eigenschaft setMeteredKey und Übergeben von öffentlichen und privaten Schlüsseln als Parameter

metered.SetMeteredKey("*****", "*****");



// Ermitteln der abgerechneten Datenmenge vor dem Aufrufen der API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Informationen anzeigen

Console.WriteLine("Betrag vor Verbrauch: " + amountbefore.ToString());

// Ermitteln der abgerechneten Datenmenge nach dem Aufrufen der API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Informationen anzeigen

Console.WriteLine("Betrag nach Verbrauch: " + amountafter.ToString());

{{< /highlight >}}

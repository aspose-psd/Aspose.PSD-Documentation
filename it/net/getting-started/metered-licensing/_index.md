---
title: Licenza a consumo
type: docs
weight: 80
url: /it/net/licenza-a-consumo/
description: La libreria C# di PSD Photoshop consente agli sviluppatori di applicare una chiave a consumo che è un nuovo meccanismo di licenza e verrà utilizzata insieme al metodo di licenza esistente.
---

{{% alert color="primary" %}}

Aspose.PSD consente agli sviluppatori di applicare una chiave a consumo. Si tratta di un nuovo meccanismo di licenza. Il nuovo meccanismo di licenza verrà utilizzato insieme al metodo di licenza esistente. I clienti che desiderano essere fatturati in base all'utilizzo delle funzionalità dell'API possono utilizzare la licenza a consumo. Per ulteriori dettagli, fare riferimento alla sezione [Domande frequenti sulla licenza a consumo](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}}
## **Licenza a consumo**
Di seguito sono riportati i semplici passaggi per utilizzare la classe Metered.

1. Creare un'istanza della classe Metered.
1. Passare le chiavi pubbliche e private al metodo setMeteredKey.
1. Eseguire l'elaborazione (eseguire il compito).
1. Chiamare il metodo getConsumptionQuantity della classe Metered.
1. Restituirà l'importo/quantità di richieste API consumate finora.

Di seguito è riportato un esempio di codice che mostra come impostare la chiave pubblica e privata a consumo.

{{< highlight java >}}

 // Creare un'istanza della classe Metered di PSD

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// Accedere alla proprietà setMeteredKey e passare le chiavi pubblica e privata come parametri

metered.SetMeteredKey("*****", "*****");



// Ottenere l'importo dei dati a consumo prima di chiamare l'API

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// Visualizzare le informazioni

Console.WriteLine("Quantità consumata prima: " + amountbefore.ToString());

// Ottenere l'importo dei dati a consumo dopo aver chiamato l'API

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// Visualizzare le informazioni

Console.WriteLine("Quantità consumata dopo: " + amountafter.ToString());

{{< /highlight >}}  

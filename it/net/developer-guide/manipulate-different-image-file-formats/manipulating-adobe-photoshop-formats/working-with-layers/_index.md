---
title: Lavorare con i Livelli
type: docs
weight: 150
url: /it/net/lavorare-con-i-livelli/
---

## **Creare un Gruppo di Livelli**
Un gruppo di livelli è costituito da uno o più livelli e aiuta ad organizzare livelli simili o correlati. Utilizzando Aspose.PSD per .NET è possibile creare un gruppo di livelli. A questo scopo, è stato aggiunto un nuovo metodo [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) in una classe **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** per aggiungere il gruppo di livelli.

I passaggi per creare gruppi di livelli sono semplici come segue:

- Creare un'istanza di un'immagine utilizzando la classe PsdImage con larghezza, altezza e opzioni immagine specificate.
- Creare un [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) con il nome del gruppo e l'indice specificati.
- Creare un'istanza della classe Layer ed assegnare l'immagine PSD ad essa.
- Aggiungere il livello creato al gruppo di livelli utilizzando il metodo AddLayer esposto dalla classe LayerGroup
- Salvare i risultati.

Il seguente frammento di codice mostra come creare un gruppo di livelli.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Rinominare un Livello**
Puoi utilizzare qualsiasi nome che desideri, ma la pratica tipica è utilizzare una descrizione generale dell'oggetto o dell'elemento che si trova in quel livello. Questo articolo dimostra come è possibile modificare il nome di un livello utilizzando Aspose.PSD per .NET. A questo scopo, è stata aggiunta una nuova proprietà [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) nella classe Layer per visualizzare correttamente un nome di livello. È stato osservato che quando Photoshop salva un nome di livello utilizzando la proprietà [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), allora i caratteri coreani vengono memorizzati come byte 63 '?' in ASCII. Quindi, se desideri visualizzare correttamente un nome di livello, utilizza la proprietà **DisplayName** poiché la proprietà **Name** non supporta i caratteri coreani.


Il seguente esempio di codice mostra come è possibile rinominare un livello.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Supporto dei Livelli Collegati**
Il collegamento dei livelli è simile all'aggregazione dei livelli. Se stai collegando due o più livelli, ti consentirà di apportare determinate modifiche ad entrambi i livelli collegati. Ad esempio, se applichi trasformazioni a un livello allora verranno applicate a tutti gli altri livoni collegati. Questo articolo dimostra come puoi ottenere e scollegare i livelli collegati utilizzando [Aspose.PSD](https://products.aspose.com/psd).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}

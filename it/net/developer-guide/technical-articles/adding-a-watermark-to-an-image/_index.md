---
title: Aggiungere un Filigrana a un'Immagine
type: docs
weight: 30
url: /it/net/aggiungere-un-filigrana-a-un-immagine/
---

## **Aggiungere un Filigrana a un'Immagine**
Questo documento spiega come aggiungere un filigrana a un'immagine utilizzando Aspose.PSD. Aggiungere un filigrana a un'immagine è un requisito comune per le applicazioni di elaborazione delle immagini. Questo esempio utilizza la classe Graphics per disegnare una stringa sulla superficie dell'immagine.
### **Aggiungere un Filigrana**
Per dimostrare l'operazione, caricheremo un'immagine BMP dal disco e disegneremo una stringa come filigrana sulla superficie dell'immagine utilizzando il metodo DrawString della classe Graphics. Salveremo l'immagine in formato PNG utilizzando la classe PngOptions. Di seguito è riportato un esempio di codice che dimostra come aggiungere un filigrana a un'immagine. Il codice di esempio è stato suddiviso in parti per renderlo facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. [Caricare](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) un'immagine.
1. Creare e inizializzare un oggetto [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. Creare e inizializzare oggetti Font e [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. Disegnare una stringa come filigrana utilizzando il metodo [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) della classe Graphics.
1. Salvare l'immagine in formato PNG.

Il seguente frammento di codice mostra come aggiungere un filigrana all'immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Aggiungere un Filigrana Diagonale**
Aggiungere un filigrana diagonale a un'immagine è simile all'aggiunta di un filigrana orizzontale come discusso in precedenza, con alcune differenze. Per dimostrare l'operazione, caricheremo un'immagine JPG dal disco, aggiungeremo trasformazioni utilizzando un oggetto della classe [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) e disegneremo una stringa come filigrana sulla superficie dell'immagine utilizzando il metodo DrawString della classe Graphics. Di seguito è riportato un esempio di codice che dimostra come aggiungere un filigrana diagonale a un'immagine. Il codice di esempio è stato suddiviso in parti per renderlo facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. Caricare un'immagine.
1. Creare e inizializzare un oggetto Graphics.
1. Creare e inizializzare oggetti [Font](https://reference.aspose.com/psd/net/aspose.psd/font) e SolidBrush.
1. Ottenere le dimensioni dell'immagine in un oggetto [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. Creare un'istanza della classe Matrix e eseguire la trasformazione composita.
1. Assegnare la trasformazione all'oggetto Graphics.
1. Creare e inizializzare un oggetto [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. Disegnare una stringa come filigrana utilizzando il metodo DrawString della classe Graphics.
1. Salvare l'immagine risultante.

Il seguente frammento di codice mostra come aggiungere un filigrana diagonale.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}


---
title: Aggiungere un Filigrana a un'Immagine
type: docs
weight: 20
url: /it/java/aggiungere-una-filigrana-a-un-immagine/
---

## **Aggiungere un Filigrana a un'Immagine**
Questo documento spiega come aggiungere un filigrana a un'immagine utilizzando Aspose.PSD. Aggiungere un filigrana a un'immagine è un requisito comune per le applicazioni di elaborazione di immagini. Questo esempio utilizza la classe Graphics per disegnare una stringa sulla superficie dell'immagine.
### **Aggiungere un Filigrana**
Per dimostrare l'operazione, caricheremo un'immagine BMP da disco e disegneremo una stringa come filigrana sulla superficie dell'immagine utilizzando il metodo DrawString della classe Graphics. Salveremo l'immagine in formato PNG utilizzando la classe PngOptions. Di seguito è riportato un esempio di codice che dimostra come aggiungere un filigrana a un'immagine. Il codice sorgente dell'esempio è stato suddiviso in parti per renderlo facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. Caricare un'immagine.
1. Creare e inizializzare un oggetto Graphics.
1. Creare e inizializzare oggetti Font e SolidBrush.
1. Disegnare una stringa come filigrana utilizzando il metodo DrawString della classe Graphics.
1. Salvare l'immagine in PNG.

Il seguente frammento di codice mostra come aggiungere un filigrana all'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Aggiungere un Filigrana Diagonale**
Aggiungere un filigrana diagonale a un'immagine è simile ad aggiungere un filigrana orizzontale come discusso in precedenza, con alcune differenze. Per dimostrare l'operazione, caricheremo un'immagine JPG da disco, aggiungeremo trasformazioni utilizzando un oggetto della classe Matrix e disegneremo una stringa come filigrana sulla superficie dell'immagine utilizzando il metodo DrawString della classe Graphics. Di seguito è riportato un esempio di codice che dimostra come aggiungere un filigrana diagonale a un'immagine. Il codice sorgente dell'esempio è stato suddiviso in parti per renderlo facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. Caricare un'immagine.
1. Creare e inizializzare un oggetto Graphics.
1. Creare e inizializzare oggetti Font e SolidBrush.
1. Ottenere la dimensione dell'immagine in un oggetto SizeF.
1. Creare un'istanza della classe Matrix e eseguire una trasformazione composita.
1. Assegnare la trasformazione all'oggetto Graphics.
1. Creare e inizializzare un oggetto StringFormat.
1. Disegnare una stringa come filigrana utilizzando il metodo DrawString della classe Graphics.
1. Salvare l'immagine risultante.

Il seguente frammento di codice mostra come aggiungere un filigrana diagonale.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}

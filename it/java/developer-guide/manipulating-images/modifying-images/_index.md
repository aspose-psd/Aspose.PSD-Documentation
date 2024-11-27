---
title: Modifica Immagini
type: docs
weight: 50
url: /it/java/modifica-immagini/
---

## **Dittering per Immagini Raster**
Il dithering è una tecnica che crea l'illusione di nuovi colori e sfumature variando il modello di punti che compongono effettivamente un'immagine. È il modo più comune per ridurre la gamma di colori delle immagini a 256 (o meno) colori. Aspose.PSD fornisce il supporto al dithering per la classe RasterImage introducendo il metodo Dither che accetta due parametri. Il primo è di tipo DitheringMethod da applicare con due opzioni possibili: FloydSteinbergDithering e ThresholdDithering. Il secondo parametro del metodo Dither è il BitCount in intero. BitCount definisce la dimensione del campionamento per il risultato del dithering. Il valore predefinito è 1 che rappresenta il bianco e nero, mentre i valori consentiti sono 1, 4, 8 generando palette con rispettivamente 2, 4 e 256 colori.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **Regolazione di Luminosità, Contrasto e Gamma**
La regolazione dei colori nelle immagini digitali è una delle funzionalità principali che la maggior parte delle librerie di elaborazione delle immagini fornisce. Le regolazioni dei colori possono essere categorizzate come segue.

1. La luminosità si riferisce alla luminosità o alla scurezza del colore. Aumentando la luminosità di un'immagine tutte le colorazioni diventano più chiare, mentre diminuendo la luminosità le colorazioni diventano più scure.
1. Il contrasto si riferisce a rendere gli oggetti o i dettagli all'interno di un'immagine più evidenti. Aumentando il contrasto di un'immagine aumenta la differenza tra le aree chiare e scure in modo che le aree chiare diventino più chiare e le aree scure diventino più scure. Riducendo il contrasto, le aree chiare e scure rimangono approssimativamente le stesse ma l'immagine complessiva diventa più omogenea.
1. Gamma ottimizza il contrasto e la luminosità dell'illuminazione indiretta che sta illuminando un oggetto nell'immagine.
### **Regolazione di Luminosità**
Aspose.PSD fornisce il metodo AdjustBrightness per la classe RasterImage che può essere utilizzato per regolare la luminosità dell'immagine passando un valore intero come parametro. Il valore del parametro più alto indica un'immagine più luminosa. Qui è presente l'immagine originale e l'immagine risultante per il confronto.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **Regolazione del Contrasto**
Il metodo AdjustContrast esposto dalla classe RasterImage può essere utilizzato per regolare il contrasto di un'immagine passando un valore float come parametro.

Il valore del parametro più alto indica un contrasto maggiore nell'immagine fornita. Qui è presente l'immagine originale e l'immagine risultante per il confronto.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **Regolazione della Gamma**
Il metodo AdjustGamma esposto dalla classe RasterImage ha due versioni. Una delle sovraccariche accetta un valore float e esegue la correzione Gamma per i coefficienti del canale rosso, blu e verde. Mentre l'altra sovraccarica accetta tre parametri float che rappresentano ciascun coefficiente di colore separatamente. L'esempio di codice seguente mostra come eseguire AdjustGamma su un'immagine.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **Sfocare un'Immagine**
Questo articolo dimostra l'uso di Aspose.PSD per Java per eseguire un effetto di sfocatura su un'immagine. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD per Java ha esposto la classe GaussianBlurFilterOptions per creare un effetto di sfocatura al volo. La classe GaussianBlurFilterOptions ha bisogno di valori di raggio e sigma per creare un effetto di sfocatura su un'immagine. I passaggi per eseguire il Ridimensionamento sono semplici come segue:

1. Caricare un'immagine utilizzando il metodo factory Load esposto dalla classe Image.
1. Convertire l'immagine in RasterImage.
1. Creare un'istanza della classe GaussianBlurFilterOptions con il costruttore predefinito o fornire i valori di raggio e sigma nel costruttore.
1. Chiamare il metodo RasterImage.Filter specificando il rettangolo come limiti dell'immagine e l'istanza della classe GaussianBlurFilterOptions.
1. Salvare i risultati.

L'esempio di codice seguente mostra come creare un effetto di sfocatura su un'immagine.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **Verificare la Trasparenza dell'Immagine**
Questo articolo dimostra l'uso di Aspose.PSD per Java per verificare la trasparenza dell'immagine. I passaggi per verificare la trasparenza dell'immagine sono semplici come segue:

1. Caricare un'immagine utilizzando il metodo factory Load esposto dalla classe Image.
1. Verificare l'opacità dell'immagine; se l'opacità è zero, l'immagine è trasparente.
1. L'esempio di codice seguente mostra come verificare se l'immagine è trasparente o meno.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **Implementare un Compressore GIF con Perdita**
Utilizzando Aspose.PSD per Java, gli sviluppatori possono impostare la differenza dei pixel. La compressione del GIF si basa su un "dizionario" di stringhe di pixel viste. L'encoder normale cerca nel dizionario la stringa più lunga di pixel che corrisponde esattamente ai pixel nell'immagine. L'encoder perdente sceglie la stringa più lunga di pixel che è "abbastanza simile" ai pixel nell'immagine. Di seguito è mostrata la dimostrazione del codice della funzionalità menzionata.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **Implementare il Ricampionamento Bicubico**
Il ricampionamento significa che si stanno cambiando le dimensioni dei pixel di un'immagine. Quando si ridimensiona in basso, si stanno eliminando pixel e quindi si sta eliminando informazioni e dettagli dall'immagine. Quando si ridimensiona verso l'alto, si stanno aggiungendo pixel. Photoshop aggiunge questi pixel utilizzando l'interpolazione. Questo articolo dimostra come è possibile eseguire il Ricampionamento Bicubico utilizzando Aspose.PSD per Java.

Di seguito è mostrata la dimostrazione del codice della funzionalità menzionata.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **Livello di Regolazione dell'Inversione**
Questo articolo dimostra come è possibile eseguire il **Livello di regolazione dell'Inversione** utilizzando Aspose.PSD per Java.  Un livello di regolazione è un tipo speciale di livello usato principalmente per la correzione del colore. Piuttosto che avere un proprio contenuto, regolano le informazioni sui livelli sottostanti. Il livello di regolazione dell'inversione crea un effetto di negativo fotografico invertendo i colori di un'immagine.

Di seguito è mostrata la dimostrazione del codice della funzionalità menzionata.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}

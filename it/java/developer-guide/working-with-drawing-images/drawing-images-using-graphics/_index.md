---
title: Disegno di immagini utilizzando Graphics
type: docs
weight: 20
url: /it/java/drawing-images-using-graphics/
---

## **Disegno di immagini utilizzando Graphics**

Con la libreria Aspose.PSD puoi disegnare forme semplici come linee, rettangoli e cerchi, così come forme complesse come poligoni, curve, archi e forme di Bezier. La libreria Aspose.PSD crea tali forme utilizzando la classe Graphics che risiede nello spazio dei nomi Aspose.PSD. Gli oggetti Graphics sono responsabili di eseguire diverse operazioni di disegno su un'immagine, modificandone così la superficie. La classe Graphics utilizza una varietà di oggetti ausiliari per migliorare le forme:

- Penne, per disegnare linee, delineare forme o renderizzare altre rappresentazioni geometriche.
- Pennelli, per definire come vengono riempite le aree.
- Caratteri, per definire la forma dei caratteri di testo.

### **Disegno con la classe Graphics**

Di seguito è riportato un esempio di codice che dimostra l'utilizzo della classe Graphics. Il codice sorgente dell'esempio è stato diviso in diverse parti per mantenerlo semplice e facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. Creare un'immagine.
1. Creare e inizializzare un oggetto Graphics.
1. Pulire la superficie.
1. Disegnare un'ellisse.
1. Disegnare un poligono riempito e salvare l'immagine.

### **Esempi di programmazione**

#### **Creazione di un'immagine**

Inizia creando un'immagine utilizzando uno dei metodi descritti in Creazione di file.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **Creare e inizializzare un oggetto Graphics**

Quindi crea e inizializza un oggetto Graphics passando l'oggetto Image al suo costruttore.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **Pulire la superficie**

Pulisci la superficie Graphics chiamando il metodo Clear della classe Graphics e passa un colore come parametro. Questo metodo riempie la superficie Graphics con il colore passato come argomento.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **Disegnare un'ellisse**

Potresti notare che la classe Graphics ha esposto molti metodi per disegnare e riempire forme. Troverai l'elenco completo dei metodi nel riferimento API di Aspose.PSD per Java. La classe Graphics ha esposto diverse versioni sovraccaricate del metodo DrawEllipse. Tutti questi metodi accettano un oggetto Pen come primo argomento. I parametri successivi sono passati per definire il rettangolo delimitante intorno all'ellisse. Per l'esempio, utilizza la versione che accetta un oggetto Rectangle come secondo parametro per disegnare un'ellisse utilizzando l'oggetto Pen nel colore desiderato.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **Disegnare un poligono riempito**

Successivamente, disegna un poligono utilizzando il LinearGradientBrush e un array di punti. La classe Graphics ha esposto diverse versioni sovraccaricate del metodo FillPolygon. Tutti questi accettano un oggetto Pennello come primo argomento, che definisce le caratteristiche del riempimento. Il secondo parametro è un array di punti. Si noti che ogni due punti consecutivi nell'array specificano un lato del poligono.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **Disegno di immagini utilizzando Graphics: Codice sorgente completo**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

Tutte le classi che implementano IDisposable e accedono a risorse non gestite sono istanziate in un'istruzione Using per garantire che vengano correttamente dispose.

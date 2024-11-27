---
title: Disegno di Immagini usando Graphics
type: docs
weight: 20
url: /it/net/drawing-images-using-graphics/
---

## **Disegno di Immagini usando Graphics**
Con la libreria Aspose.PSD puoi disegnare forme semplici come linee, rettangoli e cerchi, così come forme complesse come poligoni, curve, archi e forme di Bezier. La libreria Aspose.PSD crea tali forme utilizzando la classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) che risiede nello spazio dei nomi Aspose.PSD. Gli oggetti Graphics sono responsabili di eseguire diverse operazioni di disegno su un'immagine, modificando quindi la superficie dell'immagine. La classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) utilizza una varietà di oggetti di supporto per migliorare le forme:

· Pennelli, per disegnare linee, contornare forme o renderizzare altre rappresentazioni geometriche.

· Pennelli, per definire come vengono riempite le aree.

· Caratteri, per definire la forma dei caratteri del testo.
### **Disegno con la Classe Graphics**
Di seguito è riportato un esempio di codice che dimostra l'uso della classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). Il codice di esempio è stato suddiviso in diverse parti per mantenerlo semplice e facile da seguire. Passo dopo passo, gli esempi mostrano come:

1. Creare un'immagine.
1. Creare e inizializzare un oggetto Graphics.
1. Pulire la superficie.
1. Disegnare un'ellisse.
1. Disegnare un poligono riempito e salvare l'immagine.
### **Esempi di Programmazione**
#### **Creazione di un'Immagine**
Inizia creando un'immagine utilizzando uno qualsiasi dei metodi descritti in Creare File.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Creare e Inizializzare un Oggetto Graphics**
Quindi crea e inizializza un oggetto Graphics passando l'oggetto Image al suo costruttore.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Pulire la Superficie**
Pulisci la superficie Graphics chiamando il metodo Clear della classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) e passa il colore come parametro. Questo metodo riempie la superficie Graphics con il colore passato come argomento.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Disegnare un'Ellisse**
Potresti notare che la classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ha esposto molti metodi per disegnare e riempire forme. Troverai l'elenco completo dei metodi nel riferimento API di Aspose.PSD per .NET. Sono state esposte diverse versioni sovraccaricate del metodo DrawEllipse dalla classe Graphics. Tutti questi metodi accettano un oggetto Pen come primo argomento. I parametri successivi vengono passati per definire il rettangolo di delimitazione attorno all'ellisse. Per questo esempio, usa la versione che accetta un oggetto Rectangle come secondo parametro per disegnare un'ellisse utilizzando l'oggetto Pen nel colore desiderato.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Disegnare un Poligono Riempito**
Successivamente, disegna un poligono utilizzando il LinearGradientBrush e un array di punti. La classe Graphics ha esposto diverse versioni sovraccariche del metodo FillPolygon(). Tutti questi accettano un oggetto Brush come primo argomento, definendo le caratteristiche del riempimento. Il secondo parametro è un array di punti. Si noti che ogni due punti consecutivi nell'array specificano un lato del poligono.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Disegno di Immagini usando Graphics : Codice Sorgente Completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Tutte le classi che implementano IDisposable e accedono risorse non gestite vengono istanziate in una dichiarazione Using per garantire che vengano correttamente eliminate.

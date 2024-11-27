---
title: Disegno di immagini usando GraphicsPath
type: docs
weight: 30
url: /it/net/drawing-images-using-graphicspath/
---

## **Disegno di immagini usando GraphicsPath**
La classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) è responsabile della creazione e del mantenimento di un percorso grafico. Il GraphicsPath non ha riferimento a un'immagine e non modifica direttamente l'immagine stessa; piuttosto, può essere considerato come un oggetto che contiene metadati che descrivono i percorsi che la classe Graphics può disegnare. La classe GraphicsPath utilizza figure; ogni figura è composta da una sequenza di linee e curve collegate o da primitive di forme geometriche. Ogni forma può essere divisa in segmenti di forma. È possibile aggiungere, rimuovere e modificare diverse figure o forme in un oggetto GraphicsPath. Una volta che il GraphicsPath è stato completamente descritto, utilizzare i metodi corrispondenti della classe Graphics (DisegnaPercorso e RiempiePercorsi) per disegnare o riempire i percorsi. La classe Graphics prende ciascun segmento di forma e lo disegna per produrre l'immagine finale.
### **Disegno usando la classe GraphicsPath**
Di seguito è riportato un esempio che dimostra l'uso della classe [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath). Il codice sorgente dell'esempio è stato suddiviso in diverse parti per mantenerlo semplice e facile da seguire. Passo dopo passo, gli esempi ti mostrano come:

- Creare un'immagine.
- Inizializzare un oggetto Graphics.
- Pulire la superficie.
- Creare un'istanza di [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Creare una figura.
- Aggiungere forme alla figura.
- Creare un array di figure.
- Disegnare percorsi.
- Riempire i percorsi.

### **Disegno di immagini usando GraphicsPath: Esempi di programmazione**
#### **GraphicsPath : Creare un'immagine**
Inizia creando un'immagine utilizzando uno qualsiasi dei metodi descritti in Creazione di file.
#### **GraphicsPath : Inizializzare un oggetto Graphics**
Crea e inizializza un oggetto Graphics passando l'oggetto Image al suo costruttore.
#### **GraphicsPath : Pulire la superficie**
Pulisci la superficie grafica chiamando il metodo Clear della classe Graphics e passa un colore come parametro. Questo metodo riempirà la superficie grafica con il colore passato come argomento.
#### **GraphicsPath : Creare un'istanza del GraphicsPath**
Crea un'istanza di GraphicsPath con GraphicsPath impostato su Alternate per impostazione predefinita. Questa modalità determina come riempire l'interno di una figura chiusa. L'ulteriore valore possibile di GraphicsPath è Winding.
#### **GraphicsPath : Creare una figura**
Crea un'istanza della classe Figure. Come discusso in precedenza, Figure può contenere Forme e le forme risiedono nello spazio dei nomi Aspose.PSD.Shapes.
#### **GraphicsPath : Aggiungere forme alla figura**
Il metodo Add Shapes esposto dalla classe Figure consente di aggiungere forme alla figura. Negli esempi di codice seguenti, diverse forme vengono aggiunte a un oggetto Figure.
#### **GraphicsPath : Aggiungere figure a un array**
È possibile aggiungere più figure a un oggetto GraphicsPath utilizzando il metodo AddFigures esposto dalla classe GraphicsPath. Questo metodo accetta un array di figure come parametro.
#### **GraphicsPath : Disegnare i percorsi**
Disegna il GraphicsPath utilizzando il metodo DrawPath esposto dalla classe Graphics. Il metodo accetta due parametri. Il primo parametro è un oggetto della classe Pen, che determina il colore, la larghezza e lo stile del percorso. Il secondo parametro è l'oggetto della classe GraphicsPath, che rappresenta il percorso stesso.
#### **GraphicsPath : Riempire i percorsi**


È possibile riempire un percorso passando un oggetto GraphicsPath al metodo RiempirePercorsi esposto dalla classe Graphics. Il metodo RiempirePercorsi riempie il percorso in base alla modalità di riempimento (Alternate o Winding) attualmente impostata per il percorso. Se il percorso ha delle figure aperte, il percorso viene riempito come se quelle figure fossero chiuse.

Il metodo RiempirePercorsi accetta due parametri. Il primo parametro è un oggetto di qualsiasi classe pennello dello spazio dei nomi Aspose.PSD.Brushes. Il secondo parametro è il percorso stesso. Per l'esempio in questione, utilizzare HatchBrush che è un pennello rettangolare con uno stile di trama, un colore di primo piano e un colore di sfondo. Prima di passare l'oggetto HatchBrush al metodo RiempirePercorsi, imposta le sue proprietà.
### **GraphicsPath : Codice sorgente completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



Tutte le classi che implementano IDisposable sono istanziate in una dichiarazione Using per garantire che vengano correttamente eliminate.

---
title: Disegno Immagini utilizzando GraphicsPath
type: docs
weight: 30
url: /it/java/drawing-images-using-graphicspath/
---

## **Disegno Immagini utilizzando GraphicsPath**
La classe GraphicsPath è responsabile della creazione e gestione di un percorso grafico. Il GraphicsPath non ha un riferimento a un'immagine e non modifica l'immagine stessa, invece, può essere considerato come un oggetto che contiene metadati che descrivono i percorsi che la classe Graphics può disegnare. La classe GraphicsPath utilizza figure; ogni figura è composta da una sequenza di linee e curve collegate o da una primitiva di forma geometrica. Ogni forma può essere divisa in segmenti di forma. È possibile aggiungere, rimuovere e modificare diverse figure o forme in un oggetto GraphicsPath. Quando il GraphicsPath è stato completamente descritto, utilizzare i relativi metodi della classe Graphics (DrawPath e Fill Paths) per disegnare sopra o riempire i percorsi. La classe Graphics prende ciascun segmento di forma e lo disegna per produrre l'immagine finale.
### **Disegno utilizzando la Classe GraphicsPath**
Di seguito è riportato un esempio che mostra l'utilizzo della classe GraphicsPath. Il codice sorgente dell'esempio è stato suddiviso in diverse parti per mantenerlo semplice e facile da seguire. Passo dopo passo, gli esempi ti mostrano come:

- Creare un'immagine.
- Inizializzare un oggetto Graphics.
- Cancella la superficie.
- Creare un'istanza di GraphicsPath.
- Creare una figura.
- Aggiungere forme alla figura.
- Creare un array di figure.
- Disegnare i percorsi.
- Riempire i percorsi.

### **Disegno Immagini utilizzando GraphicsPath: Esempi di Programmazione**
#### **GraphicsPath: Creare un'immagine**
Inizia creando un'immagine utilizzando uno dei metodi descritti in Creazione di file.
#### **GraphicsPath: Inizializzare un Oggetto Graphics**
Crea e inizializza un oggetto Graphics passando l'oggetto Image al suo costruttore.
#### **GraphicsPath: Cancella la Superficie**
Cancella la superficie grafica chiamando il metodo Clear della classe Graphics e passa un Colore come parametro. Questo metodo riempie la superficie grafica con il colore passato come argomento.
#### **GraphicsPath: Creare un'istanza di GraphicsPath**
Crea un'istanza di GraphicsPath con GraphicsPath impostato su Alternativo per impostazione predefinita. Questa modalità determina come riempire l'interno di una figura chiusa. L'altro possibile valore di GraphicsPath è Winding.
#### **GraphicsPath: Creare una Figura**
Crea un'istanza della classe Figure. Come discusso in precedenza, il Figure può contenere Shapes e le forme risiedono nello spazio dei nomi Aspose.PSD.Shapes.
#### **GraphicsPath: Aggiungere Forme alla Figura**
Il metodo Add Shapes esposto dalla classe Figure consente di aggiungere forme alla figura. Negli esempi di codice sottostanti, vengono aggiunte diverse forme a un oggetto di tipo Figure.
#### **GraphicsPath: Aggiungere Figure a un Array**
È possibile aggiungere più figure a un oggetto GraphicsPath utilizzando il metodo AddFigures esposto dalla classe GraphicsPath. Questo metodo accetta un array di figure come parametro.
#### **GraphicsPath: Disegnare i Percorsi**
Disegna il GraphicsPath utilizzando il metodo DrawPath esposto dalla classe Graphics. Il metodo accetta due parametri. Il primo parametro è un oggetto della classe Pen, che determina il colore, la larghezza e lo stile del percorso. Il secondo parametro è l'oggetto della classe GraphicsPath, che rappresenta il percorso stesso.
#### **GraphicsPath: Riempire i Percorsi**
È possibile riempire un percorso passando un oggetto GraphicsPath al metodo Fill Paths esposto dalla classe Graphics. Il metodo Fill Paths riempie il percorso secondo la modalità di riempimento (alternativa o winding) attualmente impostata per il percorso. Se il percorso ha delle figure aperte, il percorso viene riempito come se quelle figure fossero chiuse.

Il metodo Fill Paths accetta due parametri. Il primo parametro è un oggetto di qualsiasi classe di pennello dello spazio dei nomi Aspose.PSD.Brushes. Il secondo parametro è il percorso stesso. Per il bene di questo esempio, utilizza il HatchBrush che è un pennello rettangolare con uno stile di sbalzo, un colore primo piano e un colore di sfondo. Prima di passare l'oggetto HatchBrush al metodo Fill Paths, imposta le sue proprietà.
### **GraphicsPath: Sorgente Completa**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Sorgente-esempio-principale-java-com-aspose-psd-esempi-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}

Tutte le classi che implementano IDisposable vengono istanziate in una dichiarazione Using per garantire che vengano correttamente eliminate.

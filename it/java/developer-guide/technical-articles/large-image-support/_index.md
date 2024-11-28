---
title: Supporto per Immagini Grandi
type: docs
weight: 60
url: /it/java/supporto-immagini-grandi/
---

## **Supporto per Immagini Grandi**
Poiché la libreria Java standard ha alcune limitazioni riguardo alle dimensioni delle immagini che può elaborare, abbiamo introdotto un nuovo meccanismo di supporto per immagini grandi. Il nuovo approccio supera tali limitazioni, ma a causa delle limitazioni sulle dimensioni dei dati, le dimensioni massime supportate per la creazione e il caricamento sono di 2.147.483.647 x 2.147.483.647 pixel.
### **Lavorare con Immagini Grandi**
Aspose.PSD ha migliorato le prestazioni e il supporto per le immagini grandi. Le immagini di centinaia di megabyte di dimensioni non sono più un problema, quindi puoi crearle, caricarle e disegnare su di esse. Tuttavia, a causa del parziale trattamento ed elaborazione delle eccezioni di OutOfMemoryException, le prestazioni possono essere molto basse su immagini molto grandi. Questo è dovuto al fatto che Aspose.PSD cerca di riallocare una quantità minore di dati per l'elaborazione e ogni passaggio di riallocazione è molto costoso. I vantaggi della nuova architettura sono evidenti:

- Non c'è alcuna limitazione alle dimensioni delle immagini.
- Non sei limitato alla memoria disponibile sul tuo PC.

Se riscontri un'elaborazione lenta, si consiglia di aumentare la quantità totale di RAM per adattare tutti i tuoi pixel alla memoria. Se non lo fai, l'elaborazione è comunque possibile ma più lenta. L'approccio è il seguente:

- Chiamare il metodo LoadPartialPixels con il rettangolo desiderato e il delegato per ricevere i pixel caricati specificati.

Aspose.PSD cerca di caricare l'intero rettangolo.

- Se c'è abbastanza memoria per adattare tutti i pixel, allora tutti i pixel vengono semplicemente restituiti al chiamante.
- Se non c'è abbastanza memoria, il chiamante riceve un sottoinsieme di pixel dall'interno del rettangolo specificato. Quando quei pixel sono stati elaborati, il chiamante riceve il rettangolo successivo. L'elaborazione termina quando l'intero rettangolo è stato elaborato.

Aspose.PSD cerca di estrarre il maggior numero di righe possibile. Se non c'è abbastanza memoria per adattare una singola riga di pixel, allora una singola riga viene divisa in parti conformi ai rettangoli con altezza 1. Puoi anche disegnare su immagini grandi. Il processo di disegno cerca di influenzare l'intero rettangolo desiderato. Se non c'è abbastanza memoria, il disegno viene eseguito su rettangoli parziali finché l'intera area non è disegnata. Inoltre, Aspose.PSD supporta il salvataggio e l'esportazione di immagini grandi. Salva l'immagine di origine su disco o esportala in un altro formato di file. Il processo di salvataggio o esportazione viene eseguito utilizzando rettangoli parziali se necessario. 
### **Formati di Immagine Supportati**
I seguenti formati sono supportati per l'elaborazione di immagini grandi:

- BMP
- GIF
- TIFF
- PSD
- JPG
- PNG

I formati sopra indicati possono essere elaborati in modo sicuro attraverso creazione, modifica, applicazione di operazioni di disegno, salvataggio su disco o esportazione indipendentemente dalle dimensioni delle immagini.
.  

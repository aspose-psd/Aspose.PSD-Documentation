---
title: Supporto per Immagini Grandi
type: docs
weight: 40
url: /it/net/supporto-immagini-grandi/
---

## **Supporto per Immagini Grandi**
Poiché la libreria standard .NET ha alcune limitazioni riguardo alle dimensioni delle immagini che può elaborare, abbiamo introdotto un nuovo meccanismo per il supporto di immagini di grandi dimensioni. Il nuovo approccio supera le limitazioni, ma a causa delle limitazioni delle dimensioni dei dati, le dimensioni massime supportate per la creazione e il caricamento sono di 2,147,483,647 x 2,147,483,647 pixel.
### **Lavorare con Immagini Grandi**
Aspose.PSD ha migliorato le prestazioni e il supporto per le immagini di grandi dimensioni. Le immagini che sono grandi centinaia di megabyte non sono più un problema, quindi è possibile crearle, caricarle e disegnare su di esse. Tuttavia, a causa del parziale trattamento e della gestione delle eccezioni OutOfMemoryException, le prestazioni possono essere molto basse su immagini molto grandi. Questo è dovuto al fatto che Aspose.PSD cerca di ri-allocare una quantità più piccola di dati per il trattamento e ogni passaggio di riallocazione è molto costoso. I vantaggi della nuova architettura sono ovvi:

- Non ci sono limiti alle dimensioni dell'immagine.
- Non sei limitato alla memoria disponibile sul tuo PC.

Se riscontri un elaborazione lenta, si consiglia di aumentare la quantità totale di RAM per adattare tutti i tuoi pixel in memoria. In caso contrario, l'elaborazione è comunque possibile ma più lenta. L'approccio è il seguente:

- Chiama il metodo [LoadPartialPixels](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) con il rettangolo desiderato e il delegato per ricevere i pixel caricati specificati.

Aspose.PSD cerca di caricare l'intero rettangolo.

- Se c'è abbastanza memoria per adattare tutti i pixel, allora tutti i pixel vengono restituiti semplicemente al chiamante.
- Se non c'è abbastanza memoria, il chiamante riceve un sottoinsieme di pixel da all'interno del rettangolo specificato. Una volta che quei pixel sono stati elaborati, il chiamante riceve il rettangolo successivo. L'elaborazione termina quando l'intero rettangolo è stato elaborato.

Aspose.PSD cerca di estrarre il maggior numero possibile di righe. Se non c'è abbastanza memoria per adattare una singola riga di pixel, allora una singola riga viene divisa in parti conformi ai rettangoli con altezza 1. È anche possibile disegnare su immagini di grandi dimensioni. Il processo di disegno cerca di influenzare l'intero rettangolo desiderato. Se non c'è abbastanza memoria, il disegno viene eseguito su rettangoli parziali fino a quando l'intera area viene disegnata. Inoltre, Aspose.PSD supporta il salvataggio e l'esportazione di immagini di grandi dimensioni. Salva l'immagine di origine su disco o esportala in un altro formato di file. Il processo di salvataggio o esportazione viene eseguito utilizzando rettangoli parziali se necessario.
### **Formati di Immagini Supportati**
I seguenti formati sono supportati per l'elaborazione di immagini di grandi dimensioni:

- [BMP](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

I formati sopra menzionati possono essere elaborati in tutta sicurezza attraverso la creazione, la modifica, l'applicazione di operazioni di disegno, il salvataggio su disco o l'esportazione indipendentemente dalle dimensioni dell'immagine.

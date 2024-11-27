---
title: Elaborazione dei Dati Grezzi
type: docs
weight: 70
url: /it/java/elaborazione-dati-grezzi/
---

## **Elaborazione dei Dati Grezzi**
Per migliorare le prestazioni dell'API Aspose.PSD abbiamo introdotto un metodo per l'elaborazione dei dati grezzi con la versione 2.4.0. L'elaborazione dei dati grezzi è ora utilizzata internamente ed ha un'API esterna in modo che possa essere usata al di fuori della libreria per migliorare le prestazioni complessive. A volte l'elaborazione diventa un po' complicata e richiede qualche spiegazione. Attualmente, l'elaborazione dei dati grezzi è disponibile solo per il formato BMP.

Per aiutare gli sviluppatori ad ottenere le migliori prestazioni, l'API Aspose.PSD fornisce un sistema di elaborazione dei dati grezzi che ha un'API esterna per la personalizzazione. Gli sviluppatori chiamano i metodi LoadRawData e SaveRawData per utilizzare l'elaborazione dei dati grezzi. Questi metodi richiedono anche di impostare il formato desiderato dei dati grezzi utilizzando la classe RawDataSettings. La classe RawDataSettings consente agli sviluppatori di specificare qualsiasi formato dei dati grezzi. Tuttavia, per ottenere le migliori prestazioni è necessario utilizzare il formato dei dati grezzi in cui i dati sono memorizzati. Le RawDataSettings definite nella classe RasterImage aiutano a determinare il formato dei dati grezzi dell'immagine. Passando l'istanza RawDataSettings al metodo LoadRawData, i dati vengono restituiti così come sono, senza applicare alcuna conversione, e possono migliorare le prestazioni. D'altra parte, è necessario prendersi cura di tutti i possibili layout di formati dei dati grezzi che a volte possono essere un po' complicati.

Per semplificare il processo di gestione, a discapito di una penalità sulle prestazioni, è possibile specificare le RawDataSettings desiderate istanziando e inizializzando la classe con le impostazioni dei dati grezzi desiderate. Ci sono casi in cui non è possibile restituire i dati grezzi nel formato specificato (ad esempio la conversione dallo spazio colore CMYK a RGB non è disponibile nella versione 2.4.0). Inoltre, potrebbero esserci situazioni in cui l'elaborazione dei dati grezzi non è disponibile affatto per un formato di immagine. Per determinare se è possibile utilizzare i metodi della famiglia LoadRawData e SaveRawData è necessario controllare la proprietà IsRawDataAvailable.

### **Approfondimento**
Per il formato dei dati dei pixel RGB sono disponibili formati dei dati grezzi basati su palette e basati su RGB. I formati dei dati grezzi basati su palette contengono indici delle voci della palette nell'intervallo 0..(2^numero di bit - 1). I formati dei dati grezzi basati su palette sono 1, 2, 4 e 8 bit per pixel. Gli altri formati sono basati su RGB. Quando si caricano i dati grezzi, è importante assicurarsi che ci siano abbastanza byte disponibili per caricare i dati, altrimenti verrà generata un'eccezione appropriata. È possibile stimare semplicemente la dimensione dell'array di byte moltiplicando la dimensione della riga per le righe necessarie. La dimensione della riga può variare e dipende dal formato di memorizzazione dei dati grezzi.

Per ottenere le migliori prestazioni, utilizzare sempre una dimensione della linea dei dati grezzi pari al valore della proprietà RasterImage.RawLineSize. Tuttavia, a volte potrebbe essere necessario aggiungere un padding aggiuntivo alle righe dei dati grezzi, o ridurlo, e in tal caso potrebbe essere utilizzata una dimensione della linea diversa. Se è necessario un sottoinsieme del rettangolo di delimitazione di un'immagine, tenere conto degli spostamenti dei bit che potrebbero verificarsi per i formati dei dati dei pixel RGB indicizzati. Ad esempio, consideriamo un'immagine con dimensioni di 100x100 pixel e un formato dei dati grezzi di 1 bit per pixel. Si desidera caricare un rettangolo di dati grezzi con la posizione (7,0) e le dimensioni (2,1), o in altre parole, si richiedono 2 pixel a partire da x=7 e y=0. In questo caso, dovresti ricevere il seguente layout dei dati:



![todo:image_alt_text](raw-data-processing_1.png)

Ciò significa che ricevi 2 byte dove il primo byte contiene 7 pixel indesiderati, poi 1 pixel desiderato, e il secondo byte contiene 1 pixel desiderato e poi 7 indesiderati. Potresti chiederti perché non abbiamo eseguito uno spostamento dei dati e inserito quei 2 pixel in un singolo byte? La risposta è semplice: mantenere alte le prestazioni. Elaborare internamente i dati viene tipicamente eseguito con tutti i dati a partire dal primo pixel e finendo con l'ultimo pixel disponibile. Ci sono rare situazioni in cui è richiesto un sottoinsieme di pixel. Inoltre, non sappiamo come quei pixel verranno elaborati successivamente, quindi lo spostamento abbasserebbe le prestazioni e renderebbe il codice inutilmente complesso. Stima sempre il bit corretto (non è necessario determinare il byte corretto poiché i dati arrivano sempre con il primo byte pieno) da cui inizieranno i pixel richiesti. Per calcolare il bit corretto può essere utilizzata una semplice formula: (rect.Left * conteggio bit) % 8.

### **Conversione dei Colori RGB Indicizzati**
Per ottenere la massima prestazione possibile, utilizzare sempre le stesse impostazioni dei dati grezzi di origine e di destinazione, i formati dei pixel e le dimensioni delle linee. Tuttavia, a volte potrebbe essere necessario eseguire una conversione dei dati. Ad esempio, è possibile caricare un'immagine RGB con 1 bit per pixel e salvarla con 2 bit per pixel, o caricare un'immagine RGB a 4 bit e ridurne la gamma di colori a 2 bit per pixel. In entrambi i casi, è necessaria una conversione del colore. La conversione di immagini RGB indicizzate può essere a volte complicata e non può essere eseguita senza alcune impostazioni applicate. È necessario determinare come il range di colori di origine è mappato nello spazio dei colori di destinazione. Per completare questo compito abbiamo diversi modi:

- Mappatura della palette (DitheringMethods.PaletteConversion)
- Mappatura dei dati grezzi (DitheringMethods.PaletteIgnore)
- Conversione personalizzata (DitheringMethods.CustomConverter)

Quando viene utilizzata la conversione della palette, lo spazio colore di origine cerca di corrispondere il più possibile allo spazio colore di destinazione. Ad esempio supponiamo di avere un'immagine a 4 bit con i seguenti colori:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

L'immagine di origine appare come segue:



![todo:image_alt_text](raw-data-processing_2.png)

E convertiamo l'immagine a 4 bit in un'immagine a 1 bit con le seguenti definizioni dei colori della palette:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Nella modalità di conversione della palette, il convertitore legge il colore di origine e determina l'indice di destinazione utilizzando il metodo GetNearestColorIndex della palette di destinazione. Il valore della proprietà RasterImage.RawFallbackIndex viene utilizzato nel caso in cui il metodo GetNearestColorIndex della palette restituisce un indice fuori campo. Ciò converte i colori di origine nei colori di destinazione più vicini in termini di valori di intensità. L'immagine di destinazione corrisponde il più possibile all'immagine di origine. È possibile vedere il seguente risultato:



![todo:image_alt_text](raw-data-processing_3.png)

Nella modalità di mappatura dei dati grezzi viene utilizzato uno scenario diverso. Le palette dei colori di origine e di destinazione sono semplicemente ignorate e gli indici di origine vengono mappati sugli indici di destinazione. Quando viene trovato un valore che non può essere mappato nel range di destinazione (quando si riducono i conteggi dei bit), allora viene utilizzato il valore della proprietà RasterImage.RawFallbackIndex. Il valore è 0 per impostazione predefinita e viene mappato sul primo colore nella palette di destinazione. Se il valore di questa proprietà si trova al di fuori del range di destinazione, verrà generata un'eccezione appropriata. Ciò porta a risultati meno prevedibili che possono essere mostrati nella seguente immagine:



![todo:image_alt_text](raw-data-processing_4.png)

La modalità di conversione della palette è una soluzione più corretta per il problema di mappatura dei colori, ma richiede anche un po' più di tempo per completare poiché è necessario eseguire calcoli per stimare la mappatura delle palette corretta. (Tipicamente c'è una differenza di prestazioni molto piccola tra i due metodi). D'altra parte, la modalità di mappatura dei dati grezzi si esegue un po' più velocemente e può essere utilizzata per una conversione più approssimativa del colore quando la mappatura esatta dei colori non è così importante. Ad esempio, ci sono casi in cui la palette dei colori di origine è ridotta e può essere tranquillamente convertita a conteggi di bit inferiori poiché i bit aggiuntivi non sono stati comunque utilizzati.

Per utilizzare uno qualsiasi di questi approcci, utilizzare la proprietà RawDitheringMethod della classe RasterImage. Per impostazione predefinita, è impostato sul metodo di conversione della palette per ottenere i risultati migliori in termini di aspetto. È possibile modificare questa proprietà prima che venga effettuata qualsiasi conversione (ad esempio al salvataggio dell'immagine su uno stream). Si noti che i metodi di dithering di conversione della palette e di ignorare la palette non avranno luogo se si è caricata un'immagine e si sono riscritti alcuni dei dati pixel originali poiché i nuovi dati vanno nella cache e la cache memorizza i dati nel formato massimo disponibile 32ARGB (a partire dalla versione 2.4.0, soggetto a modifiche). Questo formato viene utilizzato per superare i problemi con possibili differenti gamma di colori per le immagini caricate e salvate. Inoltre, i metodi di dithering di ignorare la palette e di conversione della palette verranno ignorati quando un'immagine viene caricata in modalità RGB e convertita in modalità indicizzata o viceversa.

### **Convertitori Colori Personalizzati**
A volte non è sufficiente utilizzare l'approccio standard per la conversione dei colori. Potresti desiderare utilizzare un algoritmo personalizzato per avere la massima libertà durante l'utilizzo delle routine di conversione dei colori. Quando i formati dei pixel delle immagini sorgente e di destinazione sono entrambi formati RGB indicizzati, può essere utilizzata un'interfaccia più semplice, IIndexedColorConverter. È necessario impostare la proprietà RasterImage.RawIndexedColorConverter su un'istanza dell'interfaccia IIndexedColorConverter e utilizzare il valore DitheringMethods.CustomConverter per la proprietà RawDitheringMethod. Quando viene applicata questa combinazione, qualsiasi conversione dei colori indicizzati passa attraverso quell'istanza specificata di IIndexedColorConverter. Il convertitore di colori indicizzati personalizzati ha il seguente metodo definito:

{{< highlight java >}}
 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}

Il metodo FillIndexedtoIndexedMap viene chiamato quando è richiesta una conversione da un'immagine RGB indicizzata a un formato di immagine RGB indicizzato (quando uno qualsiasi dei conteggi di 1,2,4 o 8 bit viene convertito tra loro). L'array di mappe ha una lunghezza pari al conteggio di tutte le possibili voci del formato di origine. È necessario riempire tale array per mappare l'entrata della paletta del colore di origine all'entrata della paletta del colore di destinazione. Assicurati che il valore dell'indice di destinazione sia nell'intervallo 0..(conteggi di bit - 1), altrimenti verrà generata un'eccezione appropriata.

Se il requisito è quello di eseguire uno scenario di conversione dei colori più personalizzato, allora la proprietà RasterImage.RawCustomColorConverter dovrebbe essere impostata su un'istanza dell'interfaccia IColorConverter. La proprietà RawCustomColorConverter sostituisce sempre la proprietà RawIndexedColorConverter se entrambe sono impostate e non verrà utilizzato un convertitore di colori indicizzati in tal caso. IColorConverter ha un solo metodo:

{{< highlight java >}}
 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}

Il metodo Convert viene chiamato ogni volta che è necessaria la conversione del colore. Il metodo riceve i dati grezzi di origine nel formato di origine e ha un buffer di output per ricevere il colore convertito nel formato di destinazione. Il buffer di destinazione dovrebbe essere sufficiente per ricevere i dati convertiti (se la chiamata dell'interfaccia è fatta internamente dalla libreria Aspose.PSD) e dovrebbe contenere i dati grezzi convertiti al ritorno del metodo. Il metodo Convert può essere chiamato più volte fino a quando tutti i dati di origine sono coperti.
---
title: Manipolazione delle immagini TIFF
type: docs
weight: 40
url: /it/java/manipolazione-immagini-tiff/
---

## **Aggiungere frame con diverse impostazioni**
TIFF è un formato molto flessibile che consente di aggiungere frame diversi, con diverse dimensioni, compressione e altre impostazioni. Le API Aspose.PSD ti permettono di aggiungere qualsiasi frame TIFF di qualsiasi dimensione, il che aiuta a creare documenti complessi. Se c'è la necessità di regolare i frame durante il processo di aggiunta per renderli tutti uguali, eseguire i seguenti passaggi:

- Creare un nuovo frame vuoto con le opzioni desiderate o copiare il frame di origine con le opzioni di output specificate utilizzando il metodo CreateFrameFrom.
- Ridimensionare il frame / immagine di origine alle dimensioni desiderate utilizzando il metodo Resize.
- Aggiungere i pixel del frame / immagine di origine al nuovo frame.
- Aggiungere il nuovo frame all'immagine TIFF di output.

## **Esporta strati dell'immagine PSD in un file TIFF multipagina**
A volte è necessario esportare gli strati dell'immagine PSD nel formato file TIFF multipagina. Questo articolo dimostrerà come possiamo eseguire questa operazione utilizzando l'API Aspose.PSD per Java. Per prima cosa, caricheremo l'immagine PSD dal disco. Poi itereremo sugli strati dell'immagine PSD e creeremo un TiffFrame dagli strati corrispondenti. Infine salveremo l'immagine TIFF risultante in un unico file su disco.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Configurazione di TiffOptions**


I programmatori possono regolare diverse proprietà della classe Tiffoptions per ottenere i risultati desiderati. In questo documento, ci concentreremo su 4 proprietà principali che controllano gli attributi dell'immagine risultante.

Queste proprietà sono elencate di seguito.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Ogni volta che iniziamo una struttura Tiffoptions vuota, ogni opzione viene impostata sul suo valore predefinito, ad esempio la compressione è impostata su Nessuna, BitsPerSample è impostato su 1 e Photometric su MinIsWhite. Salvando in questo formato l'immagine finale sarà in bianco e nero e questo è il comportamento atteso per tale combinazione di opzioni. Per ottenere i risultati a colori è necessario impostare tutte le proprietà menzionate sopra su valori che corrispondono allo spazio colore desiderato oppure è possibile inizializzare la struttura Tiffoptions con impostazioni predefinite come discusso successivamente in questo articolo. Di seguito è riportata una tabella che descrive i valori dei parametri attesi che è possibile impostare per ottenere i risultati desiderati. Si noti che è necessario impostare tutte e 4 le colonne tramite Tiffoptions per salvare qualsiasi immagine carica/creata nel formato file TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Non compresso|1/4/8/16 (palette, modalità colore) solo un canale|Nessuno|
|MinIsWhite/MinIsBlack|LZW/Non compresso|1/4/8/16 (modalità scala di grigi) solo un canale|Nessuno|
|Palette|LZW/Non compresso|8 (palette, modalità colore) solo un canale|Orizzontale (maggior compressione ottenuta per LZW con stessi pattern)|
|MinIsWhite/MinIsBlack|LZW/Non compresso|8 (modalità scala di grigi) solo un canale|Orizzontale (maggior compressione ottenuta per LZW con stessi pattern)|
|RGB|LZW/Non compresso|[8,8,8] (3 canali RGB)|Nessuno/Orizzontale|
|RGB|LZW/Non compresso|[8,8,8,8] (3 canali RGB e può essere impostato ulteriormente un canale alfa attraverso TiffOptions.AlphaStorage) In realtà è supportato qualsiasi numero di canali aggiuntivi ma ogni canale deve avere una dimensione di 8 bit come [8,8,8,8,8,8]|Nessuno/Orizzontale|
Tutte e 4 le proprietà devono essere impostate tramite TiffOptions per salvare qualsiasi formato immagine nel formato file Tiff. Utilizzando diverse combinazioni, alcuni visualizzatori (incluso il Visualizzatore foto di Windows) potrebbero rifiutarsi di renderizzare l'immagine risultante a causa del supporto limitato offerto. In tal caso, si prega di scegliere un visualizzatore diverso per i test.
### **Impostazioni predefinite per la classe TiffOptions**
Per facilitare gli utenti e evitare la configurazione errata dell'istanza Tiffoptions, l'API Aspose.PSD per Java ha esposto un altro costruttore che accetta un parametro di tipo TiffExpectedFormat. In base al valore selezionato dall'enumerazione TiffExpectedFormat, l'API configura automaticamente tutte le proprietà obbligatorie per l'istanza di Tiffoptions al fine di produrre i risultati desiderati. Prima di passare al codice di esempio, qui è elencato l'elenco dei campi di TiffExpectedFormat e i loro dettagli per una migliore comprensione dell'utilizzo.



- TiffExpectedFormat.Default: L'impostazione del campo su Default agisce in modo simile al costruttore predefinito della classe Tiffoptions senza impostare alcuna compressione e BitsPerPixel impostato su 1 per produrre un risultato in bianco e nero. Si consiglia di utilizzare questo campo quando altre proprietà specifiche del formato devono essere impostate manualmente in base ai risultati desiderati.
- TiffExpectedFormat.TiffCcitRle: Specifico per la codifica RLE durante il salvataggio del risultato nel formato file TIFF a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffCcittFax3: Specifico per la codifica CCITT Fax3 durante il salvataggio del risultato nel formato file TIFF a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffCcittFax4: Specifico per la codifica CCITT Fax4 durante il salvataggio del risultato nel formato file TIFF a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffDeflateBW: Specifico per la compressione Deflate durante il salvataggio del risultato nel formato file TIFF a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffDeflateRGB: Specifico per la compressione Deflate durante il salvataggio del risultato nel formato file TIFF RGB (colore).
- TiffExpectedFormat.TiffJpegRGB: Specifico per la compressione Jpeg durante il salvataggio del risultato nel formato file TIFF RGB (colore).
- TiffExpectedFormat.TiffJpegYCBCR: Specifico per la compressione Deflate durante il salvataggio del risultato nel formato file TIFF YCBCR (colore).
- TiffExpectedFormat.TiffLzwBW: Specifico per la compressione LZW durante il salvataggio del risultato nel formato file TIFF a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffLzwRGB: Specifico per la compressione LZW durante il salvataggio del risultato nel formato file TIFF RGB (colore).
- TiffExpectedFormat.TiffLzwRGBA: Specifico per la compressione LZW durante il salvataggio del risultato nel formato file TIFF RGBA (colore con trasparenza).
- TiffExpectedFormat.TiffNoCompressionBW: Specifico per il formato TIFF non compresso durante il salvataggio del risultato a 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffNoCompressionRGB: Specifico per il formato TIFF non compresso durante il salvataggio del risultato in RGB (colore).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specifico per il formato TIFF non compresso durante il salvataggio del risultato in RGBA (colore con trasparenza).



Il seguente frammento di codice illustra l'utilizzo dei campi TiffExpectedFormat durante la creazione di un'istanza della classe Tiffoptions.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Supporto per la compressione Deflate e Adobe Deflate**
Il formato file TIFF (Tagged Image File Format) supporta vari tipi di compressione, mentre il tipo di compressione è memorizzato come un tag (un valore intero) nel file. Uno di questi metodi di compressione è l'Adobe Deflate (precedentemente noto come Deflate). L'API Aspose.PSD per Java supporta questo metodo di compressione per l'esportazione e la creazione di immagini TIFF.
### **Salvataggio dell'immagine in TIFF con compressione Deflate**
Convertire le immagini caricate in TIFF con compressione Deflate/Adobe Deflate è facile come segue.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Creazione di un'immagine Tiff con compressione Adobe Deflate**
Di seguito è mostrato un esempio che illustra l'utilizzo dell'API Aspose.PSD per Java per creare un'immagine da zero utilizzando il metodo di compressione Adobe Deflate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Compressione delle immagini TIFF**
L'API Aspose.PSD per Java può essere utilizzata per convertire immagini PSD nel formato immagine TIFF e persino cambiare la compressione dell'immagine TIFF risultante. L'API può anche essere utilizzata per memorizzare diverse immagini come frame in un'immagine TIFF per scopi di archiviazione riducendo le dimensioni dei dati delle immagini alla loro dimensione più piccola. La compressione dell'immagine in ogni caso dovrebbe essere eseguita riducendo le dimensioni dei dati di origine indipendentemente dall'algoritmo di compressione utilizzato. Per ottenere il miglior rapporto di compressione, possiamo utilizzare spazi colore indicizzati. Il frammento di codice fornito di seguito esegue la migliore compressione utilizzando solo 16 colori indicizzati e l'algoritmo di compressione LZW tuttavia i colori di origine sono leggermente dithered.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-main-java-com-aspose-psd-esempi-ModificheEConversioniImmagini-TIFF-CompressioneTiff-CompressioneTiff.java" >}}

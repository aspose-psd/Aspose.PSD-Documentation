---
title: Manipolazione Immagini TIFF
type: docs
weight: 50
url: /it/manipolazione-immagini-tiff/
---

## **Aggiungere Cornici con Impostazioni Diverse**
TIFF è un formato molto flessibile che consente di aggiungere cornici diverse, con diverse dimensioni, compressione e altre impostazioni. Le API di Aspose.PSD ti consentono di aggiungere qualsiasi cornice TIFF di qualsiasi dimensione, il che aiuta nella creazione di documenti complessi. Se c'è la necessità di regolare le cornici durante il processo di aggiunta per renderle tutte uguali, eseguire i seguenti passaggi:

- Creare una nuova cornice vuota con le opzioni desiderate o copiare la cornice di origine con le opzioni di output specificate utilizzando il metodo CreateFrameFrom.
- Ridimensionare la cornice/immagine di origine alle dimensioni desiderate utilizzando il metodo Resize.
- Aggiungere i pixel della cornice/immagine di origine alla nuova cornice.
- Aggiungere la nuova cornice all'immagine TIFF di output.

## **Esportare livelli di immagine PSD in formato file Tiff Multi-pagina**
A volte è necessario esportare i livelli di immagine PSD in formato file TIFF multi-pagina. Questo articolo dimostrerà come è possibile eseguire questa attività utilizzando Aspose.PSD per .NET API. Prima caricheremo l'immagine PSD dal disco. Successivamente itereremo sui livelli di immagine PSD e creeremo TiffFrame dai livelli corrispondenti. Infine salveremo l'immagine Tiff risultante in un singolo file su disco.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConversioneImmagini-TIFF-EsportaInTiffMultiPagina-EsportaInTiffMultiPagina.cs" >}}
## **Configurazione TiffOptions**
I programmatori possono regolare diverse proprietà della classe [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) per ottenere i risultati desiderati. In questo documento, ci concentreremo su 4 proprietà principali che controllano gli attributi dell'immagine risultante.

Queste proprietà sono elencate di seguito.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Ogni volta che inizializziamo una struttura TiffOptions vuota, ciascuna opzione viene impostata sul suo valore predefinito, ad esempio la compressione è impostata su Nessuna, BitsPerSample è impostato su 1 e Photometric come MinIsWhite. Salvare in questo formato renderà l'immagine finale in bianco e nero e questo è il comportamento atteso per tale combinazione di opzioni. Per ottenere i risultati a colori è necessario impostare tutte le proprietà menzionate sopra su valori che corrispondono allo spazio dei colori desiderato oppure è possibile inizializzare la struttura TiffOptions con impostazioni predefinite come discusso più avanti in questo articolo. Di seguito è riportata una tabella che descrive i valori dei parametri attesi che è possibile impostare per ottenere i risultati desiderati. Si prega di notare che è necessario impostare tutte e 4 le colonne tramite TiffOptions per salvare qualsiasi immagine caricata/creata nel formato TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Non compresso|1/4/8/16 (logica palette, modalità colore) un solo canale|Nessuno|
|MinIsWhite/MinIsBlack|LZW/Non compresso|1/4/8/16 (modalità scala di grigi) un solo canale|Nessuno|
|Palette|LZW/Non compresso|8 (logica palette, modalità colore) un solo canale|Orizzontale (maggior compressione ottenuta per LZW stessi pattern)|
|MinIsWhite/MinIsBlack|LZW/Non compresso|8 (modalità scala di grigi) un solo canale|Orizzontale (maggior compressione ottenuta per LZW stessi pattern)|
|RGB|LZW/Non compresso|[8,8,8] (3 canali RGB)|Nessuno/Orizzontale|
|RGB|LZW/Non compresso|[8,8,8,8] (3 canali RGB e canale alfa aggiuntivo può essere impostato tramite TiffOptions.AlphaStorage) In realtà è supportato un qualsiasi numero di canali aggiuntivi ma ogni canale deve avere dimensioni di 8 bit come [8,8,8,8,8,8]|Nessuno/Orizzontale|
Tutte e 4 le proprietà devono essere impostate tramite TiffOptions per salvare qualsiasi formato immagine in formato Tiff. Quando si utilizzano diverse combinazioni, alcuni visualizzatori (incluso il Visualizzatore Foto di Windows) potrebbero rifiutarsi di renderizzare l'immagine risultante a causa del supporto limitato che offrono. In tal caso, si prega di scegliere un visualizzatore diverso per i test.
### **Impostazioni Predefinite per la Classe TiffOptions**
Al fine di facilitare agli utenti e evitare la configurazione errata dell'istanza TiffOptions, l'API Aspose.PSD per .NET ha esposto un altro costruttore che accetta un parametro di tipo [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). In base al valore selezionato dall'enumerazione TiffExpectedFormat, l'API configura automaticamente tutte le proprietà obbligatorie per l'istanza di TiffOptions al fine di produrre i risultati desiderati. Prima di passare al codice di esempio, ecco l'elenco dei campi di TiffExpectedFormat e i loro dettagli per una migliore comprensione dell'uso.


- TiffExpectedFormat.Default: Impostando il campo su Default agisce in modo simile al costruttore predefinito della classe TiffOptions senza alcuna compressione impostata e BitsPerPixel impostato su 1 per produrre un risultato in bianco e nero. Si consiglia di utilizzare questo campo quando altre proprietà specifiche del formato devono essere impostate manualmente in base ai risultati desiderati.
- TiffExpectedFormat.TiffCcitRle: Specifico per la codifica RLE durante il salvataggio del risultato nel formato TIFF 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffCcittFax3: Specifico per la codifica CCITT Fax3 durante il salvataggio del risultato nel formato TIFF 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffCcittFax4: Specifico per la codifica CCITT Fax4 durante il salvataggio del risultato nel formato TIFF 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffDeflateBW: Specifico per la compressione Deflate durante il salvataggio del risultato nel formato TIFF 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffDeflateRGB: Specifico per la compressione Deflate durante il salvataggio del risultato nel formato TIFF RGB (a colori).
- TiffExpectedFormat.TiffJpegRGB: Specifico per la compressione Jpeg durante il salvataggio del risultato nel formato TIFF RGB (a colori).
- TiffExpectedFormat.TiffJpegYCBCR: Specifico per la compressione JPEG durante il salvataggio del risultato nel formato TIFF YCBCR (a colori).
- TiffExpectedFormat.TiffLzwBW: Specifico per la compressione LZW durante il salvataggio del risultato nel formato TIFF 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffLzwRGB: Specifico per la compressione LZW durante il salvataggio del risultato nel formato TIFF RGB (a colori).
- TiffExpectedFormat.TiffLzwRGBA: Specifico per la compressione LZW durante il salvataggio del risultato nel formato TIFF RGBA (a colori con trasparenza).
- TiffExpectedFormat.TiffNoCompressionBW: Specifico per il formato TIFF non compresso durante il salvataggio del risultato in 1 BitsPerPixel (bianco e nero).
- TiffExpectedFormat.TiffNoCompressionRGB: Specifico per il formato TIFF non compresso durante il salvataggio del risultato in RGB (a colori).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specifico per il formato TIFF non compresso durante il salvataggio del risultato in RGBA (a colori con trasparenza).



Il seguente snippet di codice illustra l'uso dei campi TiffExpectedFormat durante la creazione di un'istanza della classe TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConversioneImmagini-TIFF-ConfigurazioneTiffOptions-TiffOptionsConfiguration.cs" >}}
## **Supporto per la Compressione Deflate e Adobe Deflate**
Il formato file TIFF (Tagged Image File Format) supporta vari tipi di compressione, mentre il tipo di compressione è memorizzato come un tag (un valore intero) nel file. Uno dei metodi di compressione è Adobe Deflate (precedentemente noto come Deflate). L'API di Aspose.PSD per .NET supporta questo metodo di compressione per l'esportazione e la creazione di immagini TIFF.
### **Salvataggio Immagine in TIFF con Compressione Deflate**
Convertire le immagini caricate in TIFF con compressione Deflate/Adobe Deflate è facile come segue.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConversioneImmagini-TIFF-TIFFconCompressioneDeflate-TIFFconCompressioneDeflate.cs" >}}
### **Creazione di TiffImage con Compressione Adobe Deflate**
Il campione fornito di seguito dimostra l'uso di Aspose.PSD per l'API .NET per creare un'immagine da zero utilizzando il metodo di compressione Adobe Deflate.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConversioneImmagini-TIFF-TIFFconCompressioneAdobeDeflate-TIFFconCompressioneAdobeDeflate.cs" >}}
### **Compressione Immagini TIFF**
L'API di Aspose.PSD per .NET può essere utilizzata per convertire immagini PSD nel formato immagine TIFF e anche modificare la compressione dell'immagine TIFF risultante. L'API può anche essere utilizzata per archiviare diverse immagini come frame in un'immagine TIFF a scopo di archiviazione, riducendo le dimensioni dei dati delle immagini. La compressione dell'immagine in ogni caso dovrebbe essere eseguita riducendo le dimensioni dei dati di origine indipendentemente dall'algoritmo di compressione utilizzato. Per ottenere il miglior rapporto di compressione possiamo utilizzare spazi di colori indicizzati. Il frammento di codice fornito di seguito esegue la migliore compressione utilizzando solo 16 colori indicizzati e l'algoritmo di compressione LZW, tuttavia i colori di origine sono leggermente ditherati.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConversioneImmagini-TIFF-ComprimiTiff-ComprimiTiff.cs" >}}

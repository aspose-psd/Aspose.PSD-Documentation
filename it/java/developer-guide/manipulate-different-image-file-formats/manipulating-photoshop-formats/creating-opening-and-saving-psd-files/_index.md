---
title: Creazione, Apertura e Salvataggio File PSD
type: docs
weight: 10
url: /it/creazione-apertura-e-salvataggio-file-psd/
---

## **Esportare Immagine in PSD**
PSD, documento PhotoShop, è il formato di file predefinito utilizzato da Adobe PhotoShop per lavorare con le immagini. Aspose.PSD ti permette di caricare, modificare e salvare file in formato PSD in modo che possano essere aperti e modificati in PhotoShop. Questo articolo mostra come salvare un file in PSD con Aspose.PSD e discute anche alcune delle impostazioni che possono essere utilizzate durante il salvataggio in questo formato. PsdOptions è una classe specializzata nello spazio dei nomi ImageOptions utilizzata per esportare immagini in PSD. Per esportare in PSD, crea un'istanza della classe Image, caricata da un file immagine esistente (ad esempio miniature) o creata da zero. Questo articolo spiega come. Negli esempi qui sotto, un'immagine viene creata da zero. Una volta creata e i dati dei pixel popolati, salva l'immagine utilizzando il metodo di salvataggio della classe Image, e fornisci un oggetto PsdOptions come secondo argomento. Diverse proprietà della classe PsdOptions possono essere impostate per una conversione avanzata. Alcune delle proprietà sono ColorMode, CompressionMethod e Version. Aspose.PSD supporta i seguenti metodi di compressione attraverso l'enumerazione CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

I seguenti modi di colore sono supportati attraverso l'enumerazione ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Sono disponibili risorse aggiuntive, come risorse miniature per PSD v4.0, v5.0 e superiori, o risorse griglia e guida per PSD v4.0 e superiori. Il codice qui sotto crea un file BMP da zero, popola i pixel e lo salva in PSD con compressione RLE e modalità di colore in scala di grigi. Il seguente snippet di codice ti mostra come esportare un'immagine in PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-principale-java-com-aspose-psd-esempi-ModificaEConversiaImmagini-PSD-EsportaImmagineInPSD-EsportaImmagineInPSD.java" >}}

## **Importare immagine in un livello PSD**
Questo articolo dimostra l'uso di Aspose.PSD per aggiungere o importare un'immagine in un livello PSD. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto il metodo DrawImage della classe Layer per aggiungere/importare un'immagine in un file PSD. Il metodo DrawImage ha bisogno di valori di posizione e immagine per aggiungere/importare un'immagine in un file PSD. I passaggi per importare un'immagine in un livello PSD sono semplici come segue:

- Carica un file PSD come un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
- Crea un'istanza della classe Layer e assegna l'immagine PSD del livello ad essa.
- Carica l'immagine che deve essere aggiunta o creane una da zero.
- Chiama il metodo Layer.DrawImage specificando la posizione e l'istanza dell'immagine.
- Salva i risultati.

Il seguente snippet di codice ti mostra come importare un'immagine in un livello PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-principale-java-com-aspose-psd-esempi-ModificaEConversiaImmagini-PSD-ImportaImmagineInLivelloPSD-ImportaImmagineInLivelloPSD.java" >}}

## **Creare miniature dai file PSD**
PSD è il formato di documento nativo dell'applicazione Photoshop di Adobe. Adobe Photoshop (versione 5.0 e successiva) conserva informazioni sulla miniatura per la visualizzazione del preview in un blocco di risorse immagine che consiste in un'intestazione iniziale di 28 byte, seguita da una miniatura JFIF in ordine RGB (rosso, verde, blu). L'API di Aspose.PSD fornisce un meccanismo facile da usare per accedere alle risorse dei file PSD. Queste risorse includono anche la risorsa miniatura che a sua volta può essere recuperata e salvata su disco secondo le esigenze dell'applicazione. Il seguente snippet di codice ti mostra come creare miniature dai file PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-principale-java-com-aspose-psd-esempi-ModificaEConversiaImmagini-PSD-CreaMiniatureDaFilePSD-CreaMiniatureDaFilePSD.java" >}}

## **Creare File PSD Indicizzati**
Aspose.PSD for Java API può creare file PSD Indicizzati da zero. Questo articolo dimostra l'uso delle classi PsdOptions e PsdImage per creare un PSD Indicizzato mentre si disegnano alcune forme sul canvas appena creato. I seguenti semplici passaggi sono necessari per creare un file PSD Indicizzato.

- Crea un'istanza di PsdOptions e imposta la sua sorgente.
- Imposta la proprietà ColorMode di PsdOptions su ColorModes.Indexed.
- Crea una nuova tavolozza di colori dallo spazio RGB e impostala come proprietà Palette di PsdOptions.
- Imposta la proprietà CompressionMethod sull'algoritmo di compressione richiesto.
- Crea una nuova immagine PSD chiamando il metodo PsdImage.Create.
- Disegna grafica o esegui altre operazioni come richiesto.
- Chiama il metodo PsdImage.Save per confermare tutte le modifiche.

Il seguente snippet di codice ti mostra come creare file PSD indicizzati.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-principale-java-com-aspose-psd-esempi-ModificaEConversiaImmagini-PSD-CreaFilePSDIndicizzati-CreaFilePSDIndicizzati.java" >}}

## **Esportare un Livello PSD in un'Immagine Raster**
Aspose.PSD per Java ti permette di esportare livelli in un file PSD in immagini raster. Per favore utilizza il metodo Save della classe Aspose.PSD.FileFormats.Psd.Layers.Layer per esportare il livello in immagine. Il seguente codice di esempio carica un file PSD ed esporta ciascuno dei suoi livelli in un'immagine PNG utilizzando il metodo Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Una volta che tutti i livelli sono esportati in immagini PNG, puoi aprirli utilizzando il tuo visualizzatore di immagini preferito. Il seguente snippet di codice ti mostra come esportare un livello PSD in un'immagine raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Esempi-src-principale-java-com-aspose-psd-esempi-ModificaEConversiaImmagini-PSD-EsportaLivelloPSDInImmagineRaster-EsportaLivelloPSDInImmagineRaster.java" >}}

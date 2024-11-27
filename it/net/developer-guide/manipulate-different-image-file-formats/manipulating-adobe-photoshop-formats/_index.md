---
title: Manipolazione dei Formati di Adobe Photoshop
type: docs
weight: 20
url: /it/manipolazione-dei-formati-di-adobe-photoshop/
---

## **Unire livelli PSD in altri livelli**

## **Esportare Immagine in PSD**
PSD, documento PhotoShop, è il formato di file predefinito utilizzato da Adobe Photoshop per lavorare con le immagini. Aspose.PSD ti consente di caricare, modificare e salvare file in formato PSD in modo che possano essere aperti e modificati in Photoshop. Questo articolo mostra come salvare un file in formato PSD con Aspose.PSD e discute anche alcune delle impostazioni che possono essere utilizzate durante il salvataggio in questo formato. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) è una classe specializzata nello spazio dei nomi [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) utilizzata per esportare immagini in PSD. Per esportare in PSD, crea un'istanza della classe Image, caricata da un file immagine esistente (ad esempio miniature) o creata da zero. Questo articolo spiega come. Negli esempi seguenti, un'immagine viene creata da zero. Una volta creata e popolati i dati dei pixel, salvare l'immagine utilizzando il metodo Save della classe Image e fornire un oggetto PsdOptions come secondo argomento. Diverse proprietà della classe PsdOptions possono essere impostate per una conversione avanzata. Alcune delle proprietà sono ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) e Versione. Aspose.PSD supporta i seguenti metodi di compressione attraverso l'enumerazione CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

I seguenti modi di colore sono supportati tramite l'enumerazione [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Scala di grigi
- ColorModes.RGB


È possibile aggiungere risorse aggiuntive, come risorse miniatura per PSD v4.0, v5.0 e superiori, o risorse griglia e guida per PSD v4.0 e superiori. Il codice sottostante crea un file immagine da zero, popola i pixel e lo salva in PSD con compressione RLE e modalità di colore in scala di grigi. Il seguente frammento di codice mostra come esportare un'immagine in PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Importare immagine in un livello PSD**
Questo articolo illustra l'uso di Aspose.PSD per aggiungere o importare un'immagine in un livello PSD. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto il metodo [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) della classe Layer per aggiungere/importare un'immagine in un file PSD. Il metodo DrawImage ha bisogno di valori di posizione e immagine per aggiungere/importare un'immagine in un file PSD. I passaggi per importare un'immagine in un livello PSD sono semplici come segue:

- Caricare un file PSD come immagine utilizzando il metodo factory Load esposto dalla classe Image.
- Creare un'istanza della classe Layer dal flusso con file Png, Jpeg, Tiff, Gif, Bmp, Psd o j2k
- Aggiungere il livello a Psd utilizzando il metodo AddLayer
- Salvare i risultati.


Il seguente frammento di codice mostra come importare l'immagine nel livello PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Sostituzione dei colori nei livelli PSD**
Questo articolo illustra l'uso di Aspose.PSD per aggiungere o importare un'immagine in un livello PSD. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto il metodo DrawImage della classe Layer per aggiungere/importare un'immagine in un file PSD. Il metodo DrawImage ha bisogno di valori di posizione e immagine per aggiungere/importare un'immagine in un file PSD. I passaggi per importare un'immagine in un livello PSD sono semplici come segue:

- Caricare un file PSD come immagine utilizzando il metodo factory Load esposto dalla classe Image.
- Creare un'istanza della classe Layer e assegnare il livello dell'immagine PSD ad esso.
- Caricare l'immagine che deve essere aggiunta o crearne una da zero.
- Chiamare il metodo Layer.DrawImage specificando posizione e istanza di immagine.
- Salvare i risultati.


Il seguente frammento di codice mostra come importare un'immagine in un livello PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Creazione di miniature da file PSD**
PSD è il formato di documento nativo dell'applicazione Adobe Photoshop. Adobe Photoshop (versione 5.0 e successiva) memorizza le informazioni sulla miniatura per la visualizzazione in anteprima in un blocco di risorse dell'immagine che consiste in un'intestazione iniziale di 28 byte, seguita da una miniatura JFIF in ordine RGB (rosso, verde, blu). L'API di Aspose.PSD fornisce un meccanismo facile da usare per accedere alle risorse del file PSD. Queste risorse includono anche la risorsa miniatura che a sua volta può essere recuperata e salvata su disco secondo le esigenze dell'applicazione. Il seguente frammento di codice mostra come creare miniature da file PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Creazione di file PSD indicizzati**
Aspose.PSD per .NET API può creare file PSD indicizzati da zero. Questo articolo illustra l'uso delle classi PsdOptions e [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) per creare un PSD indicizzato disegnando alcune forme sul canvas appena creato. I seguenti semplici passaggi sono necessari per creare un file PSD indicizzato.

- Creare un'istanza di PsdOptions e impostare la sua origine.
- Impostare la proprietà ColorMode di PsdOptions su ColorModes.Indexed.
- Creare una nuova tavolozza di colori dallo spazio RGB e impostarla come proprietà Palette di PsdOptions.
- Impostare la proprietà CompressionMethod sull'algoritmo di compressione richiesto.
- Creare una nuova immagine PSD chiamando il metodo PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Disegnare grafica o eseguire altre operazioni secondo le esigenze.
- Chiamare il metodo PsdImage.Save per applicare tutte le modifiche.


Il seguente frammento di codice mostra come creare file PSD indicizzati.



{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Esportazione del livello PSD in immagine raster**
Aspose.PSD per .NET consente di esportare i livelli in un file PSD in immagini raster. Utilizzare il metodo [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) per esportare il livello nell'immagine. Il seguente codice di esempio carica un file PSD ed esporta ciascuno dei suoi livelli in un'immagine PNG utilizzando Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Una volta esportati tutti i livelli in immagini PNG, è possibile aprirli utilizzando il proprio visualizzatore di immagini preferito. Il seguente frammento di codice mostra come esportare il livello PSD in un'immagine raster.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Aggiornamento del livello di testo nel file PSD**
Aspose.PSD per .NET consente di manipolare il testo nel livello di testo di un file PSD. Utilizzare la classe [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) per aggiornare il testo nel livello PSD. Il seguente frammento di codice carica un file PSD, accede al livello di testo, aggiorna il testo e salva il file PSD con un nuovo nome utilizzando il metodo [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Rilevamento dei file PSD appiattiti**
Aspose.PSD per .NET consente di rilevare se un determinato file PSD è appiattito o meno. La proprietà IsFlatten è stata introdotta nella classe Aspose.PSD.FileFormats.Psd.PsdImage per ottenere questa funzionalità. Il seguente frammento di codice carica un file PSD e accede alla proprietà [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspose-com-gists" "8e5b4e6a4d52b92e5a91a0e137fb2769" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Unire i livelli PSD**
Questo articolo mostra come unire i livelli in un file PSD convertendo un file PSD in JPG con Aspose.PSD. Nell'esempio seguente, un file PSD esistente viene caricato passando il percorso del file al metodo statico Load della classe Image. Una volta caricato, convertire/castare l'immagine a PsdImage. Creare un'istanza della classe JpegOptions e impostarne varie proprietà. Ora chiamare il metodo Save dell'istanza PsdImage. Il seguente frammento di codice mostra come unire i livelli PSD.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto Scala di grigi con Alfa per PSD**
Questo articolo mostra come supportare Scala di grigi con alfa per il file PSD durante la conversione di un file PSD in PNG con Aspose.PSD. Nell'esempio seguente, un file PSD esistente viene caricato passando il percorso del file al metodo statico Load della classe Image. Una volta caricato, convertire/castare l'immagine a PsdImage. Creare un'istanza della classe PngOptions e impostarne varie proprietà. Imposta la proprietà [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) su TruecolorWithAlpha. Ora chiamare il metodo Save dell'istanza PngOptions. Il seguente frammento di codice mostra come convertire in PNG in Scala di grigi con Alfa.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto Effetti di Livello per PSD**
Questo articolo mostra come supportare diversi effetti come **Sfocatura**, **Bagliore Interno**, **Bagliore Esterno** per il livello PSD. Il seguente frammento di codice mostra come supportare gli effetti di livello.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto Data e Ora di Creazione del Livello**
Questo articolo mostra come supportare la data e l'ora di creazione del livello per il livello PSD. Il seguente frammento di codice mostra come creare i livelli.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto per l'Evidenziazione del Colore del Livello di Sfondo**
Questo articolo mostra come caricare immagini PSD, cambiare ed evidenziare i colori di sfondo e salvarli come immagine. È stato fornito uno snippet di codice.


{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto per il Maschera del Livello**
Questo articolo mostra come supportare il maschera del livello per le immagini PSD e quindi salvare queste immagini. È stato fornito uno snippet di codice di seguito.



{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto per il Maschera Vettoriale del Livello**
Questo articolo mostra come Supporto per maschere vettoriali di livello per Aspose.PSD. Il seguente frammento di codice mostra come Aspose.PSD supporta le maschere vettoriali di livello.



{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto per i Livelli di Testo in Esecuzione**
Questo articolo mostra come aggiungere livelli di testo in esecuzione per le immagini PSD. È stato fornito uno snippet di codice di seguito.



{{< gist "aspose-com-gists" "8a4d34ce8562d175c7c0ce94ffe4a8c9" "Examples-CsnaAedwtORfyeginnapsIRhtOrevenuDHOtWRadagiD" >}}
## **Supporto per i Livelli di Regolazione**
Questo articolo mostra come regolare i livelli e in caso il livello sia nullo unirlo e salvarlo come immagini PSD. È stato fornito uno snippet di codice di seguito.



{{< gist "aspose-psd" "c68d1f8aa6f2af15b98e4d34e14a504a" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.cs" >}}
## **Gestire Luminosità e Contrasto nei Livelli di Regolazione**
Questo articolo mostra come iterare attraverso i livelli e gestire luminosità e contrasto nei livelli e quindi salvare come immagini PSD. È stato
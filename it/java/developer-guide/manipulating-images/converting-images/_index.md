---
title: Conversione Immagini
type: docs
weight: 20
url: /it/java/conversione-immagini/
---

## **Converting Immagini in Bianco e Nero e Scala di Grigi**
A volte potresti aver bisogno di convertire immagini a colori in Bianco e Nero o Scala di Grigi per scopi di stampa o archiviazione. Questo articolo dimostra l'uso di Aspose.PSD per l'API Java per raggiungere questo obiettivo utilizzando due metodi come indicato di seguito.

- Binarizzazione
- Scala di grigi
### **Binarizzazione**
Per comprendere il concetto di Binarizzazione, è importante definire un'Immagine Binaria; ossia un'immagine digitale che può avere solo due possibili valori per ogni pixel. Normalmente, i due colori utilizzati per un'immagine binaria sono nero e bianco, anche se possono essere utilizzati due colori qualsiasi. La Binarizzazione è il processo di conversione di un'immagine in bi-livello, il che significa che ogni pixel è memorizzato come un singolo bit (0 o 1) dove 0 denota l'assenza di colore e 1 significa presenza di colore. Aspose.PSD per l'API Java attualmente supporta due metodi di Binarizzazione.
#### **Binarizzazione con Soglia Fissa**
Il seguente frammento di codice mostra come utilizzare la binarizzazione con soglia fissa che può essere applicata a un'immagine.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarizzazione con Soglia di Otsu**
Il seguente frammento di codice mostra come applicare la binarizzazione con soglia di Otsu a un'immagine.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Scala di Grigi**
La scala di grigi è il processo di conversione di un'immagine a toni continui in un'immagine con sfumature di grigio discontinuo. Il seguente frammento di codice mostra come utilizzare la Scala di Grigi.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Convertire Livelli Immagine GIF in Immagine TIFF**
A volte è necessario estrarre e convertire i livelli di un'Immagine PSD in un altro formato di immagine raster per soddisfare un'esigenza dell'applicazione. L'API Aspose.PSD supporta la funzionalità di estrazione e conversione dei livelli di un'Immagine PSD in un altro formato di immagine raster. Prima creeremo un'istanza di immagine e caricheremo l'immagine PSD dal disco locale, quindi itereremo su ciascun livello nella proprietà Layer. Poi convertiremo il blocco in immagine TIFF. Il seguente frammento di codice mostra come convertire i livelli di un'immagine PSD in immagini TIFF.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Converting CMDYK PSD in CMDYK TIFF**
Utilizzando Aspose.PSD per Java, gli sviluppatori possono convertire il file CMDYK PSD in formato TIFF CMDYK. Questo articolo mostra come esportare / convertire il file CMDYK PSD in formato TIFF CMDYK con Aspose.PSD. Utilizzando Aspose.PSD per Java è possibile caricare immagini PSD e quindi è possibile impostare varie proprietà utilizzando la classe TiffOptions e salvare o esportare l'immagine. Il seguente frammento di codice mostra come raggiungere questa funzionalità.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Esportare Immagini**
Oltre a un ricco set di routine di elaborazione delle immagini, Aspose.PSD fornisce classi specializzate per convertire formati di file PSD in altri formati. Utilizzando questa libreria, la conversione delle immagini PSD è molto semplice e intuitiva. Di seguito sono riportate alcune classi specializzate a tale scopo nello spazio dei nomi ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

È facile esportare immagini PSD con Aspose.PSD per Java API. Tutto ciò di cui hai bisogno è un oggetto della classe appropriata dello spazio dei nomi ImageOptions. Utilizzando queste classi, è possibile esportare facilmente qualsiasi immagine creata, modificata o semplicemente caricata con Aspose.PSD per Java in qualsiasi formato supportato.
## **Combinare Immagini**
Questo esempio utilizza la classe Graphics e mostra come combinare due o più immagini in un'unica immagine completa. Per dimostrare l'operazione, l'esempio crea una nuova PsdImage e disegna immagini sulla superficie del canvas utilizzando il metodo Draw Image esposto dalla classe Graphics. Utilizzando la classe Graphics, due o più immagini possono essere combinate in modo che l'immagine risultante sembri un'immagine completa senza spazio tra le parti dell'immagine e senza pagine. Le dimensioni del canvas devono essere uguali alle dimensioni dell'immagine risultante. Di seguito è riportata la dimostrazione del codice che mostra come utilizzare il metodo Draw Image della classe Graphics per combinare immagini in un'unica immagine.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Espandere e Ritagliare Immagini**
Aspose.PSD API consente di espandere o ritagliare un'immagine durante il processo di conversione dell'immagine. Lo sviluppatore deve creare un rettangolo con coordinate X e Y e specificare la larghezza e l'altezza della scatola rettangolare. Le coordinate X, Y e la larghezza, altezza del rettangolo rappresenteranno l'espansione o il ritaglio dell'immagine caricata. Se è necessario espandere o ritagliare l'immagine durante la conversione dell'immagine, eseguire i seguenti passaggi:

1. Creare un'istanza della classe RasterImage e caricare l'immagine esistente.
1. Creare un'istanza della classe ImageOption.
1. Creare un'istanza della classe Rectangle e inizializzare le coordinate X, Y e la larghezza, l'altezza del rettangolo.
1. Chiamare il metodo Save della classe RasterImage passando il nome del file di output, le opzioni dell'immagine e l'oggetto rettangolo come parametri.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Leggere e Scrivere Dati XMP nelle Immagini**
XMP (Extensible Metadata Platform) è uno standard ISO. XMP standardizza un modello di dati, un formato di serializzazione e proprietà core per la definizione e l'elaborazione di metadati estensibili. Fornisce inoltre linee guida per l'incorporazione delle informazioni XMP in immagini popolari come JPEG, senza comprometterne la leggibilità da parte di applicazioni che non supportano XMP. Utilizzando l'API Aspose.PSD per Java, gli sviluppatori possono leggere o scrivere metadati XMP nelle immagini. Questo articolo dimostra come i metadati XMP possono essere letti dall'immagine e come i metadati XMP possono essere scritti nelle immagini.
### **Creare Metadati XMP, Scrivere e Leggerli dal File**
Con l'aiuto dello spazio dei nomi XMP, lo sviluppatore può creare un oggetto di metadati XMP e scriverlo in un'immagine. Il seguente frammento di codice mostra come utilizzare i pacchetti XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage e DublinCorePackage contenuti nello spazio dei nomi XMP.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Esportare Immagini in un Ambiente Multithread**
Aspose.PSD per Java supporta ora la conversione di immagini in un ambiente multithread. Aspose.PSD per Java garantisce le prestazioni ottimizzate delle operazioni durante l'esecuzione del codice in un ambiente multithread. Tutte le classi di opzioni delle immagini (ad es. BmpOptions, TiffOptions, JpegOptions, ecc.) in Aspose.PSD per Java implementano l'interfaccia IDisposable. Pertanto è necessario che lo sviluppatore disponga correttamente dell'oggetto della classe di opzioni delle immagini nel caso in cui venga impostata la proprietà Source. Il seguente frammento di codice dimostra la suddetta funzionalità.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}

Aspose.PSD ora supporta la proprietà SyncRoot mentre si lavora in un ambiente multithread. Lo sviluppatore può utilizzare questa proprietà per sincronizzare l'accesso allo stream di origine. Il seguente frammento di codice dimostra come la proprietà SyncRoot può essere utilizzata.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}

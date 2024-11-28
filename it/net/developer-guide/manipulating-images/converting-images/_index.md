---
title: Conversione delle immagini
type: docs
weight: 20
url: /it/net/converting-images/
---

## **Conversione delle immagini in bianco e nero e scala di grigi**
A volte potresti aver bisogno di convertire immagini a colori in bianco e nero o in scala di grigi per scopi di stampa o archiviazione. Questo articolo illustra l'uso di Aspose.PSD per l'API .NET per raggiungere questo scopo utilizzando due metodi come indicato di seguito.

- Binariazione
- Scala di grigi

### **Binariazione**
Per capire il concetto di binariazione, è importante definire un'immagine binaria; cioè un'immagine digitale che può avere solo due possibili valori per ogni pixel. Normalmente, i due colori utilizzati per un'immagine binaria sono il nero e il bianco anche se possono essere usati qualsiasi due colori. La binarizzazione è il processo di conversione di un'immagine in bianco e nero, il che significa che ogni pixel è memorizzato come un singolo bit (0 o 1) dove 0 indica l'assenza di colore e 1 significa presenza di colore. Attualmente, Aspose.PSD per .NET API supporta due metodi di binariazione.

#### **Binariazione con soglia fissa**
Il seguente frammento di codice ti mostra come utilizzare la binariazione con soglia fissa per applicarla a un'immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binariazione con soglia di Otsu**
Il seguente frammento di codice ti mostra come applicare la binariazione con soglia di Otsu a un'immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Scala di grigi**
La scala di grigi è il processo di conversione di un'immagine a toni continui in un'immagine con sfumature di grigio discontinuo. Il seguente frammento di codice ti mostra come utilizzare la Scala di grigi.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}


## **Convertire i livelli di immagine GIF in immagine TIFF**
A volte è necessario estrarre e convertire i livelli di un'immagine PSD in un'altra immagine raster per soddisfare le esigenze di un'applicazione. L'API di Aspose.PSD supporta la funzionalità di estrazione e conversione dei livelli di un'immagine PSD in un'altra immagine raster. Innanzitutto, creeremo un'istanza dell'immagine e caricheremo l'immagine PSD dal disco locale, quindi iteraeremo su ogni livello nella proprietà Layer. Quindi convertiremo il blocco in immagine TIFF. Il seguente frammento di codice ti mostra come convertire i livelli di un'immagine PSD in immagini TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}


## **Conversione di PSD CMYK in TIFF CMYK**
Utilizzando Aspose.PSD per .NET, i programmatori possono convertire un file PSD CMYK in formato TIFF CMYK. Questo articolo mostra come esportare / convertire un file PSD CMYK in formato TIFF CMYK con Aspose.PSD. Utilizzando Aspose.PSD per .NET è possibile caricare immagini PSD e quindi è possibile impostare diverse proprietà utilizzando la classe [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) e salvare o esportare l'immagine. Il seguente frammento di codice mostra come ottenere questa funzionalità.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}


## **Esportazione di immagini**
Oltre a un ricco insieme di routine di elaborazione delle immagini, Aspose.PSD fornisce classi specializzate per convertire i formati dei file PSD in altri formati. Utilizzando questa libreria, la conversione delle immagini PSD è molto semplice e intuitiva. Di seguito sono riportate alcune classi specializzate per questo scopo nel [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

È facile esportare le immagini PSD con Aspose.PSD for .NET API. Tutto ciò di cui hai bisogno è un oggetto della classe appropriata da [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. Utilizzando queste classi, è possibile esportare facilmente qualsiasi immagine creata, modificata o semplicemente caricata con Aspose.PSD for .NET in qualsiasi formato supportato.

## **Unione di immagini**
Questo esempio utilizza la classe Graphics e mostra come combinare due o più immagini in un'unica immagine completa. Per dimostrare l'operazione, l'esempio crea una nuova PsdImage e disegna le immagini sulla superficie del canvas utilizzando il metodo DrawImage esposto dalla classe Graphics. Utilizzando la classe Graphics, due o più immagini possono essere combinate in modo che l'immagine risultante sembri un'immagine completa senza spazio tra le parti dell'immagine e senza pagine. La dimensione del canvas deve essere uguale alla dimensione dell'immagine risultante. Di seguito è riportata la dimostrazione del codice che mostra come utilizzare il metodo [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) della classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) per combinare le immagini in un'unica immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}


## **Espandere e ritagliare immagini**
L'API Aspose.PSD ti consente di espandere o ritagliare un'immagine durante il processo di conversione dell'immagine. Il programmatore deve creare un rettangolo con coordinate X e Y e specificare la larghezza e l'altezza del rettangolo. Le coordinate X, Y e larghezza, altezza del rettangolo mostreranno l'espansione o il ritaglio dell'immagine caricata. Se è necessario espandere o ritagliare l'immagine durante la conversione dell'immagine, eseguire i seguenti passaggi:

1. Creare un'istanza della classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) e caricare l'immagine esistente.
1. Creare un'istanza della classe ImageOption.
1. Creare un'istanza della classe [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) e inizializzare le coordinate X,Y e larghezza, altezza del rettangolo.
1. Chiamare il metodo [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) della classe RasterImage passando il nome del file di output, le opzioni dell'immagine e l'oggetto rettangolo come parametri.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}


## **Leggere e scrivere dati XMP nelle immagini**
XMP (Extensible Metadata Platform) è uno standard ISO. XMP standardizza un modello di dati, un formato di serializzazione e proprietà principali per la definizione e l'elaborazione di metadati estensibili. Fornisce anche linee guida per l'incorporazione di informazioni XMP in un'immagine popolare come JPEG, senza comprometterne la leggibilità da parte di applicazioni che non supportano XMP. Utilizzando l'API Aspose.PSD per .NET, i programmatori possono leggere o scrivere metadati XMP nelle immagini. Questo articolo dimostra come i metadati XMP possono essere letti da un'immagine e come i metadati XMP possono essere scritti nelle immagini.
### **Creare metadati XMP, scriverli e leggerli dal file**
Con l'aiuto dello spazio dei nomi Xmp, il programmatore può creare un oggetto di metadati XMP e scriverlo nell'immagine. Il seguente frammento di codice mostra come utilizzare i pacchetti XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage e DublinCorePackage contenuti nello spazio dei nomi [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}


## **Esportare immagini in ambiente multi-threaded**
Aspose.PSD per .NET supporta ora la conversione delle immagini in un ambiente multi-threaded. Aspose.PSD per .NET garantisce le prestazioni ottimizzate delle operazioni durante l'esecuzione del codice in un ambiente multi-threaded. Tutte le classi delle [opzioni per l'immagine](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (ad esempio BmpOptions, TiffOptions, JpegOptions, ecc.) in Aspose.PSD for .NET implementano l'interfaccia IDisposable. Pertanto, è importante che il programmatore disponga correttamente dell'oggetto della classe delle opzioni dell'immagine nel caso in cui la proprietà Source sia impostata. Il seguente frammento di codice dimostra la funzionalità menzionata.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD supporta ora la proprietà SyncRoot durante il lavoro in un ambiente multi-threaded. Il programmatore può utilizzare questa proprietà per sincronizzare l'accesso allo stream di origine. Il seguente frammento di codice mostra come può essere utilizzata la proprietà SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}

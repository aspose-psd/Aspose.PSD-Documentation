---
title: Manipolazione delle immagini JPEG
type: docs
weight: 20
url: /it/java/manipolazione-immagini-jpeg/
---

## **Utilizzo della classe ExifData per leggere e modificare i tag EXIF JPEG**

Quasi tutte le fotocamere digitali (compresi gli smartphone), scanner e altri sistemi che gestiscono le immagini salvano le immagini con le informazioni EXIF (Exchangeable Image File). Le impostazioni della fotocamera e le informazioni sulla scena vengono registrate dalla fotocamera nel file dell'immagine. I dati EXIF includono anche la velocità dell'otturatore, la data e l'ora in cui è stata scattata una foto, la lunghezza focale, la compensazione dell'esposizione, il modello di misurazione e se è stato utilizzato un flash. Le API di Aspose.Imaging hanno reso possibile estrarre le informazioni EXIF da un'immagine data in modo molto semplice e facile. Gli sviluppatori possono anche scrivere i dati EXIF sulle immagini o modificare le informazioni esistenti secondo le proprie esigenze. Aspose.Imaging ha fornito la classe ExifData per leggere, scrivere e modificare i dati EXIF, mentre lo spazio dei nomi Aspose.PSD.Exif.Enums contiene le enumerazioni pertinenti utilizzate nel processo.
### **Lettura dei dati EXIF**
Le API di Aspose.PSD forniscono il modo per leggere i dati EXIF da un'immagine data. I passaggi forniti di seguito illustrano l'utilizzo della classe ExifData per leggere le informazioni EXIF da un'immagine.

- Caricare l'immagine PSD utilizzando il metodo factory Load.
- Trovare l'immagine miniatura JPEG tra le risorse PSD.
- Estrarre un'istanza della classe ExifData.

Recuperare le informazioni necessarie e scriverle sulla console.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



In alternativa, gli sviluppatori possono ottenere informazioni specifiche utilizzando il seguente codice snippet.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Scrittura e modifica dei dati EXIF**
Utilizzando le API di Aspose.PSD, gli sviluppatori possono scrivere nuove informazioni EXIF e modificare i dati EXIF esistenti di un'immagine. Entrambi i processi (Scrittura e Modifica) richiedono il caricamento di un'immagine e l'ottenimento dei dati EXIF in un'istanza della classe ExifData. Quindi è possibile accedere alle proprietà esposte dalla classe ExifData per impostarle di conseguenza. Si tenga presente che le immagini da manipolare devono essere immagini JPEG o TIFF che di solito sono miniature PSD. Il codice di esempio per dimostrare l'utilizzo è il seguente:


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Estrazione delle miniature dalle risorse PSD**
Le miniature sono versioni ridotte delle immagini utilizzate per visualizzare una parte significativa dell'immagine anziché l'intero fotogramma. Alcuni file immagine (specialmente quelli scattati con una fotocamera digitale) hanno un'immagine di anteprima incorporata nel file. L'API Aspose.PSD consente di estrarre le miniature delle risorse PSD e salvarle separatamente su disco. Le risorse delle miniature contengono la proprietà ExifData.Thumbnail che può recuperare i dati della miniatura. Il codice di esempio fornito di seguito dimostra come utilizzarlo.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Utilizzare l'approccio discusso sopra per salvare la miniatura in altri formati di file supportati. Se si desidera esportare i dati della miniatura in altri formati di immagine come BMP e PNG, è possibile utilizzare altre opzioni di esportazione dell'immagine.
### **Estrazione delle miniature dai segmenti JFIF**
È anche possibile estrarre le miniature dal segmento ExifData o JFIF delle risorse delle miniature PSD. Il codice seguente mostra come eseguire l'estrazione dei dati della miniatura dal segmento JFIF o ExifData:


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Utilizzare l'approccio discusso sopra per salvare la miniatura in altri formati di file supportati. Se si desidera esportare i dati della miniatura in altri formati di immagine come BMP e PNG, è possibile utilizzare altre opzioni di esportazione dell'immagine.
### **Aggiungere una miniatura al segmento JFIF**
Il codice snippet di seguito illustra come utilizzare la proprietà JFIF.Thumbnail per aggiungere un'immagine di anteprima al segmento JFIF di un'immagine PSD caricata.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Le immagini di anteprima con altri dati del segmento non possono occupare più di 65.545 byte a causa delle specifiche del formato JPEG. Nei casi in cui si devono impostare immagini di grandi dimensioni come anteprima, potrebbe verificarsi un'eccezione.


### **Aggiungere una miniatura al segmento EXIF**
Il codice snippet di seguito dimostra come utilizzare la proprietà ExifData.Thumbnail per aggiungere un'immagine di anteprima al segmento EXIF di un'immagine PSD caricata.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

In questo caso, le API di Aspose.PSD non possono stimare le dimensioni dell'immagine di anteprima, ma possono verificare le dimensioni dell'intero segmento dei dati EXIF. Questo non può essere superiore a 65.535 byte.
## **Utilizzo della classe JpegExifData per leggere e modificare i tag EXIF JPEG**
Le API di Aspose.PSD forniscono la classe JpegExifData che è esclusiva per i formati di immagini JPEG per recuperare e aggiornare le informazioni EXIF. Questo articolo dimostra l'utilizzo della classe JpegExifData per ottenere lo stesso risultato. La classe Aspose.PSD.Exif.JpegExifData serve come contenitore dati EXIF per le immagini JPEG e fornisce il modo per recuperare i tag EXIF JPEG standard come mostrato di seguito:


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Lista completa dei tag EXIF**
Il codice di cui sopra legge alcuni tag EXIF utilizzando le proprietà offerte dalla classe Aspose.PSD.Exif.JpegExifData. L'elenco completo di queste proprietà è disponibile qui. Il codice seguente leggerà tutti i tag EXIF utilizzando la classe System.Reflection.PropertyInfo.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Correzione automatica dell'orientamento delle immagini JPEG**
Le foto possono essere scattate con una fotocamera ruotata di 90°, 180°, 270° o nessuna (orientamento normale). La maggior parte delle fotocamere digitali memorizza le informazioni sull'orientamento insieme ai dati dell'immagine come tag EXIF delle immagini JPEG. Queste informazioni possono essere utilizzate per eseguire la rotazione automatica delle immagini per correggere l'orientamento. Le API di Aspose.PSD forniscono il metodo AutoRotate per la classe JpegImage per correggere automaticamente l'orientamento delle immagini JPEG. Di seguito è riportato come utilizzare il metodo AutoRotate con l'API Aspose.PSD per Java.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Supporto per JPEG-LS con CMYK e YCCK**
Aspose.PSD fornisce supporto per i modelli di colore CMYK e YCCK con JPEG-LS. Il codice snippet di seguito mostra come utilizzare quel supporto per JPEG-LS.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Supporto per immagini JPEG-LS con 2-7 bit per campione**
Aspose.PSD fornisce supporto per immagini JPEG-LS con 2-7 bit per campione. Il codice snippet di seguito mostra come utilizzare quel supporto per JPEG-LS.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Impostare il tipo di colore e il tipo di compressione per le immagini JPEG**
Aspose.PSD fornisce supporto per il tipo di colore e il tipo di compressione e li imposta in scala di grigi e progressiva per le immagini JPEG. Il codice snippet di seguito mostra come utilizzare quel supporto.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}





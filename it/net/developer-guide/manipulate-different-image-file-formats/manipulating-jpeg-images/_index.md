---
title: Manipolazione immagini JPEG
type: docs
weight: 30
url: /it/manipolazione-immagini-jpeg/
---

## **Utilizzo della classe ExifData per leggere e modificare i tag Exif delle immagini JPEG**
Quasi tutte le fotocamere digitali (compresi gli smartphone), scanner e altri sistemi che gestiscono immagini salvano le immagini con informazioni EXIF (Exchangeable Image File). Le impostazioni della fotocamera e le informazioni sulla scena vengono registrate dalla fotocamera nel file dell'immagine. I dati EXIF includono anche la velocità dell'otturatore, la data e l'ora in cui è stata scattata una foto, la lunghezza focale, la compensazione dell'esposizione, il modello di misurazione e se è stato utilizzato un flash. Le API di Aspose.Imaging hanno reso possibile estrarre le informazioni EXIF da un'immagine data in modo molto facile e semplice. Gli sviluppatori possono anche scrivere dati EXIF sulle immagini o modificare le informazioni esistenti secondo le proprie esigenze. Aspose.PSD ha fornito la classe [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) per la lettura, scrittura e modifica dei dati EXIF, mentre il namespace [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) contiene le enumerazioni rilevanti utilizzate nel processo.
### **Lettura dei dati EXIF**
Le API di Aspose.PSD forniscono il modo per leggere i dati EXIF da un'immagine data. I passaggi forniti di seguito illustrano l'utilizzo della classe ExifData per leggere le informazioni EXIF da un'immagine.

- Caricare un'immagine PSD utilizzando il metodo di fabbrica Load.
- Trovare l'anteprima JPEG tra le risorse PSD.
- Estrarre un'istanza della classe ExifData.

Recuperare le informazioni richieste e scriverle sulla console.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-LeggiTuttiITagEXIF-LeggiTuttiITagEXIF.cs" >}}


In alternativa, gli sviluppatori possono ottenere le informazioni specifiche utilizzando il seguente snippet di codice.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-LeggiInformazioniSpecificheTagEXIF-LeggiInformazioniSpecificheTagEXIF.cs" >}}
### **Scrittura e modifica dei dati EXIF**
Utilizzando le API di Aspose.PSD, gli sviluppatori possono scrivere nuove informazioni EXIF e modificare i dati EXIF esistenti di un'immagine. Entrambi i processi (Scrittura e Modifica) richiedono il caricamento di un'immagine e l'ottenimento dei dati EXIF in un'istanza della classe ExifData. Quindi è possibile accedere alle proprietà esposte dalla classe ExifData per impostarle di conseguenza. Si noti che le immagini da manipolare dovrebbero essere immagini Jpeg o Tiff che di solito sono miniature PSD. Il codice di esempio per dimostrare l'utilizzo è il seguente:




{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-ScritturaEModificaDatiEXIF-ScritturaEModificaDatiEXIF.cs" >}}
## **Estrazione delle miniature dalle risorse PSD**
Le miniature sono versioni ridotte delle immagini, utilizzate per mostrare una parte significativa dell'immagine anziché l'intero frame. Alcuni file immagine (specialmente quelli scattati con una fotocamera digitale) hanno un'immagine in miniatura incorporata nel file. L'API di Aspose.PSD consente di estrarre le miniature delle risorse PSD e salvarle separatamente su disco. Le risorse delle miniature contengono la proprietà [Miniatura](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) di ExifData che può recuperare i dati della miniatura. Lo snippet di codice fornito di seguito dimostra come utilizzarlo.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-EstraiMiniaturaDaPSD-EstraiMiniaturaDaPSD.cs" >}}


Utilizza l'approccio discusso sopra per salvare la miniatura in altri formati di file supportati. Se desideri esportare i dati della miniatura in altri formati di immagini come BMP e PNG, utilizza altre opzioni di esportazione delle immagini.
### **Estrazione delle miniature dai segmenti JFIF**
È anche possibile estrarre le miniature dai segmenti ExifData o JFIF delle risorse di miniatura PSD. Il seguente codice mostra come eseguire l'estrazione dei dati della miniatura dal segmento JFIF o ExifData:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-EstraiMiniaturaDaPSD-EstraiMiniaturaDaPSD.cs" >}}


Utilizza l'approccio discusso sopra per salvare la miniatura in altri formati di file supportati. Se desideri esportare i dati della miniatura in altri formati di immagini come BMP e PNG, utilizza altre opzioni di esportazione delle immagini.
### **Aggiungi Miniatura al segmento JFIF**
Lo snippet di codice sottostante illustra come utilizzare la proprietà JFIF. Miniatura per aggiungere un'immagine miniatura al segmento JFIF di un'immagine PSD caricata.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-AggiungiMiniaturaAlSegmentoJFIF-AggiungiMiniaturaAlSegmentoJFIF.cs" >}}


Le immagini miniatura con altri dati di segmento non possono occupare più di 65.545 byte a causa delle specifiche del formato JPEG. Nei casi in cui debbano essere impostate immagini di grandi dimensioni come miniatura, potrebbero verificarsi eccezioni.


### **Aggiungi Miniatura al segmento EXIF**
Lo snippet di codice sottostante mostra come utilizzare la proprietà ExifData.Thumbnail per aggiungere un'immagine miniatura al segmento EXIF di un'immagine PSD caricata.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-AggiungiMiniaturaAlSegmentoEXIF-AggiungiMiniaturaAlSegmentoEXIF.cs" >}}


In questo caso, l'API di Aspose.PSD non può stimare le dimensioni dell'immagine miniatura, ma può controllare le dimensioni dell'intero segmento dei dati EXIF. Questo non può essere più grande di 65.535 byte.

## **Utilizzo della classe JpegExifData per leggere e modificare i tag Exif delle immagini Jpeg**
Le API di Aspose.PSD forniscono la classe [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) che è esclusiva per i formati di immagini Jpeg per recuperare e aggiornare le informazioni EXIF. Questo articolo illustra l'utilizzo della classe JpegExifData per raggiungere lo stesso obiettivo. La classe Aspose.PSD.Exif.JpegExifData funge da contenitore dati EXIF per immagini Jpeg e fornisce il modo per recuperare i tag standard EXIF delle immagini Jpeg come dimostrato di seguito:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-AggiungiMiniaturaAlSegmentoEXIF-AggiungiMiniaturaAlSegmentoEXIF.cs" >}}
### **Elenco completo dei tag EXIF**
Lo snippet di codice sopra legge alcuni tag EXIF utilizzando le proprietà offerte dalla classe Aspose.PSD.Exif.JpegExifData. L'elenco completo di queste proprietà è disponibile qui. Il codice seguente leggerà tutti i tag EXIF utilizzando la classe [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-LeggiTuttiIElencoTagEXIF-LeggiTuttiIElencoTagEXIF.cs" >}}
## **Correzione automatica dell'orientamento delle immagini JPEG**


Le foto possono essere scattate con una fotocamera ruotata di 90°, 180°, 270° o nessuna (orientamento normale). La maggior parte delle fotocamere digitali memorizza le informazioni sull'orientamento insieme ai dati dell'immagine come tag EXIF delle immagini JPEG. Queste informazioni possono essere utilizzate per eseguire l'auto-rotazione delle immagini per correggere l'orientamento. Le API di Aspose.PSD forniscono il metodo AutoRotate per la classe JpegImage per correggere automaticamente l'orientamento delle immagini JPEG. Ecco come puoi utilizzare il metodo AutoRotate con Aspose.PSD per .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModificaEConvertiImmagini-JPEG-CorrezioneAutomaticaDellOrientamentoDelleImmaginiJPEG-CorrezioneAutomaticaDellOrientamentoDelleImmaginiJPEG.cs" >}}
## **Supporto per JPEG-LS con CMYK e YCCK**


Aspose.PSD per .NET API fornisce supporto per i modelli di colore CMYK e YCCK con JPEG-LS. Lo snippet di codice di seguito dimostra come utilizzare quel supporto per JPEG-LS.


{{< gist "aspose-com-gists" "8a4dce132fc534c17542d168e9d34a8" "Esempi-CSharp-Adobe-AnalisiEVisualizzazioneImmagini-JPEG-SupportoPerJPEG_LSConCMYK-SupportoPerJPEG_LSConCMYK.cs" >}}
## **Supporto per immagini JPEG-LS con 2-7 bit per campione**


Aspose.PSD per .NET API fornisce supporto per immagini JPEG-LS con 2-7 bit per campione. Lo snippet di codice seguente dimostra come utilizzare quel supporto per JPEG-LS.


{{< gist "aspose-com-gists" "8127a894fc3e5a426034192486de2d5" "Esempi-CSharp-Adobe-AnalisiEVisualizzazioneImmagini-JPEG-SupportoPer2-7BitsJPEG-SupportoPer2_7BitsJPEG.cs" >}}
## **Impostazione del tipo di colore e del tipo di compressione per le immagini JPEG**



Aspose.PSD per .NET API fornisce supporto per il tipo di colore e il tipo di compressione e li imposta come scala di grigi e progressivo per le immagini JPEG. Lo snippet di codice seguente dimostra come utilizzare quel supporto.


{{< gist "aspose-com-gists" "8c479341582d095c105e641843d225d" "Esempi-CSharp-Adobe-AnalisiEVisualizzazioneImmagini-JPEG-TipoColoreETipoCompressione-TipoColoreETipoCompressione.cs" >}}

Il seguente snippet di codice mostra come utilizzare la proprietà ExifData.Thumbnail per aggiungere un'immagine miniatura al segmento EXIF di un'immagine PSD caricata.


{{< gist "aspose-com-gists" "8b7d914b767f2748337b154908e6936" "Esempi-CSharp-Adobe-AnalisiEVisualizzazioneImmagini-JPEG-AggiungiMiniaturaAlSegmentoEXIF-AggiungiMiniaturaAlSegmentoEXIF.cs" >}}

In questo caso, l'API di Aspose.PSD non può stimare le dimensioni dell'immagine miniatura, ma può controllare le dimensioni dell'intero segmento dei dati EXIF. Questo non può essere più grande di 65.535 byte.

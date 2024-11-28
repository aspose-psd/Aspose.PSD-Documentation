---
title: Creazione, Apertura e Salvataggio Immagini
type: docs
weight: 30
url: /it/net/creazione-apertura-e-salvataggio-immagini/
---

## **Creazione File Immagine**
Aspose.PSD per .NET consente agli sviluppatori di creare le proprie immagini. Utilizzare il metodo statico Create esposto dalla classe Image per creare nuove immagini. Tutto ciò che devi fare è fornire l'oggetto appropriato di una delle classi dello spazio dei nomi ImageOptions per il formato di immagine di output desiderato. Per creare un file immagine, prima creare un'istanza di una delle classi dello spazio dei nomi ImageOptions. Queste classi determinano il formato dell'immagine di output. Di seguito alcune classi dello spazio dei nomi ImageOptions (nota che attualmente sono supportati solo i formati di file PSD della famiglia):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) imposta le opzioni per la creazione di un file PSD. I file immagine possono essere creati impostando un percorso di output o impostando uno stream.
### **Creazione Impostando il Percorso**
Creare PsdOptions dallo [spazio dei nomi ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) e impostare le varie proprietà. La proprietà più importante da impostare è la proprietà Source. Questa proprietà specifica dove risiedono i dati dell'immagine (in un file o uno stream). Nell'esempio seguente, la sorgente è un file. Dopo aver impostato le proprietà, passare l'oggetto a uno dei metodi statici [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) insieme ai parametri di larghezza e altezza. Larghezza e altezza sono definite in pixel.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Creazione Utilizzando uno Stream**
Il processo per creare un'immagine utilizzando uno stream è lo stesso dell'utilizzo di un percorso. L'unica differenza è che è necessario creare un'istanza di [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) passando un oggetto Stream al suo costruttore e assegnandolo alla proprietà Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Apertura File Immagine**
Gli sviluppatori possono utilizzare l'API Aspose.PSD per .NET per aprire file immagine PSD esistenti per scopi diversi, come l'aggiunta di effetti all'immagine o la conversione di un file esistente in un altro formato. Qualunque sia lo scopo, Aspose.PSD fornisce due modi standard per aprire file esistenti: da file o da uno stream.
### **Apertura da Disco**
Aprire un file immagine passando il percorso e il nome del file come parametro al metodo statico Load esposto dalla classe Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Apertura Utilizzando uno Stream**
A volte l'immagine che dobbiamo aprire è memorizzata come uno stream. In tali casi, utilizzare la versione sovraccaricata del metodo Load. Questo accetta un oggetto Stream come argomento per aprire l'immagine.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Carica Immagine come Livello**
Questo articolo dimostra l'utilizzo di Aspose.PSD per caricare un'immagine come livello. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto il metodo AddLayer della classe PsdImage per aggiungere un'immagine in un file PSD come livello.

I passaggi per caricare un'immagine in un PSD come livello sono semplici come segue:

- Creare un'istanza di un'immagine utilizzando la classe PsdImage con una larghezza e altezza specificate.
- Caricare un file PSD come immagine utilizzando il metodo factory Load esposto dalla classe Image.
- Creare un'istanza della classe Layer e assegnare il livello dell'immagine PSD ad essa.
- Aggiungere il livello creato utilizzando il metodo AddLayer esposto dalla classe PsdImage
- Salvare i risultati.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Carica Immagine come Livello da uno Stream**
Questo articolo dimostra l'utilizzo di Aspose.PSD per caricare un'immagine come livello da uno stream. Per caricare un'immagine da uno stream, basta passare un oggetto stream che contiene un'immagine al costruttore della classe Layer. Aggiungere il livello creato utilizzando il metodo AddLayer esposto dalla classe PsdImage e salvare i risultati.


Ecco il codice di esempio.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Salvataggio File Immagine**
Aspose.PSD consente di creare file immagine da zero. Fornisce anche i mezzi per modificare file immagine esistenti. Una volta creata o modificata l'immagine, il file di solito viene salvato su disco. Aspose.PSD fornisce metodi per salvare immagini su disco specificando un percorso o utilizzando un oggetto Stream.
### **Salvataggio su Disco**
La classe Image rappresenta un oggetto immagine, quindi questa classe fornisce tutti gli strumenti necessari per creare, caricare e salvare un file immagine. Utilizzare il metodo Save della classe Image per salvare le immagini. Una versione sovraccaricata del metodo Save accetta la posizione del file come stringa.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Salvataggio su uno Stream**
Un'altra versione sovraccaricata del metodo Save accetta un oggetto Stream come argomento e salva il file immagine nello stream.

Se l'immagine è creata specificando uno qualsiasi dei CreateOptions nel costruttore Image, l'immagine viene salvata automaticamente nel percorso o streaming fornito durante l'inizializzazione della classe Image chiamando il metodo Save che non accetta alcun parametro.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Impostazione per la Sostituzione dei Caratteri Mancanti**
Gli sviluppatori possono utilizzare l'API di Aspose.PSD per .NET per caricare file immagine PSD esistenti per scopi diversi, ad esempio per impostare il nome del carattere predefinito durante il salvataggio dei documenti PSD come immagine raster (in formati PNG, JPG e BMP). Questo carattere predefinito dovrebbe essere utilizzato come sostituzione per tutti i caratteri mancanti (caratteri che non si trovano nel Sistema Operativo corrente). Una volta modificata l'immagine, il file viene salvato su disco.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}

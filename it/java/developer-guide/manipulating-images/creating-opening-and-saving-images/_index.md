---
title: Creazione, Apertura e Salvataggio delle Immagini
type: docs
weight: 30
url: /it/java/creazione-apertura-e-salvataggio-immagini/
---

## **Creazione dei File Immagine**
Aspose.PSD per Java consente agli sviluppatori di creare le proprie immagini. Utilizza il metodo statico Create esposto dalla classe Image per creare nuove immagini. Tutto ciò che devi fare è fornire l'oggetto appropriato di una delle classi dello spazio dei nomi ImageOptions per il formato di immagine in uscita desiderato. Per creare un file immagine, prima crea un'istanza di una delle classi dello spazio dei nomi ImageOptions. Queste classi determinano il formato dell'immagine in uscita. Di seguito alcune classi dello spazio dei nomi ImageOptions (nota che attualmente sono supportati solo i formati di file PSD):

PsdOptions imposta le opzioni per la creazione di un file PSD. I file immagine possono essere creati impostando un percorso di output o impostando un flusso.
### **Creazione Impostando il Percorso**
Crea PsdOptions dallo spazio dei nomi ImageOptions e imposta le varie proprietà. La proprietà più importante da impostare è la proprietà Source. Questa proprietà specifica dove risiedono i dati dell'immagine (in un file o in un flusso). Nell'esempio sottostante, il sorgente è un file. Dopo aver impostato le proprietà, passa l'oggetto a uno dei metodi statici Create insieme ai parametri larghezza e altezza. La larghezza e l'altezza sono definite in pixel.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Creazione utilizzando un Flusso**
Il processo per la creazione di un'immagine utilizzando un flusso è simile a quello per l'utilizzo di un percorso. L'unica differenza è che devi creare un'istanza di StreamSource passando un oggetto Stream al suo costruttore e assegnandolo alla proprietà Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Apertura dei File Immagine**
Gli sviluppatori possono utilizzare l'API di Aspose.PSD per Java per aprire i file immagine PSD esistenti per scopi diversi, come aggiungere effetti all'immagine o convertire un file esistente in un altro formato. Qualunque sia lo scopo, Aspose.PSD fornisce due modi standard per aprire i file esistenti: da file o da un flusso.
### **Apertura da Disco**
Apri un file immagine passando il percorso e il nome del file come parametro al metodo statico Load esposto dalla classe Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Apertura utilizzando un Flusso**
A volte l'immagine che deve essere aperta è memorizzata come flusso. In tali casi, utilizza la versione sovraccarica del metodo Load. Questo accetta un oggetto Stream come argomento per aprire l'immagine.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Carica Immagine come Livello**
Questo articolo mostra l'utilizzo di Aspose.PSD per caricare un'immagine come livello. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD ha esposto il metodo AddLayer della classe PsdImage per aggiungere un'immagine in un file PSD come livello.

I passaggi per caricare un'immagine in PSD come livello sono semplici come di seguito:

- Crea un'istanza dell'immagine utilizzando la classe PsdImage con larghezza e altezza specificate.
- Carica un file PSD come immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
- Crea un'istanza della classe Layer e assegna il livello dell'immagine PSD ad essa.
- Aggiunge il livello creato utilizzando il metodo AddLayer esposto dalla classe PsdImage
- Salva i risultati.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Salvataggio dei File Immagine**
Aspose.PSD ti consente di creare file immagine da zero. Fornisce anche i mezzi per modificare i file immagine esistenti. Una volta che l'immagine è stata creata o modificata, il file viene solitamente salvato su disco. Aspose.PSD ti fornisce metodi per salvare le immagini su disco specificando un percorso o utilizzando un oggetto Stream.
### **Salvataggio su Disco**
La classe Image rappresenta un oggetto immagine, quindi questa classe fornisce tutti gli strumenti necessari per creare, caricare e salvare un file immagine. Utilizza il metodo Save della classe Image per salvare le immagini. Una versione sovraccarica del metodo Save accetta il percorso del file come stringa.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Salvataggio su un Flusso**
Un'altra versione sovraccarica del metodo Save accetta l'oggetto Stream come argomento e salva il file immagine sul flusso.

Se l'immagine è creata specificando uno qualsiasi dei CreateOptions nel costruttore Image, l'immagine viene automaticamente salvata nel percorso o nel flusso fornito durante l'inizializzazione della classe Image chiamando il metodo Save che non accetta alcun parametro.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Impostazione per Sostituire i Font Mancanti**
Gli sviluppatori possono utilizzare l'API di Aspose.PSD per Java per caricare file immagine PSD esistenti per scopi diversi, ad esempio per impostare il nome del font predefinito durante il salvataggio di documenti PSD come immagine raster (in formati PNG, JPG e BMP). Questo font predefinito dovrebbe essere utilizzato come sostituto per tutti i font mancanti (font non trovati nel sistema operativo corrente). Una volta che l'immagine è stata modificata, il file verrà salvato su disco.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}


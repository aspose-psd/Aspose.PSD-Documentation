---
title: Conversione dello spazio colore per JPEG attraverso profili ICC
type: docs
weight: 50
url: /it/java/conversione-spazio-colore-per-jpeg-tramite-profili-icc/
---

## **Gestione del colore per il formato JPEG**

Questo articolo discute l'utilizzo dei profili ICC per eseguire la gestione dello spazio colore durante la gestione del formato JPEG con le API Aspose.PSD. Lo spazio colore interno del JPEG è YCbCr, tuttavia questo formato può anche ospitare spazi colore Grayscale, RGB, CMYK e YCCK per memorizzare i metadati dell'immagine. Le API Aspose.PSD operano principalmente nello spazio RGB, quindi l'API deve eseguire la conversione dello spazio colore da e verso per gestire correttamente i file JPEG. Le conversioni da scala di grigi a RGB e da YCbCr a RGB possono essere effettuate con trasformazioni matematiche, ma gli spazi colore CMYK e YCCK non possono essere facilmente convertiti nello spazio RGB.

Le API Aspose.PSD devono eseguire una trasformazione del colore diretta da RGB a CMYK per le immagini JPEG che hanno lo spazio colore CMYK. D'altra parte, le immagini che hanno lo spazio colore YCCK richiedono una trasformazione del colore da RGB a CMYK a YCCK, dove la trasformazione da CMYK a YCCK utilizza la conversione ITU-R BT.601 applicata ai primi tre canali, lasciando il canale k invariato. In breve, le API Aspose.PSD devono eseguire l'interconversione degli spazi colore RGB e CMYK per entrambe le immagini CMYK e YCCK, e tali trasformazioni vengono eseguite con l'aiuto dei profili ICC che sono essenzialmente tabelle di ricerca che descrivono le proprietà di un colore e aiutano nelle trasformazioni del colore.

## **Profili ICC**

Il meccanismo di conversione ICC utilizza "Profili" che mappano lo spazio colore di origine agli spazi colore CIELAB o CIEXYZ indipendenti dal dispositivo. Aspose.PSD può convertire i dati nello spazio colore come richiesto utilizzando questi due spazi colore con profili aggiuntivi. Pertanto, per la conversione ICC l'utente deve fornire due profili: un profilo RGB per arrivare allo spazio colore CIE interno e un profilo CMYK per ottenere le caratteristiche del colore CMYK. Per ottenere la conversione da CMYK a RGB, è necessario scambiare i profili, cioè; utilizzare il profilo CMYK come profilo di origine e il profilo RGB come profilo di destinazione.
 
## **Conversione del colore per JPEG attraverso profili ICC**

Le API Aspose.PSD nascondono i dettagli, fornendo un meccanismo facile da usare per specificare i profili ICC tramite la classe JpegOptions. Inoltre, Aspose.PSD utilizza i profili campione di SWOP CMYK e sRGB incorporati nel suo core, quindi nella maggior parte dei casi d'uso comuni, l'utente non ha bisogno di cercare profili specifici. C'è un inconveniente di tali correzioni, cioè; tali conversioni dello spazio colore sono irreversibili perché non possiamo aspettarci di ottenere lo stesso colore dopo la conversione da RGB a CMYK a RGB a causa degli spazi colore incompatibili e dei diversi profili colore. Il seguente snippet di codice dimostra l'utilizzo di Aspose.PSD per le API Java per specificare i profili colore RGB e CMYK per l'immagine JPEG YCCK. Nell'esempio sottostante i profili colore RGB e CMYK vengono modificati e l'immagine viene salvata nello spazio colore YCCK. Si noti che le proprietà RgbColorProfile e CmykColorProfile funzioneranno per modificare i dati dei pixel per lo spazio colore YCCK. Tutti gli altri spazi colore non recuperano i profili colore per l'aggiornamento dei dati di colore.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.java" >}}

Se non vengono impostati profili, allora le API di Aspose.PSD per Java utilizzeranno i profili predefiniti. L'esempio sottostante utilizza le proprietà dei profili di destinazione che cambiano lo spazio colore di destinazione per la maggior parte delle JpegImages.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.java" >}}

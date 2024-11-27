---
title: Conversione dello Spazio Colore per JPEG tramite Profili ICC
type: docs
weight: 60
url: /it/net/conversione-dello-spazio-colore-per-jpeg-tramite-profili-icc/
---

## **Gestione del Colore per Formato JPEG**

Questo articolo discute l'uso dei profili ICC per eseguire la gestione dello spazio colore durante la gestione del formato JPEG con le API Aspose.PSD. Lo spazio colore interno del JPEG è YCbCr tuttavia questo [formato](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) può anche ospitare spazi colore Grayscale, RGB, CMYK e YCCK per memorizzare i metadati dell'immagine. Le API Aspose.PSD operano principalmente nello spazio RGB quindi l'API deve eseguire la conversione dello spazio colore da e verso per gestire correttamente i file JPEG. Le conversioni da Grayscale a RGB e da YCbCr a RGB possono essere realizzate mediante trasformazioni matematiche ma gli spazi CMYK e YCCK non possono essere facilmente convertiti in spazio RGB.

Le API Aspose.PSD devono eseguire una trasformazione diretta da RGB a CMYK per le immagini JPEG con spazio colore CMYK. D'altra parte, le immagini con spazio colore YCCK richiedono una trasformazione del colore da RGB a CMYK a YCCK, dove la trasformazione da CMYK a YCCK utilizza la conversione [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) applicata ai primi tre canali, lasciando intatto il canale k. In breve, le API Aspose.PSD devono eseguire l'interconversione degli spazi colore RGB e CMYK per entrambe le immagini CMYK e YCCK, e tali trasformazioni vengono eseguite con l'aiuto dei profili ICC che sono essenzialmente tabelle di ricerca che descrivono le proprietà di un colore e aiutano nelle trasformazioni del colore.

## **Profili ICC**

Il meccanismo di conversione ICC utilizza "Profili" che mappano lo spazio colore di origine verso spazi colore CIELAB o CIEXYZ indipendenti dal dispositivo. Aspose.PSD può convertire i dati nello spazio colore desiderato utilizzando questi due spazi colore con profili aggiuntivi. Pertanto, per la conversione ICC, l'utente deve fornire due profili: un profilo RGB per arrivare allo spazio colore CIE interno e un profilo CMYK per ottenere le caratteristiche del colore CMYK. Per ottenere la conversione da CMYK a RGB, è necessario scambiare i profili, cioè; utilizzare il profilo CMYK come profilo di origine e il profilo RGB come profilo di destinazione.

## **Conversione del Colore per JPEG tramite Profili ICC**

Le API Aspose.PSD nascondono i dettagli, fornendo un meccanismo facile da usare per specificare i profili ICC tramite la classe [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions). Inoltre, Aspose.PSD utilizza i profili di esempio di SWOP, CMYK e sRGB integrati nel suo nucleo perciò nella maggior parte dei casi d'uso comuni, l'utente non ha bisogno di cercare profili specifici. C'è un inconveniente di tali correzioni, ovvero; tali conversioni dello spazio colore sono irreversibili poiché non possiamo aspettarci di ottenere lo stesso colore dopo la conversione da RGB a CMYK a RGB a causa di spazi colore incompatibili e profili di colore diversi. Il seguente snippet di codice dimostra l'uso di Aspose.PSD per .NET API per specificare profili di colore RGB e CMYK per immagini JPEG YCCK. Nell'esempio sottostante i profili di colore RGB e CMYK vengono modificati e l'immagine viene salvata nello spazio colore YCCK. Si noti che le proprietà [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) e [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) funzioneranno per cambiare i dati dei pixel per lo spazio colore YCCK. Tutti gli altri spazi colore non recuperano i profili di colore per l'aggiornamento dei dati di colore.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

Se nessun profilo è impostato, allora Aspose.PSD per l'API .NET utilizzerà i profili predefiniti. Nell'esempio sottostante vengono utilizzate le proprietà dei profili di destinazione che modificano lo spazio colore di destinazione per la maggior parte delle immagini JPEG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}

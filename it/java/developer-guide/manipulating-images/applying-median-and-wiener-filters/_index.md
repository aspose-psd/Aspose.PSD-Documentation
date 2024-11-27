---
title: Applicazione dei filtri Mediana e Wiener
type: docs
weight: 10
url: /it/java/applicazione-dei-filtri-mediana-e-wiener/
---

## **Applicazione dei filtri Mediana e Wiener**
Il filtro mediano è una tecnica di filtraggio digitale non lineare, spesso utilizzata per rimuovere il rumore. Tale riduzione del rumore è un tipico passaggio di pre-elaborazione per migliorare i risultati dell'elaborazione successiva. Il filtro Wiener è il filtro lineare stazionario ottimale per l'errore quadratico medio (MSE) per le immagini degradate da rumore additivo e sfocatura. Utilizzando Aspose.PSD per gli sviluppatori API Java è possibile applicare il filtro mediano per eliminare il rumore dall'immagine e applicare il filtro Gauss Wiener sulle immagini. Questo articolo mostra come i filtri mediano e Gauss Wiener possono essere applicati alle immagini.
### **Applicazione del Filtro Mediano**
Aspose.PSD fornisce la classe MedianFilterOptions per applicare un filtro su un'immagine Raster. Lo snippet di codice di seguito mostra come applicare il filtro mediano a un'immagine raster.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Applicazione del Filtro Gauss Wiener**
Aspose.PSD fornisce la classe GaussWienerFilterOptions per applicare un filtro su un'immagine Raster. Lo snippet di codice di seguito mostra come applicare il filtro Gauss Wiener a un'immagine raster.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Applicazione del Filtro Gauss Wiener per immagini a colori**
Aspose.PSD fornisce anche GaussWienerFilterOptions per immagini a colori. Lo snippet di codice di seguito mostra come applicare il filtro Gauss Wiener a un'immagine a colori.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Applicazione del Filtro Wiener del Movimento**
Aspose.PSD fornisce la classe MotionWienerFilterOptions per applicare un filtro su un'immagine Raster. Lo snippet di codice di seguito mostra come applicare il filtro Wiener del movimento a un'immagine raster.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Applicare il Filtro di Correzione su un'Immagine**
Questo articolo mostra l'uso di Aspose.PSD per Java per eseguire filtri di correzione su un'immagine. Le API di Aspose.PSD hanno metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD for Java ha esposto le classi BilateralSmoothingFilterOptions e SharpenFilterOptions per la filtrazione. La classe BilateralSmoothingFilterOptions necessita di un intero come dimensione. I passaggi per eseguire il Ridimensionamento sono semplici come segue:


1. Caricare un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
1. Convertire l'immagine in RasterImage.
1. Creare istanze delle classi BilateralSmoothingFilterOptions e SharpenFilterOptions.
1. Chiamare il metodo RasterImage.Filter specificando il rettangolo come limiti dell'immagine e l'istanza della classe BilateralSmoothingFilterOptions.
1. Chiamare il metodo RasterImage.Filter specificando il rettangolo come limiti dell'immagine e l'istanza della classe SharpenFilterOptions.
1. Regolare il contrasto
1. Impostare la luminosità.
1. Salvare i risultati.

Il seguente snippet di codice mostra come applicare il filtro di correzione.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Utilizzare l'algoritmo di soglia di Bradley**
Il thresholding dell'immagine è utilizzato nelle applicazioni grafiche. L'obiettivo del thresholding di un'immagine è classificare i pixel come "scuri" o "chiari". L'API di Aspose.PSD consente di utilizzare il thresholding di Bradley durante la conversione delle immagini. Il seguente snippet di codice mostra come definire il valore di soglia e quindi invocare l'algoritmo di soglia di Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}

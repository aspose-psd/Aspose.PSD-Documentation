---
title: Applicazione dei filtri mediano e Wiener
type: docs
weight: 10
url: /it/applicazione-dei-filtri-mediano-e-wiener/
---

## **Applicazione dei filtri mediano e Wiener**
Il filtro mediano è una tecnica di filtraggio digitale non lineare, spesso utilizzata per rimuovere il rumore. Tale riduzione del rumore è un tipico passaggio di pre-elaborazione per migliorare i risultati dell'elaborazione successiva. Il filtro di Wiener è il filtro lineare stazionario ottimale MSE (errore quadratico medio) per le immagini degradate da rumore additivo e sfocatura. Utilizzando Aspose.PSD per gli sviluppatori API .NET è possibile applicare un filtro mediano per eliminare il rumore dall'immagine e applicare un filtro wiener gaussiano sulle immagini. Questo articolo illustra come il filtro mediano e il filtro wiener gaussiano possono essere applicati alle immagini.
### **Applicazione del filtro mediano**
Aspose.PSD fornisce la classe [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) per applicare un filtro su un [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). La porzione di codice fornita di seguito illustra come applicare il filtro mediano a un'immagine raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Applicazione del filtro Wiener gaussiano**
Aspose.PSD fornisce la classe [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) per applicare un filtro su un [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). La porzione di codice fornita di seguito illustra come applicare il filtro wiener gaussiano a un'immagine raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Applicazione del filtro Wiener gaussiano per immagini a colori**
Aspose.PSD fornisce [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) anche per immagini a colori. La porzione di codice fornita di seguito illustra come applicare il filtro wiener gaussiano a un'immagine a colori.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Applicazione del filtro Wiener di movimento**
Aspose.PSD fornisce la classe [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) per applicare un filtro su un [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). La porzione di codice fornita di seguito illustra come applicare un filtro di Wiener di movimento a un'immagine raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Applica un filtro di correzione su un'immagine**
Questo articolo illustra l'uso di Aspose.PSD per .NET per eseguire filtri di correzione su un'immagine. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD per .NET ha esposto le classi [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) e [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) per la filtrazione. La classe BilateralSmoothingFilterOptions necessita di un intero come dimensione. I passaggi per eseguire il ridimensionamento sono semplici come segue:

1. Carica un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
1. Converti l'immagine in RasterImage.
1. Crea un'istanza delle classi BilateralSmoothingFilterOptions e SharpenFilterOptions.
1. Chiama il metodo [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) specificando il rettangolo come limiti dell'immagine e un'istanza della classe BilateralSmoothingFilterOptions.
1. Chiama il metodo [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) specificando il rettangolo come limiti dell'immagine e un'istanza della classe SharpenFilterOptions.
1. Regola il contrasto
1. Imposta la luminosità
1. Salva i risultati.


## **Utilizza l'algoritmo di soglia di Bradley**
La sogliatura dell'immagine è utilizzata nelle applicazioni grafiche. L'obiettivo della sogliatura di un'immagine è classificare i pixel come "scuri" o "chiari". L'API di Aspose.PSD ti consente di utilizzare la sogliatura di Bradley durante la conversione delle immagini. La porzione di codice seguente mostra come definire il valore di soglia e quindi invocare l'algoritmo di soglia di Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}

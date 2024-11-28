---
title: Ritaglia, Ruota e Ridimensiona Immagini
type: docs
weight: 40
url: /it/net/ritaglia-ruota-e-ridimensiona-immagini/
---

## **Ritaglio Immagini**
Il ritaglio delle immagini si riferisce generalmente alla rimozione delle parti esterne di un'immagine per migliorare l'inquadratura. Il ritaglio può anche essere utilizzato per tagliare una parte dell'immagine al fine di aumentare il focus su un'area particolare. L'API di Aspose.PSD supporta due approcci diversi al ritaglio delle immagini: mediante spostamenti e rettangoli.
### **Ritaglio con Spostamenti**
La classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) fornisce una versione sovraccaricata del metodo Crop che accetta 4 valori interi che indicano Sinistra, Destra, Alto e Basso. In base a questi quattro valori, il metodo Crop muove i confini dell'immagine verso il centro dell'immagine eliminando la porzione esterna. Il frammento di codice seguente dimostra come ritagliare un'immagine con spostamenti.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RitaglioConSpostamenti-RitaglioConSpostamenti.cs" >}}
### **Ritaglio con Rettangolo**
La classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) fornisce un'altra versione sovraccaricata del metodo Crop che accetta un'istanza della classe Rectangle. È possibile tagliare qualsiasi parte di un'immagine fornendo i confini desiderati all'oggetto Rectangle. Il frammento di codice seguente dimostra come ritagliare un'immagine con un rettangolo.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RitaglioConRettangolo-RitaglioConRettangolo.cs" >}}
## **Ruota e Capovolgi un'Immagine**
Aspose.PSD per .NET è una libreria facile da utilizzare in quanto fornisce metodi semplici per eseguire operazioni complesse. Ad esempio, Aspose.PSD per .NET ha fornito il metodo RotateFlip per la sua classe base Image se un'applicazione richiede di ruotare un'immagine. Indipendentemente dal formato dell'immagine, la libreria può eseguire una specifica procedura di Rotazione & Capovolgimento su di essa.
### **Rotazione di un'Immagine**
Il metodo Image.RotateFlip può essere utilizzato per ruotare l'immagine di 90/180/270 gradi e capovolgerla orizzontalmente o verticalmente. Il metodo Image.RotateFlip accetta un parametro di tipo RotateFlipType che specifica il tipo di rotazione e capovolgimento da applicare all'immagine. I passaggi per eseguire Rotazione & Capovolgimento sono semplici come di seguito,

1. Caricare l'immagine utilizzando il metodo factory Load esposto dalla classe Image.
1. Chiamare il metodo Image.RotateFlip specificando l'opportuno RotateFlipType.
1. Salvare i risultati.

L'esempio di codice seguente dimostra come impostare la proprietà RotateFlip di un'immagine e l'enumerazione RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RuotareUnImmagine-RuotareUnImmagine.cs" >}}
## **Ruotare un'Immagine su un Angolo Specifico**
Aspose.PSD per .NET API espone il metodo [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate per facilitare gli utenti che desiderano ruotare un'immagine su un angolo specifico. A differenza del metodo [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, il metodo [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate accetta tre parametri:

1. Angolo di rotazione: un parametro di tipo float che specifica l'angolo di rotazione con cui l'immagine deve essere ruotata. Un valore positivo ruota l'immagine in senso orario; un valore negativo esegue una rotazione in senso antiorario.
1. Ridimensiona proporzionalmente: un parametro di tipo Boolean che specifica se le dimensioni dell'immagine devono essere modificate in base alle proiezioni del rettangolo ruotato (punti angolari). Se impostato su false, le dimensioni dell'immagine rimarrebbero invariate e solo i contenuti interni dell'immagine verrebbero ruotati.
1. Colore di sfondo: un parametro di tipo Color che specifica il colore da riempire sullo sfondo dell'immagine ruotata.

Il frammento di codice seguente dimostra l'utilizzo del metodo [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RuotareUnImmagineSuUnAngoloSpecifico-RuotareUnImmagineSuUnAngoloSpecifico.cs" >}}
## **Ridimensiona Immagini**
Questo articolo dimostra l'uso di Aspose.PSD per .NET per eseguire l'operazione di Ridimensionamento su un'immagine. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da usare per raggiungere questo obiettivo. Aspose.PSD per .NET ha esposto il metodo Resize per la classe Image che può essere utilizzato per ridimensionare le immagini esistenti al volo. Ci sono due sovraccarichi del metodo Resize per soddisfare le esigenze dell'applicazione.
### **Ridimensionamento Semplice**
I passaggi per eseguire il ridimensionamento sono semplici come di seguito:

1. Caricare l'immagine utilizzando il metodo factory Load esposto dalla classe Image.
1. Chiamare il metodo Image.Resize specificando la nuova Altezza e Larghezza.
1. Salvare i risultati.

L'esempio di codice seguente dimostra come ridimensionare un'immagine.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RidimensionamentoSemplice-RidimensionamentoSemplice.cs" >}}
### **Ridimensionamento con Enumerazione ResizeType**
Aspose.PSD API ha esposto l'enumerazione ResizeType che può essere utilizzata con Image.Resize per ottenere i risultati desiderati. Il frammento di codice fornito di seguito dimostra l'utilizzo dell'enumerazione ResizeType, mentre i dettagli dei membri dell'enumerazione ResizeType possono essere trovati in fondo a questa pagina.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RidimensionamentoconEnumerazioneResizeType-RidimensionamentoconEnumerazioneResizeType.cs" >}}



Se si desidera ottenere un risultato di qualità dopo l'applicazione del ridimensionamento, è consigliabile utilizzare sempre ResizeType.LanczosResample poiché produrrà risultati di alta qualità ma potrebbe funzionare più lentamente rispetto a ResizeType.NearestNeighbourResample. D'altra parte, l'algoritmo ResizeType.NearestNeighbourResample è specificamente utilizzato per il ridimensionamento veloce a discapito della qualità dell'immagine. Questo metodo può essere utile per la generazione di miniature in tempo reale o processi simili in cui è richiesta la performance.
## **Ridimensionare un'Immagine Proporzionalmente**
È possibile ridimensionare le immagini passando nuove altezza e larghezza come parametri al metodo Image.Resize ma in tal caso è necessario calcolare il rapporto d'aspetto da soli. Questo perché quando la larghezza o l'altezza di un'immagine viene alterata, l'immagine viene ridimensionata o rimpicciolita per riempire la nuova dimensione . Se le modifiche alla larghezza e all'altezza di un'immagine non sono proporzionali, ciò può portare a un risultato allungato e distorto. Questo articolo dimostra l'uso di Aspose.PSD per .NET API per ridimensionare le immagini passando sia la nuova altezza che la larghezza consentendo all'API di calcolare automaticamente l'altro valore proporzionale.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingAndFormattingImages-RidimensionareImmagineProporzionalmente-RidimensionareImmagineProporzionalmente.cs" >}}
### **Enumerazione ResizeType**
ResizeType determina il tipo di ridimensionamento da eseguire sull'immagine in base al filtro selezionato.

Membri dell'Enumerazione [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Nome Membro**|**Valore**|**Descrizione**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Il punto in alto a sinistra della nuova immagine coinciderà con il punto in alto a sinistra dell'immagine originale. Il ritaglio avverrà se necessario.|
|RightTopToRightTop|1|Il punto in alto a destra della nuova immagine coinciderà con il punto in alto a destra dell'immagine originale. Il ritaglio avverrà se necessario.|
|RightBottomToRightBottom|2|Il punto in basso a destra della nuova immagine coinciderà con il punto in basso a destra dell'immagine originale. Il ritaglio avverrà se necessario.|
|LeftBottomToLeftBottom|3|Il punto in basso a sinistra della nuova immagine coinciderà con il punto in basso a sinistra dell'immagine originale. Il ritaglio avverrà se necessario.|
|CenterToCenter|4|Il centro della nuova immagine coinciderà con il centro dell'immagine originale. Il ritaglio avverrà se necessario.|
|LanczosResample|5|Ridimensionare utilizzando l'algoritmo Lanczos utilizzando una maschera 7x7.|
|NearestNeighbourResample|6|Ridimensionare utilizzando l'algoritmo del vicino più vicino.|

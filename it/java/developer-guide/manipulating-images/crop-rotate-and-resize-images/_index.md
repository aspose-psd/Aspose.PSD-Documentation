---
title: Ritaglia, Ruota e Ridimensiona Immagini
type: docs
weight: 40
url: /it/java/ritaglia-ruota-e-ridimensiona-immagini/
---

## **Ritaglio Immagini**
Il ritaglio delle immagini si riferisce di solito alla rimozione delle parti esterne di un'immagine per migliorarne l'inquadratura. Il ritaglio può anche essere utilizzato per tagliare una parte dell'immagine al fine di aumentare il focus su un'area specifica. L'API di Aspose.PSD supporta due approcci differenti al ritaglio delle immagini: per spostamenti e per rettangolo.
### **Ritaglio per Spostamenti**
La classe RasterImage fornisce una versione sovraccaricata del metodo Crop che accetta 4 valori interi che indicano Sinistra, Destra, Alto e Basso. Sulla base di questi quattro valori, il metodo Crop sposta i confini dell'immagine verso il centro dell'immagine scartando la parte esterna. Il frammento di codice sottostante mostra come ritagliare un'immagine per spostamenti.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RitaglioPerSpostamenti-RitaglioPerSpostamenti.java" >}}
### **Ritaglio per Rettangolo**
La classe RasterImage fornisce un'altra versione sovraccaricata del metodo Crop che accetta un'istanza della classe Rectangle. È possibile tagliare qualsiasi parte di un'immagine fornendo i confini desiderati all'oggetto Rectangle. Il frammento di codice sottostante mostra come ritagliare un'immagine per Rettangolo.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RitaglioPerRettangolo-RitaglioPerRettangolo.java" >}}
## **Ruota e Capovolgi un'Immagine**
Aspose.PSD per Java è una libreria facile da utilizzare perché fornisce metodi semplici per eseguire operazioni complesse. Ad esempio, Aspose.PSD per Java ha fornito il metodo RotateFlip per la sua classe di base Image se un'applicazione richiede di ruotare un'immagine. Indipendentemente dal formato dell'immagine, la libreria può eseguire una procedura specifica di Rotazione & Capovolgimento su di essa.
### **Ruotare un'Immagine**
Il metodo Image.RotateFlip può essere utilizzato per ruotare l'immagine di 90/180/270 gradi e capovolgere l'immagine orizzontalmente o verticalmente. Il metodo Image.RotateFlip accetta un parametro di tipo RotateFlipType che specifica il tipo di rotazione e capovolgimento da applicare all'immagine. I passaggi per eseguire la Rotazione & Capovolgimento sono semplici come segue,

1. Caricare un'immagine utilizzando il metodo di fabbrica Load esposto dalla classe Image.
1. Chiamare il metodo Image.RotateFlip specificando il RotateFlipType appropriato.
1. Salvare i risultati.

L'esempio di codice seguente mostra come impostare la proprietà RotateFlip di un'immagine e l'enumerazione RotateFlipType.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RuotareUnImmagine-RuotareUnImmagine.java" >}}
## **Ruotare un'Immagine su un Angolo Specifico**
Aspose.PSD per Java API espone il metodo RasterImage.Rotate per agevolare gli utenti che desiderano ruotare un'immagine su un angolo specifico. A differenza del metodo RasterImage.RotateFlip, il metodo RasterImage.Rotate accetta tre parametri:

1. Angolo di rotazione: Un parametro di tipo float che specifica l'angolo di rotazione con cui l'immagine deve essere ruotata. Un valore positivo ruota l'immagine in senso orario; un valore negativo esegue una rotazione in senso antiorario.
1. Ridimensionare proporzionalmente: Un parametro di tipo booleano specifica se le dimensioni dell'immagine devono essere modificate in base alle proiezioni del rettangolo ruotato (punti angolari). Se impostato su false, le dimensioni dell'immagine rimarranno invariate e verranno ruotati solo i contenuti interni dell'immagine.
1. Colore di sfondo: Un parametro di tipo Colore specifica il colore da riempire allo sfondo dell'immagine ruotata.

Il frammento di codice sottostante mostra l'utilizzo del metodo RasterImage.Rotate.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RuotareUnImmagineSuUnAngoloSpecifico-RuotareUnImmagineSuUnAngoloSpecifico.java" >}}
## **Ridimensionamento Immagini**
Questo articolo mostra l'utilizzo di Aspose.PSD per Java per eseguire operazioni di Ridimensionamento su un'immagine. Le API di Aspose.PSD hanno esposto metodi efficienti e facili da utilizzare per raggiungere questo obiettivo. Aspose.PSD per Java ha esposto il metodo Resize per la classe Image che può essere utilizzato per ridimensionare immagini esistenti al volo. Ci sono due sovraccarichi del metodo Resize per adattarsi alle esigenze dell'applicazione.
### **Semplice Ridimensionamento**
I passaggi per eseguire il Ridimensionamento sono semplici come segue:

1. Carica un'immagine usando il metodo di fabbrica Load esposto dalla classe Image.
1. Chiama il metodo Image.Resize specificando l'Altezza e la Larghezza nuove.
1. Salva i risultati.

L'esempio di codice seguente mostra come Ridimensionare un'immagine.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RidimensionamentoSemplice-RidimensionamentoSemplice.java" >}}
### **Ridimensionamento con Enumerazione ResizeType**
Aspose.PSD API ha esposto l'enumerazione ResizeType che può essere utilizzata con Image.Resize per ottenere i risultati desiderati. Il frammento di codice fornito di seguito mostra l'utilizzo dell'enumerazione ResizeType, mentre i dettagli dei membri dell'enumerazione ResizeType possono essere trovati in fondo a questa pagina.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RidimensionamentoconEnumerazioneResizeType-RidimensionamentoconEnumerazioneResizeType.java" >}}



Se si desidera ottenere risultati di alta qualità dopo l'applicazione del ridimensionamento, è consigliabile utilizzare sempre ResizeType.LanczosResample in quanto produrrà risultati di alta qualità ma potrebbe funzionare più lentamente rispetto a ResizeType.NearestNeighbourResample. D'altra parte, l'algoritmo ResizeType.NearestNeighbourResample è utilizzato specificamente per un ridimensionamento rapido con un compromesso sulla qualità dell'immagine. Questo metodo può essere utile per la generazione di miniature in tempo reale o processi simili dove è richiesta la massima velocità.
## **Ridimensionamento Proporzionale dell'Immagine**
È possibile ridimensionare le immagini passando nuove altezze e larghezze come parametri al metodo Image.Resize ma in tal caso è necessario calcolare il rapporto di aspetto da soli. Questo perché quando la larghezza o l'altezza di un'immagine viene modificata, l'immagine viene ridimensionata o rimpicciolita per riempire le nuove dimensioni. Se le modifiche alla larghezza e all'altezza di un'immagine non sono proporzionate, ciò può portare a risultati stirati e distorti. Questo articolo illustra l'uso di Aspose.PSD per l'API di Java per ridimensionare le immagini passando solo una nuova altezza o larghezza consentendo all'API di calcolare automaticamente l'altro valore proporzionale.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-principale-java-com-aspose-psd-esempi-DisegnoEFormattazioneImmagini-RidimensionamentoProporzionaledellImmagine-RidimensionamentoProporzionaledellImmagine.java" >}}
### **Enumerazione ResizeType**
ResizeType determina il tipo di ridimensionamento da eseguire sull'immagine in base al filtro selezionato.

Membri dell'Enumerazione ResizeType

|**Nome Membro**|**Valore**|**Descrizione**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Il punto in alto a sinistra della nuova immagine coinciderà con il punto in alto a sinistra dell'immagine originale. Il ritaglio avverrà se necessario.|
|RightTopToRightTop|1|Il punto in alto a destra della nuova immagine coinciderà con il punto in alto a destra dell'immagine originale. Il ritaglio avverrà se necessario.|
|RightBottomToRightBottom|2|Il punto in basso a destra della nuova immagine coinciderà con il punto in basso a destra dell'immagine originale. Il ritaglio avverrà se necessario.|
|LeftBottomToLeftBottom|3|Il punto in basso a sinistra della nuova immagine coinciderà con il punto in basso a sinistra dell'immagine originale. Il ritaglio avverrà se necessario.|
|CenterToCenter|4|Il centro della nuova immagine coinciderà con il centro dell'immagine originale. Il ritaglio avverrà se necessario.|
|LanczosResample|5|Campionatura utilizzando l'algoritmo di Lanczos usando una maschera 7x7.|
|NearestNeighbourResample|6|Campionatura utilizzando l'algoritmo del vicino più prossimo.|

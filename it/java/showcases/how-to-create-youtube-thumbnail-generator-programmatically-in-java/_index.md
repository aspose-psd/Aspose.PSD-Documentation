---
title: Come creare un generatore di miniature di YouTube in Java
type: docs
weight: 10
url: /it/java/come-creare-un-generatore-di-miniature-di-youtube-programmaticamente-in-java/
---

## **Introduzione**
Lo scopo di questo documento è quello di dimostrare l'utilizzo dell'API di alcuni strumenti composti di [Aspose.PSD for Java](https://products.aspose.com/psd/java) su un esempio del mondo reale. In questo articolo, **verrà scritto ed esaminato un semplice programma Java che genera miniature di YouTube** per il canale [DW Documentary](https://www.youtube.com/channel/UCW39zufHfsuGgpLviKh297Q). Questo canale è stato scelto dal mondo reale perché le sue miniature sono abbastanza standard e illustrano l'utilizzo di alcuni strumenti composti popolari di Aspose.PSD for Java (ad esempio, effetto di [ombra](/psd/it/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), riempimento radiale a gradiente, disegno di testi e forme):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **Funzionamento in breve**
Un semplice programma Java prende in input due argomenti: una didascalia e un'immagine. Viene generato un **documento Photoshop (PSD) in memoria** da quell'input utilizzando Aspose.PSD for Java. Successivamente, il programma **converte il documento da PSD a PNG** per ottenere una miniatura di YouTube con una dimensione di 1280x720 pixel. L'immagine di output assomiglia a quella seguente:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **Requisiti tecnici**
Le seguenti tecnologie sono necessarie per eseguire con successo il codice di questo articolo:

- Java 6+
- [Aspose.PSD for Java](/psd/it/java/installation/) (ultimo)

## **Per iniziare**
Come già accennato, il programma utilizza un PSD in memoria per generare una miniatura. Quindi, permettiamo di **creare un documento PSD**, per cominciare:

PsdImage psdImage = new PsdImage(1280, 720);

Se osservi più attentamente la miniatura di YouTube sopra, potresti notare che **è composta da diversi componenti**:

1. un'immagine di sfondo (maschera stampata)
2. un riempimento a gradiente radiale PSD (evidenzia l'area in alto a destra)
3. un logotipo con un effetto ombra
4. una didascalia e un disegno semplice (rettangolo blu)

Permettiamo di approfondire per vedere come implementare ciascuno di questi componenti utilizzando Aspose.PSD for Java nelle prossime sezioni.

## **1. Aggiungi un'immagine di sfondo**
L'ordine dei livelli è importante. Pertanto, un'immagine di sfondo deve essere aggiunta per prima per non coprire gli altri livelli. Presta attenzione che adesso sono supportati solo [formati file raster](/psd/it/java/supported-file-formats/) al momento.
### **1.1. Aggiungi un'immagine di sfondo a un livello di Photoshop**
Per **aggiungere un'immagine raster a un PSD**, è necessario passare un flusso di input come argomento durante la costruzione del livello (vedi più [esempi di caricamento di immagini raster](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}

### **1.2. Adatta l'immagine di sfondo al canvas**
Le seguenti 2 azioni (ridimensionamento, posizionamento) sono utili per quei casi in cui **la dimensione dell'immagine differisce dalla dimensione del canvas**, anche se l'immagine in questo articolo ha la stessa dimensione del canvas (assumiamo che non sarà sempre così).

Assicurati che l'immagine caricata si **adatti** alla **dimensione del canvas** (vedi più [esempi di ridimensionamento](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}

Dopo il ridimensionamento, la posizione dell'immagine cambia. Pertanto, per **ripristinare la posizione dell'immagine**, sposta l'immagine ridimensionata nell'angolo in alto a sinistra:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}

## **2. Aggiungi un gradiente radiale**
Ci sono **due modi per aggiungere un gradiente radiale**, utilizzando:

- un [effetto sovrapposizione gradiente](/psd/it/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163) su un livello esistente (un effetto gradiente che si lega al livello corrente e si applica al suo contenuto)
- un nuovo [livello di riempimento a gradiente](/psd/it/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) (un livello separato con una configurazione autonoma del gradiente)

Basta utilizzare l'effetto sovrapposizione gradiente per questo esempio. Tuttavia, per rendere questo articolo più interessante e utile **viene utilizzato il livello di riempimento con gradiente** poiché tutti gli effetti dei livelli si applicano in modo simile e verrà utilizzato un altro effetto di layer nella prossima sezione.
### **2.1. Aggiungi un livello di riempimento a gradiente radiale**
Il processo di aggiunta di un nuovo livello di riempimento a gradiente consiste nei seguenti 2 passaggi:

1. È necessario **dichiarare le impostazioni di riempimento a gradiente** poiché non sono predefinite. La configurazione minima richiesta appare come segue (il tipo di gradiente, la scala, i punti di colore e trasparenza sono proprietà necessarie):

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}

La configurazione sopra dichiara un gradiente radiale che è trasparente ai bordi e blu scuro al centro. La posizione del gradiente è al centro del canvas per impostazione predefinita.

Per invertire il riempimento a gradiente e spostarlo leggermente in alto a destra, utilizzare proprietà facoltative corrispondenti:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}

2. Quando la configurazione è pronta, aggiungi un livello di riempimento a gradiente insieme alle sue impostazioni in PSD:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}

## **Aggiungi un logotipo con un'ombra**
L'**ombra** è un effetto che consente di aggiungere un'ombra personalizzata lungo il contorno dell'oggetto (immagine, testo ecc.).
### **3.1. Aggiungi un logotipo a un livello di Photoshop**
Lo stesso approccio della sezione 1.1. può essere utilizzato per **aggiungere un logotipo in un PSD**:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}

### **3.2. Posiziona il logotipo**
L'immagine caricata è strettamente aderente all'angolo in alto a sinistra per impostazione predefinita. Tuttavia, devono essere aggiunti alcuni **margini** per assomigliare alla miniatura di YouTube originale sul canale. Pertanto, la posizione dell'immagine deve essere spostata dai bordi del livello:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}

### **3.3. Aggiungi un effetto ombra al logotipo**
Il logotipo può essere invisibile se viene utilizzata un'immagine di sfondo chiara. Pertanto, è desiderabile **aggiungere un effetto ombra** a un logotipo tramite la proprietà delle opzioni di mescolamento (vedi altri [esempi di ombreggiatura](/psd/it/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect)):

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}

L'effetto ombra non ha le proprietà necessarie a causa della configurazione predefinita (è simile a quello di Photoshop). Tuttavia, l'ombra sopra è modificata per assomigliare a un bordo traslucido sfocato sui bordi.

## **4. Aggiungi un disegno di testo e di una forma**
### **3.1. Crea un livello grafico**
Il disegno non è supportato direttamente da un livello regolare. Pertanto, viene utilizzato il motore grafico accanto al livello per **fornire un'API per il disegno** (vedi altri [esempi di disegno](/psd/it/java/drawing-images-using-graphics/)):

Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **nuovo** Graphics(graphicLayer);

### **3.2. Disegna del testo multilinea**
Un lettore esperto potrebbe chiedersi: perché non utilizzare un livello di testo per aggiungere un testo? Beh, ci sono un paio di motivi: in questo caso non è richiesta la modifica del testo perché il PSD è generato da zero ogni volta; la personalizzazione del carattere non è supportata dall'API del [testo](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers) ancora (v20.6 al momento della scrittura).

È facile **disegnare del testo con un carattere personalizzato** istanziare semplicemente un carattere desiderabile e invocare il metodo corrispondente dal motore grafico. Tuttavia, rendere un rettangolo (vedi dettagli nella prossima sezione) che cambia automaticamente la sua altezza in base al numero di righe di testo è un po' più difficile. La altezza esatta di tutte le righe deve essere calcolata prima:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}

Dove 1.15 è l'altezza della riga, 3 è il padding del testo.

### **3.3. Disegna un rettangolo**
Anche un rettangolo è facile da disegnare anche con una pennello a gradiente (basta impostare un'area da disegnare e un intervallo di colori). Quando l'altezza del testo è nota, si calcolano le dimensioni e la posizione del rettangolo. Per **disegnare un rettangolo riempito** **in psd** (non solo un contorno) chiama il metodo corrispondente dal motore grafico con tutto ciò:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}

` `Dove 40, 15, 25 sono rientranze.

## **Risultato**
Quindi, la creazione della miniatura è terminata. Pertanto, è il momento di **esportare la miniatura in un formato di file raster** (ad esempio, PNG) per la distribuzione successiva:

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}

## **Conclusione**
In questo articolo, abbiamo creato un generatore di miniature di YouTube per il canale DW Documentary e spiegato come utilizzare alcuni degli strumenti composti più popolari come l'effetto di ombra, il riempimento a gradiente radiale, il disegno di testi e forme.

## **Esempio Completo**
Puoi [scaricare Aspose.PSD SDK](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-YouTubeThumbnailGenerator.java" >}}
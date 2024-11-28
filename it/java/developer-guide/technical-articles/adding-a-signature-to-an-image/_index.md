---
title: Aggiungere una Firma a un'Immagine
type: docs
weight: 10
url: /it/java/aggiungere-una-firma-a-un-immagine/
---

## **Aggiungere una Firma**

Aggiungere una firma a un'immagine è a volte necessario per firmare digitalmente le immagini al fine di evitare la contraffazione. Un altro pensiero potrebbe essere trattare l'immagine più come se venisse mostrata in una galleria. Qualunque sia il motivo, le API Aspose.PSD forniscono la funzionalità di aggiungere una firma a un'immagine utilizzando il meccanismo più semplice come spiegato di seguito. Si prega di notare che questo esempio fa uso della classe Graphics per disegnare un'altra immagine con la firma sull'immagine originale. Per dimostrare l'operazione, caricheremo un'immagine PSD dal disco e disegneremo un'altra immagine come firma sull'immagine originale utilizzando il metodo DrawImage della classe Graphics. Salveremo l'immagine risultante in formato PNG utilizzando la classe PngOptions. Di seguito è riportato un esempio di codice che dimostra come aggiungere una firma a un'immagine. Il codice di esempio è stato suddiviso in parti per renderlo facile da seguire. Passo dopo passo, l'esempio mostra come:

- Caricare le immagini primaria e secondaria (firma).
- Creare e inizializzare un oggetto Graphics.
- Disegnare un'immagine utilizzando il metodo DrawImage della classe Graphics.
- Salvare il risultato in formato PNG.
### **Esempi di Programmi**
#### **Caricamento delle Immagini**
Innanzitutto, creare istanze della classe Image per caricare le immagini di esempio dal disco.
#### **Creazione e Inizializzazione di un Oggetto Grafico**
Dopo aver caricato le immagini, creare e inizializzare un oggetto della classe Graphics utilizzando l'oggetto dell'immagine primaria.
#### **Disegnare l'Immagine Secondaria sull'Immagine Primaria**
Successivamente, utilizzando il metodo DrawImage della classe Graphics, aggiungere l'immagine secondaria all'immagine primaria. Ci sono diversi sovraccarichi del metodo DrawImage che accettano un oggetto di tipo Image come primo parametro mentre tutti gli altri parametri corrispondono alla posizione in cui l'immagine deve essere disegnata. Per scopi dimostrativi, il seguente codice utilizza la versione sovraccarica di DrawImage che accetta un oggetto di tipo Point come secondo parametro e cerca di disegnare la firma nell'angolo in basso a destra dell'immagine primaria.
#### **Salvare l'Immagine**
Infine, salvare l'immagine sul disco locale come file PNG utilizzando la classe PngOptions.
#### **Codice Sorgente Completo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}

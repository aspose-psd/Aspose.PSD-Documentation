---
title: Aggiungere una firma a un'immagine
type: docs
weight: 70
url: /it/net/aggiungere-una-firma-a-unimmagine/
---

## **Aggiungere una firma**

Aggiungere una firma a un'immagine è talvolta necessario per firmare digitalmente le immagini e evitare la contraffazione. Un altro motivo potrebbe essere trattare l'immagine come se fosse esposta in una galleria. Qualunque sia la ragione, le API Aspose.PSD forniscono la funzionalità di aggiungere una firma a un'immagine utilizzando il meccanismo più semplice come spiegato di seguito. Si prega di notare che questo esempio fa uso della classe [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) per disegnare un'altra immagine con la firma sull'immagine originale. Per dimostrare l'operazione, caricheremo un'immagine PSD da disco e disegneremo un'altra immagine come firma sull'immagine originale utilizzando il metodo [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage) della classe Graphics. Salveremo l'immagine risultante in formato PNG utilizzando la classe [PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions). Di seguito è riportato un esempio di codice che illustra come aggiungere una firma a un'immagine. Il codice di esempio è stato diviso in parti per renderlo più facile da seguire. Passo dopo passo, l'esempio mostra come:

- Caricare le immagini primaria e secondaria (firma).
- Creare e inizializzare un oggetto Graphics.
- Disegnare l'immagine utilizzando il metodo DrawImage della classe Graphics.
- Salvare il risultato in formato PNG.

### **Campioni di Programma**

#### **Caricamento Immagini**
Innanzitutto, creare istanze della classe Image per caricare le immagini di esempio da disco.

#### **Creazione e Inizializzazione di un Oggetto Grafico**
Dopo aver caricato le immagini, creare e inizializzare un oggetto della classe Graphics utilizzando l'oggetto dell'immagine primaria.

#### **Disegno dell'Immagine Secondaria sull'Immagine Primaria**
Successivamente, utilizzando il metodo DrawImage della classe Graphics, aggiungere l'immagine secondaria all'immagine primaria. Ci sono diverse sovrapposizioni del metodo DrawImage che accettano un oggetto dell'Immagine come primo parametro mentre tutti gli altri parametri corrispondono alla posizione in cui l'immagine deve essere disegnata. Per scopi dimostrativi, il seguente codice utilizza la versione di sovrapposizione del DrawImage che accetta un oggetto del Punto come secondo parametro e cerca di disegnare la firma nell'angolo in basso a destra dell'immagine primaria.

#### **Salvataggio dell'Immagine**
Infine, salvare l'immagine nuovamente sul disco locale come file PNG utilizzando la classe PngOptions.

#### **Codice Sorgente Completo**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-DrawingImages-AggiungiFirmaAImmagine-AggiungiFirmaAImmagine.cs" >}}

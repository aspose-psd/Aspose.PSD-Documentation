---
title: Evita la degradazione delle prestazioni durante il disegno su immagini compresse
type: docs
weight: 10
url: /it/net/evita-la-degradazione-delle-prestazioni-durante-il-disegno-su-immagini-comprese/
---

## **Evita la degradazione delle prestazioni durante il disegno su immagini compresse**
Ci sono momenti in cui si desidera eseguire operazioni grafiche estremamente complesse su un'immagine compressa. Quando Aspose.PSD deve comprimere e decomprimere immagini al volo, potrebbe verificarsi una degradazione delle prestazioni. Disegnare su immagini compresse potrebbe comportare anche una penalità sulle prestazioni.
### **Soluzione**
Per evitare la degradazione delle prestazioni, consigliamo di convertire l'immagine in un formato non compresso, o grezzo, prima di eseguire operazioni grafiche.
### **Utilizzo del percorso del file**
Nell'esempio seguente, un'immagine PSD viene convertita in formato grezzo (senza compressione) e salvata su disco. L'immagine non compressa viene quindi caricata nuovamente prima che vengano eseguite operazioni grafiche su di essa. La stessa tecnica si applica anche ai file BMP e GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImmagineNonCompressaUtilizzandoFile-ImmagineNonCompressaUtilizzandoFile.cs" >}}
### **Utilizzo di un oggetto Stream**
Di seguito viene mostrato come l'immagine PSD viene convertita in formato grezzo (senza compressione) e salvata su disco utilizzando MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Esempi-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImmagineNonCompressaOggettoStream-ImmagineNonCompressaOggettoStream.cs" >}}

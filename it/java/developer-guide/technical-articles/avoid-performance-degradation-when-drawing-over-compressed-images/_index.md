---
title: Evitare la degradazione delle prestazioni durante il disegno su immagini compresse
type: docs
weight: 40
url: /it/java/evitare-degradazione-prestazioni-disegno-immagini-compresse/
---

## **Evitare la degradazione delle prestazioni durante il disegno su immagini compresse**
Ci sono momenti in cui si desidera eseguire operazioni grafiche estremamente intensive su un'immagine compressa. Quando Aspose.PSD deve comprimere e decomprimere immagini al volo, potrebbe verificarsi una degradazione delle prestazioni. Disegnare su immagini compresse può comportare anche una penalità sulle prestazioni.
### **Soluzione**
Per evitare la degradazione delle prestazioni, ti consigliamo di convertire l'immagine in un formato non compresso, o grezzo, prima di eseguire operazioni grafiche.
### **Utilizzo del percorso del file**
Nell'esempio che segue, un'immagine PSD viene convertita in formato grezzo (senza compressione) e salvata su disco. L'immagine non compressa viene quindi ricaricata prima di eseguire operazioni grafiche su di essa. La stessa tecnica si applica anche ai file BMP e GIF.



{{< gist "aspose-com-gists" "9030f785bf7a3c0fa2df0be268147778" "Esempi-src-main-java-com-aspose-psd-esempi-ModificaEConversioneImmagini-PSD-ImmagineNonCompressaUtilizzandoFile-ImmagineNonCompressaUtilizzandoFile.java" >}}
### **Utilizzo di un oggetto Stream**
Il seguente snippet di codice mostra come un'immagine PSD viene convertita in formato grezzo (senza compressione) e salvata su disco utilizzando Stream.



{{< gist "aspose-com-gists" "9030f785bf7a3c0fa2df0be268147778" "Esempi-src-main-java-com-aspose-psd-esempi-ModificaEConversioneImmagini-PSD-ImmagineNonCompressaOggettoStream-ImmagineNonCompressaOggettoStream.java" >}}

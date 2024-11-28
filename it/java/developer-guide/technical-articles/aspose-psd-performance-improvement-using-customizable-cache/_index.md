---
title: Miglioramento delle prestazioni di Aspose.PSD utilizzando una cache personalizzabile
type: docs
weight: 30
url: /it/java/aspose-psd-miglioramento-delle-prestazioni-utilizzando-cache-personalizzabile/
---

## **Miglioramento delle prestazioni con cache personalizzabile**
Aspose.PSD utilizza la memorizzazione nella cache per lo stoccaggio temporaneo dei dati. Il meccanismo è semplice da utilizzare, personalizzabile e trasparente. Garantisce che non ci siano problemi di prestazioni durante l'elaborazione delle immagini. Questo articolo spiega come personalizzare la cache con l'API Aspose.PSD per Java.

### **Personalizzazione della cache**
Quando un processo necessita di memorizzazione temporanea dei dati, questa memorizzazione viene allocata nella cache. La cache può essere spazio in memoria o su disco e viene impostata dall'utente. Quando i dati temporanei non sono più necessari, lo spazio viene rilasciato. Le statistiche dello spazio allocato possono essere ispezionate in qualsiasi momento. Come Aspose.PSD alloca e utilizza le cache può essere personalizzato. Questa sezione descrive le varie impostazioni e i relativi valori predefiniti e i frammenti di codice di seguito mostrano come possono essere utilizzati.

### **Impostazione del luogo di allocazione della cache**
Per personalizzare come viene allocato lo spazio della cache, impostare la proprietà CacheType. Per impostazione predefinita, la cache viene allocata in memoria e quando non c'è più spazio disponibile in memoria, viene allocata su disco. Questo comportamento è catturato dalla modalità Auto. La modalità Auto è flessibile e massimizza le prestazioni. Ci sono anche altre modalità:

- Modalità CacheOnDiskOnly: allocazione solo su disco.
- Modalità CacheInMemoryOnly: allocazione solo in memoria.

La selezione della modalità CacheOnDiskOnly può comportare prestazioni scadenti.

### **Impostazione delle dimensioni della cache**
Impostare lo spazio massimo (in byte) che può essere allocato su disco o memoria impostando rispettivamente le proprietà MaxDiskSpaceForCache e MaxMemoryForCache. Per impostazione predefinita, entrambi i valori sono impostati su 0, il che significa che non c'è un limite superiore.

### **Controllo della riallocazione della cache**
Se non vi è abbastanza spazio disponibile in memoria (come specificato dalla proprietà MaxMemoryForCache) quando viene allocata una nuova cache, la cache viene allocata su disco. Se non c'è abbastanza spazio su disco, viene generata un'eccezione. Il processo di allocazione della cache si sposta dalla memoria al disco ma non viceversa. La proprietà ExactReallocateOnly viene utilizzata per controllare la riallocazione della memoria. La riallocazione è molto probabile che avvenga per le cache pre-allocate. Può verificarsi quando il sistema capisce che lo spazio allocato non sarà sufficiente. Se ExactReallocateOnly è impostato sul valore predefinito, False, lo spazio viene riallocato allo stesso mezzo. Quando impostato su True, la riallocazione non può superare lo spazio massimo specificato. In questo caso la cache allocata in memoria esistente (che richiede riallocazione) viene liberata e lo spazio esteso viene allocato su disco.

### **Esempi di programma**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.java" >}}

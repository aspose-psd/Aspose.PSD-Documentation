---
title: Miglioramento delle prestazioni di Aspose.PSD utilizzando una cache personalizzabile
type: docs
weight: 20
url: /it/net/aspose-psd-performance-improvement-using-customizable-cache/
---

## **Migliora le prestazioni con la cache personalizzabile**
[Aspose.PSD](https://products.aspose.com/psd/family) utilizza la cache per lo storage temporaneo dei dati. Il meccanismo è semplice da utilizzare, personalizzabile e trasparente. Garantisce che non ci siano problemi di prestazioni durante l'elaborazione delle immagini. Questo articolo spiega come personalizzare la cache con l'API di Aspose.PSD per .NET.
### **Personalizzazione della cache**
Quando un processo necessita di uno storage temporaneo per i dati, questo storage viene allocato nella cache. La cache può essere nello spazio di memoria o su disco ed è impostata dall'utente. Quando i dati temporanei non sono più necessari, lo spazio viene rilasciato. Le statistiche dello spazio allocato possono essere ispezionate in qualsiasi momento. Come Aspose.PSD alloca e utilizza le cache può essere personalizzato. Questa sezione descrive le varie impostazioni e i rispettivi valori predefiniti e i frammenti di codice di seguito mostrano come possono essere utilizzati.
### **Impostazione del luogo di allocazione della cache**
Per personalizzare come lo spazio di cache viene allocato, impostare la proprietà [CacheType](https://reference.aspose.com/psd/net/aspose.psd/cachetype). Per impostazione predefinita, la cache viene allocata in memoria e quando non c'è più spazio disponibile in memoria, viene allocata su disco. Questo comportamento è catturato da Auto mode. Auto mode è flessibile e massimizza le prestazioni. Ci sono anche altri modi:

- modalità CacheOnDiskOnly: allocazione solo su disco.
- modalità CacheInMemoryOnly: allocazione solo in memoria.

La selezione della modalità CacheOnDiskOnly può comportare prestazioni scadenti.
### **Impostazione delle dimensioni della cache**
Impostare lo spazio massimo (in byte) che può essere allocato su disco o in memoria impostando rispettivamente le proprietà [MaxDiskSpaceForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxdiskspaceforcache) e [MaxMemoryForCache](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/maxmemoryforcache). Per impostazione predefinita, entrambi i valori sono impostati su 0, il che significa che non c'è un limite superiore.
### **Controllo della riallocazione della cache**
Se non c'è spazio sufficiente disponibile in memoria (come specificato dalla proprietà MaxMemoryForCache) quando viene allocata una nuova cache, la cache viene allocata su disco. Se non c'è abbastanza spazio su disco, viene generata un'eccezione. Il processo di allocazione della cache si sposta dalla memoria a disco ma non viceversa. La proprietà [ExactReallocateOnly](https://reference.aspose.com/psd/net/aspose.psd/cache/properties/exactreallocateonly) viene utilizzata per controllare la riallocazione della memoria. La riallocazione è più probabile che avvenga per cache pre-allocate. Può accadere quando il sistema capisce che lo spazio allocato non sarà sufficiente. Se ExactReallocateOnly è impostato sul valore predefinito, False, lo spazio viene riallocato allo stesso mezzo. Quando impostato su True, la riallocazione non può superare lo spazio massimo specificato. In questo caso, la cache allocata esistente in memoria (che richiede riallocazione) viene liberata e lo spazio esteso viene allocato su disco.
### **Esempi di programma**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ControllCacheReallocation-ControllCacheReallocation.cs" >}}

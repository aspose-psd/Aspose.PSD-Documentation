---
title: Esempio di utilizzo dei gruppi di livelli in Aspose.PSD per C#
weight: 100
type: docs
description: Uso del Gruppo di Livelli del File PSD tramite C#
keywords: [gruppo di livelli, gruppo di layer, aggiungere layer a un gruppo, API psd, C#, csharp, esempio di codice]
url: it/net/psd-group-layer/
---

## Panoramica

I gruppi di livelli in Aspose.PSD per C# consentono un'organizzazione ed una manipolazione efficienti dei livelli in un file PSD. Utilizzando i layer di cartelle, è possibile raggruppare più layer insieme e applicare trasformazioni o effetti all'intero gruppo.

Questo esempio dimostra la creazione di una nuova immagine PSD con `PsdImage.Create`. Successivamente, viene creato un nuovo oggetto `LayerGroup` utilizzando `AddLayerGroup` dall'oggetto `PsdImage`. Il layer di gruppo è nominato "Cartella", inserito all'indice 0 e impostato come visibile.

Successivamente, vengono creati due oggetti `Layer` con le loro proprietà `DisplayName` impostate. Questi layer vengono aggiunti al layer di gruppo utilizzando `AddLayer`.

I livelli all'interno del gruppo possono essere acceduti tramite la proprietà `Layers` dell'oggetto `LayerGroup`. Nell'esempio si afferma che i nomi visualizzati dei primi due livelli nel gruppo sono "Layer 1" e "Layer 2".

Dopo aver modificato i gruppi di livelli, l'immagine PSD aggiornata viene salvata con il metodo `Save` dell'oggetto `PsdImage`.

Questo esempio di base introduce il lavoro con i gruppi di livelli utilizzando Aspose.PSD per C#. La libreria offre funzionalità avanzate per la manipolazione e la trasformazione dei livelli nei file PSD. Consulta la documentazione di Aspose.PSD per C# per ulteriori esempi dettagliati e funzionalità.

Ecco un codice di esempio che dimostra l'uso dei gruppi di livelli in Aspose.PSD per C#:

## Esempio

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Per ulteriori informazioni dettagliate ed esempi, visita la [documentazione di Aspose.PSD per C#](https://docs.aspose.com/psd/net/).

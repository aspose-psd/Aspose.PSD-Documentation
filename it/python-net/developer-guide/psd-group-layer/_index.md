---
title: Esempio di utilizzo dei layer di gruppo in Aspose.PSD per Python
weight: 100
type: docs
description: Utilizzo del livello di gruppo del file PSD tramite Python
keywords: [livello di gruppo, layer di gruppo, aggiungere layer al gruppo, psd api, python, esempio di codice]
url: it/python-net/psd-group-layer/
---

## **Panoramica**

Lavorare con i layer di gruppo in Aspose.PSD per Python è una funzionalità potente che ti consente di organizzare e manipolare i layer all'interno di un'immagine PSD. I layer di gruppo, noti anche come layer di cartelle, forniscono un modo per raggruppare più layer insieme e applicare trasformazioni o effetti all'intero gruppo.

In questo esempio, creiamo innanzitutto una nuova immagine PSD utilizzando il metodo PsdImage.create. Quindi, creiamo un nuovo oggetto LayerGroup utilizzando il metodo add_layer_group dell'oggetto PsdImage. Forniamo il nome del layer di gruppo ("Cartella"), l'indice a cui dovrebbe essere inserito (0) e un flag booleano che indica se il layer di gruppo dovrebbe essere visibile (True).

Successivamente, creiamo due oggetti Layer e impostiamo i loro nomi visualizzati utilizzando la proprietà display_name. Aggiungiamo questi layer al layer di gruppo utilizzando il metodo add_layer.

Infine, possiamo accedere ai layer all'interno del gruppo utilizzando la proprietà layers dell'oggetto LayerGroup. Nell'esempio, verifichiamo che i nomi visualizzati dei primi e secondi layer nel gruppo siano rispettivamente "Layer 1" e "Layer 2".

Dopo aver manipolato i layer di gruppo, possiamo salvare l'immagine PSD modificata utilizzando il metodo save dell'oggetto PsdImage.

Questo è solo un esempio di base per aiutarti a iniziare a lavorare con i layer di gruppo utilizzando Aspose.PSD per Python. La libreria fornisce molte altre funzionalità avanzate per manipolare e trasformare i layer all'interno delle immagini PSD. Puoi consultare la documentazione di Aspose.PSD per Python per ulteriori dettagli ed esempi su come lavorare con i layer di gruppo e altre funzionalità della libreria.

Per lavorare con i layer di gruppo in Aspose.PSD per Python, è possibile utilizzare la classe LayerGroup. Qui è riportato un esempio di codice che mostra come creare un layer di gruppo, aggiungervi layer e salvare l'immagine PSD modificata.

Si prega di verificare l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}

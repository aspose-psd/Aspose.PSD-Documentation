---
title: Aggiornamento del livello di riempimento PSD utilizzando Python
weight: 100
type: docs
description: Esempi dell'utilizzo di tutti i tipi di livelli di regolazione inclusi il riempimento a colori, il riempimento a gradiente e il riempimento a motivi
keywords: [livello di riempimento, Riempimento di colore, Riempimento a gradiente, Riempimento a motivi, api psd, python, esempio di codice]
url: it/python-net/psd-riempimento-del-livello-di-modifica/
---

## **Panoramica**

Per creare un livello regolare, è possibile utilizzare la funzione create_regular_layer fornita nel codice. Questa funzione richiede i parametri left, top, width e height per definire la posizione e le dimensioni del livello. Crea un nuovo livello, imposta i suoi limiti e lo riempie con un colore specificato.

Per creare un livello di riempimento a colori, è possibile utilizzare il metodo FillLayer.create_instance con il parametro FillType.COLOR. Dopo aver creato il livello di riempimento, è possibile accedere alle impostazioni di riempimento utilizzando la proprietà fill_settings e impostare il colore utilizzando la proprietà color della classe ColorFillSettings. Nel codice fornito, il colore è impostato su Color.coral. La proprietà di clipping del livello di riempimento è impostata su 1, il che fa sì che il livello funzioni come maschera di ritaglio.

Per creare un livello di riempimento a gradiente, è possibile utilizzare il metodo FillLayer.create_instance con il parametro FillType.GRADIENT. Similmente al livello di riempimento di colore, è possibile accedere alle impostazioni di riempimento utilizzando la proprietà fill_settings e impostare i punti di colore del gradiente e i punti di trasparenza. Nel codice fornito, i punti di colore del gradiente sono definiti utilizzando la classe GradientColorPoint, e i punti di trasparenza sono definiti utilizzando la classe GradientTransparencyPoint. Anche la proprietà di clipping del livello di riempimento è impostata su 1.

Per creare un livello di riempimento a motivi, è possibile utilizzare il metodo FillLayer.create_instance con il parametro FillType.PATTERN. Di nuovo, è possibile accedere alle impostazioni di riempimento utilizzando la proprietà fill_settings e impostare i dati del motivo e altre proprietà. Nel codice fornito, i dati del motivo sono definiti utilizzando la classe PatternFillSettings, e la proprietà di clipping è impostata su 1.

Dopo aver creato i livelli di riempimento, è possibile aggiungerli all'immagine PSD utilizzando il metodo add_layer. È inoltre possibile specificare il nome visualizzato e altre proprietà per ciascun livello di riempimento.

Infine, è possibile salvare l'immagine PSD e l'immagine PNG corrispondente utilizzando il codice fornito. Le opzioni PNG sono impostate per utilizzare il truecolor con alpha per la trasparenza.

Si prega di controllare l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentazione-Python-Aspose-psd-riempimento-del-livello-di-modifica.py" >}}

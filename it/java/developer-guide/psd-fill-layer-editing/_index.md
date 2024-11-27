---
title: Aggiornamento del livello di riempimento PSD utilizzando Java
weight: 100
type: docs
description: Esempi di utilizzo di tutti i tipi di livelli di regolazione, inclusi il riempimento a colori, il riempimento a gradiente e il riempimento a pattern
keywords: [livello di riempimento, Riempimento a colori, Riempimento a gradiente, Riempimento a pattern, API psd, java, esempio di codice]
url: it/java/psd-fill-layer-editing/
---

## **Panoramica**

Creare un livello regolare comporta l'utilizzo della funzione createRegularLayer, che richiede parametri per definire la posizione e le dimensioni del livello. Questa funzione crea un nuovo livello, imposta i suoi limiti e lo riempie con un colore specificato.

Per un livello di riempimento a colori, si utilizza il metodo FillLayer.createInstance con il parametro FillType.Color. Una volta creato il livello di riempimento, si accede alle impostazioni di riempimento tramite la proprietà fill_settings e si imposta il colore desiderato utilizzando la proprietà colore della classe ColorFillSettings. In questo contesto, il colore è impostato su Color.getCoral(). Inoltre, la proprietà di ritaglio del livello di riempimento è impostata su 1, facendolo funzionare come maschera di ritaglio.

I livelli di riempimento a gradiente vengono creati analogamente utilizzando il metodo FillLayer.create_instance, ma con il parametro FillType.Gradient. Come per i livelli di riempimento a colori, si accede alle impostazioni di riempimento tramite fill_settings e si impostano i punti di colore del gradiente e i punti di trasparenza. In questo esempio, i punti di colore del gradiente sono definiti con la classe GradientColorPoint e i punti di trasparenza con la classe GradientTransparencyPoint. Anche la proprietà di ritaglio del livello di riempimento è impostata su 1.

I livelli di riempimento a pattern vengono creati utilizzando FillLayer.createInstance con il parametro FillType.Pattern. Ancora una volta, accedere alle impostazioni di riempimento tramite fill_settings e impostare i dati del pattern e le altre proprietà. In questo codice, i dati del pattern sono definiti utilizzando la classe PatternFillSettings, e la proprietà di ritaglio è impostata su 1.

Una volta creati i livelli di riempimento, aggiungerli all'immagine PSD utilizzando il metodo addLayer, specificando il nome visualizzato e le altre proprietà per ciascun livello di riempimento.

Infine, salvare l'immagine PSD e la relativa immagine PNG con il codice fornito. Le opzioni PNG sono configurate per utilizzare il vero colore con alfa per la trasparenza.

Si prega di fare riferimento all'esempio completo per ulteriori dettagli.

## **Esempio**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-psd-fill-layer-editing.java" >}}

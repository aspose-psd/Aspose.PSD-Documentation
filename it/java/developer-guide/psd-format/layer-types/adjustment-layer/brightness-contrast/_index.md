---
title: Layer di Regolazione Luminosità Contrasto
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/brightness-contrast/
---

# Lavorare con il layer di regolazione luminosità/contrasto di Photoshop in Java

In questo articolo applicheremo la regolazione luminosità/contrasto a un documento di Adobe® Photoshop® utilizzando la libreria Aspose.PSD for Java®. Inoltre, impareremo di più sulle funzionalità della libreria legate a questo tipo di layer di regolazione lungo il percorso.

Ma prima un po' di teoria.

Il layer di regolazione luminosità/contrasto modifica luminosità e contrasto dell'immagine. Ma aspetta un momento, cosa significa esattamente? Aumentare la luminosità schiarisce il valore del colore fino a diventare bianco e diminuire la luminosità scurisce il valore del colore fino a diventare nero. Aumentare il contrasto aumenterà a sua volta la differenza tra colori chiari e scuri e diminuire il contrasto diminuirà tale differenza rispettivamente; ciò significa che i colori chiari diventano più chiari e i colori scuri diventano più scuri.

## Il supporto della modalità colore

La libreria permette di aggiungere un layer di regolazione luminosità/contrasto a immagini in modalità colore RGB, CMYK o Lab.

## Il comportamento attuale e legacy

L'implementazione attuale della libreria (v20.6 al momento della scrittura) utilizza l'algoritmo predefinito di Photoshop che preserva l'intera gamma tonale dalle ombre agli highlights, ma non supporta ancora il comportamento legacy. Ciò significa che la libreria supporta il layer di regolazione luminosità/contrasto in documenti creati nelle ultime versioni di Photoshop (CS4 e successive). Tuttavia, è possibile [richiedere l'implementazione legacy del layer di regolazione luminosità/contrasto](https://forum.aspose.com/c/psd) sul nostro forum se necessario.

## Regolare luminosità e contrasto

Ora descriviamo come funziona l'API di alto livello del layer di regolazione luminosità/contrasto (guardando avanti, l'API è diretta). La classe PsdImage contiene un metodo di fabbrica (addBrightnessContrastAdjustmentLayer) per istanziare la classe BrightnessContrastLayer che è la porta d'ingresso per la regolazione luminosità e contrasto. La classe BrightnessContrastLayer contiene semplicemente una coppia di getter e setter per accedere alle proprietà di luminosità e contrasto e cambiare i loro valori.

![|Esempio di Layer di Regolazione Luminosità/Contrasto in PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Quindi, prendiamo un'immagine di un cane (b), ad esempio, per regolarne la luminosità1 e il contrasto2 (a), utilizzando solo il metodo di fabbrica con gli argomenti corrispondenti, per ottenere infine un'immagine (c) che risulta più vivida:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Note:

1. Il valore della luminosità deve essere compreso tra -150 e 150.
2. Il valore del contrasto deve essere compreso tra -50 e 100.

Consultare la documentazione di [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) per ulteriori dettagli.

## Conclusione

In questo articolo abbiamo ottenuto una panoramica rapida del layer di regolazione luminosità/contrasto e appreso come regolare luminosità e contrasto dell'immagine utilizzando il metodo di fabbrica.

Consultare la nostra serie di [articoli sulle API dei layer di regolazione](/psd/it/java/layer-types/adjustment-layer/) di Aspose.PSD for Java per saperne di più.

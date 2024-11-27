---
title: Livello di regolazione invertito
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/invert/
---

# Lavorare con il livello di regolazione invertito di Photoshop in Java

In questo articolo vedremo come trasformare un'immagine di un documento Photoshop in negativo in modo programmato in Java. A tal scopo, utilizzeremo la libreria per la manipolazione del formato di file PSD chiamata Aspose.PSD per Java.

L'API di inversione del colore consente di **aggiungere un effetto negativo a un'immagine**. Forse già hai visto come [invertere i colori dell'immagine utilizzando il livello di regolazione tramite Curve](/psd/it/java/layer-types/adjustment-layer/curves/). Tuttavia, oggi considereremo un modo più veloce e facile per fare il lavoro con il livello di regolazione invertito.

## Panoramica dell'API

**L'API del livello di regolazione invertito** è composta dalla classe del livello stesso che è [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Questa classe non ha membri pubblici propri, poiché eredita tutti i membri pubblici dalla classe genitore ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Questo semplifica il suo utilizzo perché tutto ciò che devi fare è aggiungerlo a un file PSD e l'immagine diventa negativa.

## Invertire i colori dell'immagine

Quindi, anche se sembra ovvio, dimostriamo per chiarezza come **applicare un livello di regolazione invertito all'immagine** di un astronauta (a) per ottenere l'effetto negativo per quell'immagine (b).

![Esempio di livello di regolazione invertito prima e dopo](invert-adjustment-layer-figure-1.png)

Per **invertire i colori dell'immagine**, aggiungi semplicemente un livello di regolazione invertito al PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

E questo è tutto! Non ci sono proprietà specifiche da configurare per questo tipo di livello di regolazione.

## Conclusione

In questo articolo abbiamo appreso riguardo all'API del livello di regolazione invertito di Aspose.PSD per Java. È uno strumento semplice per ottenere immagini negative perché l'API di questo livello di regolazione non dichiara alcun membro pubblico.

---
title: Strato di regolazione dell'esposizione
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/exposure/
---

# Lavorare con lo strato di regolazione dell'esposizione di Photoshop in Java

In questo articolo aggiungeremo uno strato di regolazione dell'esposizione a un documento di Adobe® Photoshop® utilizzando Aspose.PSD per Java, una libreria di manipolazione del formato file PSD. La libreria funziona senza bisogno di un editor Photoshop installato poiché utilizza i propri algoritmi di elaborazione delle immagini. Abbiamo anche appreso alcuni dettagli relativi all'API di regolazione dell'esposizione della libreria.

## Panoramica dell'API

Lo strato di regolazione dell'esposizione è configurato attraverso la classe [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) che contiene le seguenti proprietà per lavorare con la regolazione dell'esposizione:

- Definisce quanto luce ha la foto comprimendo o allargando l'intero istogramma rispetto ai neri. Quindi, influisce principalmente sui punti luminosi.
- A differenza dell'esposizione, l'offset dell'esposizione influenza principalmente le ombre.
- Correzione gamma. Corregge la luminanza dell'immagine.

## Regolazione corretta dell'esposizione

Correggere l'esposizione e le proprietà correlate è semplice come modificare alcune proprietà della classe. Applichiamo quindi una regolazione dell'esposizione (a) a una foto sottoesposta di una biblioteca (b) per renderla percepibile all'occhio umano (c).

![Esempio di strato di regolazione dell'esposizione](exposure-adjustment-layer-figure-1.png)

L'intera regolazione è principalmente fatta utilizzando la correzione gamma. Tuttavia, l'esposizione e l'offset vengono regolati leggermente. Tutto ciò che devi fare è impostare valori appropriati alle proprietà già menzionate:

```java
ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
exposureLayer.setExposure(-0.03f);
exposureLayer.setOffset(-0.0005f);
exposureLayer.setGammaCorrection(1.85f);
```

Presta attenzione che l'esposizione deve essere compresa tra -20.0 e 20.0, il valore dell'offset deve essere compreso tra -0.5 e 0.5 e il valore della correzione gamma deve essere compreso tra 9,99 e 0,01.

Consulta il [riferimento API dello strato di regolazione dell'esposizione](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) per ulteriori dettagli.

## Conclusione

In questo articolo abbiamo imparato come aggiungere uno strato di regolazione dell'esposizione a un file PSD per illuminare l'immagine e abbiamo considerato alcuni dettagli dell'API.

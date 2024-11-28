---
title: Livello di aggiustamento delle curve
type: docs
weight: 30
url: /it/java/layer-types/adjustment-layer/curves/
---

# Lavorare con il livello di aggiustamento delle curve di Photoshop in Java

Lo scopo di questo articolo è dimostrare le capacità della libreria Aspose.PSD per Java mentre si lavora con i **livelli di aggiustamento delle curve** nei documenti di Adobe® Photoshop®. La libreria è completamente autonoma. Pertanto, funziona senza installare l'editor fotografico Photoshop. L'elenco completo delle funzionalità si può trovare nella nostra base di conoscenza. Ora, torniamo alle curve.

## Panoramica dell'API

Lo strumento Curve può essere rappresentato come una linea diagonale (curva) su un grafico con luci nell'angolo in alto a destra e ombre nell'angolo in basso a destra.

La libreria fornisce un'API per lavorare con la curva, ovvero la classe [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Tuttavia, questa classe ha **due approcci completamente diversi** per lavorare con la curva. Pertanto, può essere modificata in uno dei due modi contemporaneamente:

- Continuo (la curva rappresentata come un percorso con punti nei punti di flessione)
- Discreto (la curva rappresentata come una linea tratteggiata)

Quindi, la libreria offre due modi per modificare la curva utilizzando rispettivamente il [gestore continuo](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) e il [gestore discreto](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager). Successivamente, spiegheremo come utilizzare ciascuno di essi su un esempio specifico.

## Regolare colore e tono utilizzando il Gestore Continuo delle Curve

Il [Gestore Continuo delle Curve](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **configura i punti di flessione di una curva continua** per il canale composito (RGB) così come per ciascun canale del colore particolare. A scopo dimostrativo, verrà applicato un aggiustamento delle curve (a) a un'immagine oscurata di un'orchestra (b) per ottenere un'immagine schiarita con colori più caldi (c):

![Figura 1 del Livello di Aggiustamento delle Curve](curves-psd-adjustment-layer-figure-1.png)

Dato che ci sono due gestori, è necessario selezionare esplicitamente uno (il gestore continuo in questo caso) prima di ottenerlo. Successivamente, possiamo aggiungere direttamente i punti della curva in determinate coordinate per i canali dei colori desiderati (composito RGB, rosso e blu rispettivamente) per ricreare la forma della curva:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

L'origine delle coordinate si trova nell'angolo in basso a sinistra. Il valore massimo della coordinata di un punto è limitato al tipo di dati (byte) ed è pari a 255 (127 per il tipo firmato).

Ci sono anche alcuni [metodi aggiuntivi](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) che è possibile utilizzare.

## Regolare il tono utilizzando il Gestore Discreto delle Curve

Il Gestore Discreto delle Curve consente anche di posizionare i punti della curva (cambiare effettivamente colore e tono), ma la differenza è che lo fanno in modo diverso. In primo luogo, la **curva è composta da punti** o punti (non una linea solida). In secondo luogo, questo gestore **non posiziona un punto in nessun punto** sul grafico. Invece, **sposta il punto verso l'alto o verso il basso** con un intervallo di valori compreso tra 255 e 0 rispettivamente. Per impostazione predefinita, i valori dei punti della curva aumentano incrementalmente per modellare una curva che è inclinata di 45 gradi.

Quindi, tenendo presente ciò, è facile ricreare il preset di Photoshop "Negativo (RBG)" (a) e applicarlo a un'immagine in scala di grigi di una valle (b) per ottenere alla fine una rappresentazione negativa della valle (c).

![Figura 2 del Livello di Aggiustamento delle Curve](curves-psd-adjustment-layer-figure-2.png) Prima di tutto, non dimenticare di selezionare il gestore corrispondente per poterlo utilizzare e quindi impostare i valori dei punti della curva in ordine decrescente partendo da 255 fino a 0 per ciascun punto della curva (255 in totale):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Il gestore fornisce anche alcuni [altri metodi](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) per gestire la curva.

## Conclusione

In questo articolo abbiamo imparato come lavorare con i livelli di aggiustamento delle curve nei documenti di Photoshop utilizzando Aspose.PSD per Java in due modi completamente diversi (gestori continui e discreti).

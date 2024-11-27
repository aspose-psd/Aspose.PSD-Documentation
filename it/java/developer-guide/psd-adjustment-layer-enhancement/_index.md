---
title: Utilizzo del livello di regolazione per miglioramenti PSD
weight: 100
type: docs
description: Esempi di utilizzo del livello di regolazione tramite Aspose.PSD per Java
keywords: [livello di regolazione, miglioramento foto, regolazione curve, miglioramento livelli, inverti, filtro foto, api psd, java, esempio di codice]
url: it/java/adjustment-layer-enhancement/
---

## **Panoramica**

Questo articolo esplora la modifica dei livelli di regolazione in Aspose.PSD per Java. I livelli di regolazione sono una potente funzionalità nella modifica delle immagini che ti permettono di apportare modifiche non distruttive alle tue immagini. Aspose.PSD fornisce un set completo di classi di livelli di regolazione che puoi utilizzare per modificare vari aspetti delle tue immagini.

Per dimostrare la modifica dei livelli di regolazione, forniremo un frammento di codice di esempio alla fine della pagina che carica un'immagine PSD e applica diverse regolazioni ai suoi livelli.

Nel frammento di codice seguente, iniziamo caricando l'immagine PSD utilizzando il metodo PsdImage.load(). Quindi, configuriamo le opzioni per salvare i file PNG di output. La classe PngOptions ci consente di specificare il tipo di colore per l'immagine di output.

Successivamente, iteriamo attraverso ogni livello nell'immagine PSD e controlliamo il suo tipo utilizzando il metodo isAssignable(). Se il livello è di un tipo specifico, lo convertiamo a quel tipo utilizzando il metodo cast() e applichiamo la regolazione desiderata. Ad esempio, regoliamo la luminosità e il contrasto di un BrightnessContrastLayer, modifichiamo i livelli di un LevelsLayer, aggiungiamo un punto curva a un CurvesLayer, e così via.

Puoi aggiungere del codice aggiuntivo per applicare altre regolazioni ai rispettivi livelli. Aspose.PSD fornisce un'ampia gamma di classi di livelli di regolazione, come [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) e altro ancora.

Infine, salviamo l'immagine modificata utilizzando il metodo save() della classe PsdImage.

Questo fornisce una panoramica di base su come modificare i livelli di regolazione in Aspose.PSD per Java. Puoi personalizzare le regolazioni in base alle tue esigenze ed esplorare le varie opzioni disponibili nella documentazione dell'API.

Si prega di controllare l'esempio completo qui sotto.

## **Esempio**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentazione-Java-Aspose-adjustment-layer-enhancement.java" >}}

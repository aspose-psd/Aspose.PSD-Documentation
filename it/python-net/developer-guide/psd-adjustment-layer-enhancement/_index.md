---
title: Utilizzo del livello di regolazione per miglioramenti PSD
weight: 100
type: docs
description: Esempi sull'utilizzo del livello di regolazione tramite Aspose.PSD per Python
keywords: [livello di regolazione, miglioramento delle foto, regolazione delle curve, miglioramento dei livelli, inverti, filtro fotografico, API psd, python, esempio di codice]
url: it/python-net/miglioramento-del-livello-di-regolazione/
---

## **Panoramica**

In questo articolo esploreremo la modifica dei livelli di regolazione in Aspose.PSD per Python. I livelli di regolazione sono una potente funzionalità nell'editing delle immagini che ti permette di apportare modifiche non distruttive alle tue immagini. Aspose.PSD fornisce un set completo di classi di livelli di regolazione che puoi utilizzare per modificare vari aspetti delle tue immagini.

Per dimostrare la modifica dei livelli di regolazione, utilizzeremo un frammento di codice di esempio alla fine della pagina che carica un'immagine PSD e applica diverse regolazioni ai suoi livelli.

Nel frammento di codice sottostante, iniziamo caricando l'immagine PSD utilizzando il metodo PsdImage.load(). Impostiamo quindi le opzioni per salvare i file PNG in output. La classe PngOptions ci consente di specificare il tipo di colore per l'immagine in uscita.

Successivamente, iteriamo attraverso ciascun livello nell'immagine PSD e controlliamo il suo tipo utilizzando il metodo is_assignable(). Se il livello è di un determinato tipo, lo convertiamo a quel tipo utilizzando il metodo cast() e applichiamo la regolazione desiderata. Ad esempio, regoliamo la luminosità e il contrasto di un livello BrightnessContrastLayer, modifichiamo i livelli di un livello LevelsLayer, aggiungiamo un punto curva a un livello CurvesLayer, e così via.

Puoi aggiungere del codice aggiuntivo per applicare altre regolazioni ai rispettivi livelli. Aspose.PSD fornisce una vasta gamma di classi di livelli di regolazione, come [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), e altro ancora.

Infine, salviamo l'immagine modificata utilizzando il metodo save() della classe PsdImage.

Questo codice fornisce una panoramica di base su come modificare i livelli di regolazione in Aspose.PSD per Python. Puoi personalizzare le regolazioni in base alle tue esigenze ed esplorare le varie opzioni disponibili nella documentazione dell'API.

Si prega di controllare l'esempio completo.

## **Esempio**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentazione-Python-Aspose-miglioramento-del-livello-di-regolazione.py" >}}

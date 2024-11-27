---
title: Utilizzo del livello di regolazione per migliorare le PSD
weight: 100
type: docs
description: Esempi sull'utilizzo dei livelli di regolazione tramite Aspose.PSD per C#
keywords: [livello di regolazione, miglioramento foto, regolazione curve, miglioramento livelli, invertire, filtro fotografico, API psd, C#, csharp, esempio di codice]
url: it/adjustment-layer-enhancement/
---

## Panoramica

In questo articolo, esploreremo la modifica dei livelli di regolazione in Aspose.PSD per C#. I livelli di regolazione sono una funzionalità potente nella modifica delle immagini che ti permette di apportare modifiche non distruttive alle tue immagini. Aspose.PSD fornisce un set completo di classi di livello di regolazione che puoi utilizzare per modificare vari aspetti delle tue immagini.

Per dimostrare la modifica dei livelli di regolazione, useremo un frammento di codice di esempio alla fine della pagina che carica un'immagine PSD e applica diverse regolazioni ai suoi livelli.

Nel frammento di codice sottostante, iniziamo caricando l'immagine PSD utilizzando il metodo `PsdImage.Load()`. Impostiamo poi le opzioni per salvare i file PNG di output. La classe `PngOptions` ci permette di specificare il tipo di colore per l'immagine di output.

Successivamente, iteriamo attraverso ciascun livello nell'immagine PSD e controlliamo il suo tipo utilizzando il metodo `IsAssignable()`. Se il livello è di un tipo specifico, lo convertiamo a quel tipo utilizzando il metodo `Cast()` e applichiamo la regolazione desiderata. Ad esempio, regoliamo la luminosità e il contrasto di un `BrightnessContrastLayer`, modifichiamo i livelli di un `LevelsLayer`, aggiungiamo un punto curva a un `CurvesLayer`, ecc.

Puoi aggiungere codice aggiuntivo per applicare altre regolazioni ai rispettivi livelli. Aspose.PSD fornisce una vasta gamma di classi di livello di regolazione, come [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), e altro ancora.

Infine, salviamo l'immagine modificata utilizzando il metodo `Save()` della classe `PsdImage`.

Questo codice fornisce una panoramica di base su come modificare i livelli di regolazione in Aspose.PSD per C#. Puoi personalizzare le regolazioni in base alle tue esigenze ed esplorare le varie opzioni disponibili nella documentazione dell'API.

## Esempio

Ecco un esempio di codice che dimostra come utilizzare i livelli di regolazione tramite Aspose.PSD per C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Per ulteriori informazioni dettagliate ed esempi, visita la [documentazione di Aspose.PSD per C#](https://docs.aspose.com/psd/net/).


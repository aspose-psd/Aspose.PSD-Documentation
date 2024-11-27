---
title: Note sulla versione di Aspose.PSD per .NET 22.6
type: docs
weight: 70
url: /it/net/aspose-psd-for-net-22-6-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-940|Creare API per ottenere l'hash univoco per livelli simili in file diversi|Potenziamento|
|PSDNET-678|Rendering incorretto di FillLayer con pattern nel caso in cui i pattern siano più di uno e l'ordine dei livelli è cambiato|Errore|
|PSDNET-1125|Eccezione nel carico di un file PSD specifico con modalità di colore CMYK|Errore|


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **API rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-678. Rendering incorretto di FillLayer con pattern nel caso in cui i pattern siano più di uno e l'ordine dei livelli è cambiato**

{{< highlight csharp >}}
string sourceFile = "cattivoPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Creare API per ottenere l'hash univoco per livelli simili in diversi file**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
	// Resto del codice dell'esempio di utilizzo...
}
{{< /highlight >}}

**PSDNET-1125. Eccezione nel carico di un file PSD specifico con modalità di colore CMYK**

{{< highlight csharp >}}
string sourceFile = "02_canali-alfa.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
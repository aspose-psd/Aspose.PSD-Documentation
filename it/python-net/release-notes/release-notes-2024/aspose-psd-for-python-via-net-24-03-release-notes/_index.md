---
title: Note sulla versione di Aspose.PSD per Python via .NET 24.3
type: docs
weight: 10
url: /it/net/aspose-psd-per-python-tramite-dot-net-24-3-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per Python via .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                                          | **Categoria**|
|:------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [Formato AI] Riduzione del tempo di caricamento di immagini AI multipagina di grandi dimensioni | Miglioramento |
| PSDPYTHON-45 | Il file PSD dopo la conversione da 8 bit a 16 bit è diventato illeggibile |     Bug     |
| PSDPYTHON-46 | Il file PSD dopo la conversione da 8 bit a 32 bit è diventato illeggibile |     Bug     |
| PSDPYTHON-47 | [Formato AI] Risoluzione del rendering di curve brevi nel file AI     |     Bug     |



## **Modifiche all'API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna


## **Esempi d'uso:**

**PSDPYTHON-42. [Formato AI] Riduzione del tempo di caricamento di immagini AI multipagina di grandi dimensioni**

{{< highlight python >}}
   # Nessun esempio
{{< /highlight >}}

**PSDPYTHON-45. Il file PSD dopo la conversione da 8 bit a 16 bit è diventato illeggibile**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # è corretto
                pass
            else:
                raise Exception("Risorsa globale errata, la prima risorsa dovrebbe essere Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. Il file PSD dopo la conversione da 8 bit a 32 bit è diventato illeggibile**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # è corretto
                pass
            else:
                raise Exception("Risorsa globale errata, la prima risorsa dovrebbe essere Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [Formato AI] Risoluzione del rendering di curve brevi nel file AI**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

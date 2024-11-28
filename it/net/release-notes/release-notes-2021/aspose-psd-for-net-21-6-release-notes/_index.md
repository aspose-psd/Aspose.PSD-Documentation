---
title: Note sulla versione di Aspose.PSD per .NET 21.6
type: docs
weight: 70
url: /it/net/aspose-psd-per-net-21-6-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-546|Il mascheramento del ritaglio per un gruppo non viene reso correttamente|Errore|
|PSDNET-547|La maschera regolare o vettoriale per un gruppo di livelli viene ignorata durante il rendering|Errore|
|PSDNET-647|L'immagine PSD con maschere di livello vettoriali disabilitate durante il salvataggio abilita le maschere vettoriali|Errore|
|PSDNET-786|Eccezione durante la creazione di un TextLayer con testo più lungo di 255 caratteri|Errore|
|PSDNET-900|Il testo del livello di testo non può essere reso su Linux|Miglioramento|

## **Modifiche all'API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-546. Il mascheramento del ritaglio per un gruppo non viene reso correttamente**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. La maschera regolare o vettoriale per un gruppo di livelli viene ignorata durante il rendering**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. L'immagine PSD con maschere di livello vettoriali disabilitate durante il salvataggio abilita le maschere vettoriali**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Eccezione durante la creazione di un TextLayer con testo più lungo di 255 caratteri**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

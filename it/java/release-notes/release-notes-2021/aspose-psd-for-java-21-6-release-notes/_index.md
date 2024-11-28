---
title: Note sulla versione di Aspose.PSD per Java 21.6
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-21-6-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Chiave**|**Riepilogo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-351|Il mascheramento di ritaglio per un gruppo non viene reso correttamente|Bug|
|PSDJAVA-352|La maschera regolare o vettoriale per un gruppo di livelli viene ignorata durante il rendering|Bug|
|PSDJAVA-353|L'immagine PSD con maschere di livello vettoriali disabilitate durante il salvataggio abilita le maschere vettoriali|Bug|
|PSDJAVA-354|Eccezione durante la creazione di un TextLayer con un testo più lungo di 255 caratteri|Bug|

# **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- Nessuna

# **API rimosse:**
- Nessuna

# **Esempi d'uso:**

**PSDJAVA-351. Il mascheramento di ritaglio per un gruppo non viene reso correttamente**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. La maschera regolare o vettoriale per un gruppo di livelli viene ignorata durante il rendering**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. L'immagine PSD con maschere di livello vettoriali disabilitate durante il salvataggio abilita le maschere vettoriali**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Eccezione durante la creazione di un TextLayer con un testo più lungo di 255 caratteri**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

---
title: Note sulla versione Aspose.PSD per Java 23.9
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-23-9-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Chiave**   | **Sommario**                                                                                                                      | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implementazione della creazione di maschere per nuovi livelli di regolazione                                                             | Funzionalità |
| PSDJAVA-528 | Aggiunta del supporto per i livelli Clipped Layers come opzione di sfumatura di gruppo                                                  | Funzionalità |
| PSDJAVA-529 | I file PSD con modalità colore a 16 bit non applicano la maschera ai livelli di regolazione                                              | Bug          |
| PSDJAVA-530 | Rappresentazione errata delle parentesi nel livello di testo                                                                         | Bug          |
| PSDJAVA-531 | Impossibile aggiornare gli stili nei livelli di testo                                                                                | Bug          |
| PSDJAVA-532 | Dopo l'esportazione di un file PSD con CMYK, i colori nel PSD esportato vengono alterati                                                | Bug          |
| PSDJAVA-533 | Un file PSB specifico genera un'eccezione "Il rettangolo non ha un'area di elaborazione comune"                                         | Bug          |
| PSDJAVA-534 | Caricamento dell'immagine fallito. OverflowException: Operazione aritmetica risultata in un overflow                                    | Bug          |

## **Modifiche all'API pubblica**
# **API aggiunte:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **API rimosse:**

- Nessuna

## **Esempi di utilizzo:**

**PSDJAVA-527. Implementazione della creazione di maschere per nuovi livelli di regolazione**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Aggiunta del supporto per i livelli Clipped Layers come opzione di sfumatura di gruppo**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

*(Continua...)*

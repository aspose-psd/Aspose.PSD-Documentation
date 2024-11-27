---
title: Note sulla versione Aspose.PSD per Java 23.8
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-23-8-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione per [Aspose.PSD per Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Chiave**  | **Sommario**                                                                                                                                      | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Aggiunta un nuovo tipo di deformazione (Flag)                                                                                                      |    Funzionalità   |
| PSDJAVA-519 | Aggiunti nuovi tipi di deformazione: arco su, arco giù, sfera                                                                                       |    Funzionalità   |
| PSDJAVA-520 | Implementato il nuovo metodo PsdImage.AddPosterizeAdjustmentLayer per aggiungere il nuovo livello di Posterize                                        |    Funzionalità   |
| PSDJAVA-521 | Informazioni PSD perse aprendo e salvando l'immagine                                                                                               |      Bug     |
| PSDJAVA-522 | Caricamento immagine fallito                                                                                                                      |      Bug     |
| PSDJAVA-523 | Caricamento immagine fallito: Impossibile eseguire il cast dell'oggetto di tipo UnknownStructure in tipo DescriptorStructure                       |      Bug     |
| PSDJAVA-524 | Modificare il file nella libreria di terze parti corrompe il file PSD ma può essere aperto in Photoshop                                           |      Bug     |

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **API Rimosse:**

- Nessuna

## **Esempi di utilizzo:**

**PSDJAVA-518. Aggiungi un nuovo tipo di deformazione (Flag)**

{{< highlight java >}}
    String fileSorgente = "src/main/resources/flag_warp.psd";
    String fileOutput = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgente, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(fileOutput, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Aggiungi nuovi tipi di deformazione: arco su, arco giù, sfera**

{{< highlight java >}}
    String fileSorgenteArcoSuperiore = "src/main/resources/arc_upper_warp.psd";
    String fileSorgenteArcoInferiore = "src/main/resources/arc_lower_warp.psd";
    String fileSorgenteBulge = "src/main/resources/bulge_warp.psd";

    String fileOutputArcoSuperiore = "src/main/resources/ArcUpper_export.png";
    String fileOutputArcoInferiore = "src/main/resources/ArcLower_export.png";
    String fileOutputBulge = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgenteArcoSuperiore, psdLoadOptions)) {
        psdImage.save(fileOutputArcoSuperiore, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgenteArcoInferiore, psdLoadOptions)) {
        psdImage.save(fileOutputArcoInferiore, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgenteBulge, psdLoadOptions)) {
        psdImage.save(fileOutputBulge, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementa il nuovo metodo PsdImage.AddPosterizeAdjustmentLayer per aggiungere il nuovo livello Posterize**

{{< highlight java >}}
public static void main(String[] args) {
    String fileSrc = "src/main/resources/zendeya.psd";
    String fileOut = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(fileSrc)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(fileOut);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Verifica le modifiche salvate
    try (PsdImage image = (PsdImage) Image.load(fileOut, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object atteso, Object attuale) {
    assertAreEqual(atteso, attuale, "Gli oggetti non sono uguali.");
}

static void assertAreEqual(Object atteso, Object attuale, String messaggio) {
    if (!atteso.equals(attuale)) {
        throw new IllegalArgumentException(messaggio);
    }
}
{{< /highlight >}}

**PSDJAVA-521. Informazioni PSD perse aprendo e salvando**

{{< highlight java >}}
    String sorgente = "src/main/resources/Original file.psd";
    String outputPsd = "src/main/resources/out_Original file.psd";
    String outputPng = "src/main/resources/out_Original file.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sorgente)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Caricamento immagine fallito**

{{< highlight java >}}
    String fileSorgente1 = "src/main/resources/test_text.psd";
    String fileSorgente2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgente1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(fileSorgente2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Caricamento immagine fallito: Impossibile eseguire il cast dell'oggetto di tipo UnknownStructure in tipo DescriptorStructure**

{{< highlight java >}}
   try (PsdImage newPsd = new PsdImage(10, 10)) {
        newPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            newPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // Dovrebbe caricarsi correttamente
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Modificare il file nella libreria di terze parti corrompe il file PSD ma può essere aperto in Photoshop**

{{< highlight java >}}
    String fileSorgente = "src/main/resources/output.psd";
    String fileOutput = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(fileSorgente, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(fileOutput, pngOptions);
    }
{{< /highlight >}}

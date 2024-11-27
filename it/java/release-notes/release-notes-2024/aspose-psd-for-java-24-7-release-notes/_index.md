---
title: Note sulla release di Aspose.PSD per Java 24.7
type: docs
weight: 40
url: /it/java/aspose-psd-for-java-24-7-note-sulla-release/
---

{{% avviso color="primary" %}} Questa pagina contiene le note sulla release per [Aspose.PSD per Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /avviso %}}

| **Chiave**  | **Sommario**                                                                                     | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Eccezione "Caricamento immagine non riuscito" durante l'apertura di un documento AI             | Bug          |
| PSDJAVA-636 | Testo renderizzato in modo errato nei file PDF di output                                         | Bug          |
| PSDJAVA-637 | Risoluzione del problema ImageSaveException: l'esportazione dell'immagine non riesce per il file specificato su Linux | Bug          |
| PSDJAVA-638 | Risoluzione del caricamento dei font quando si utilizza Aspose.Drawing                            | Bug          |
| PSDJAVA-639 | 'L'operazione aritmetica ha prodotto un overflow' durante la creazione di un livello di oggetto intelligente utilizzando un grande JPEG | Bug          |
| PSDJAVA-640 | Il file AI non può essere convertito in un file JPG                                               | Bug          |

## **Modifiche delle API pubbliche**
# **API Aggiunte:**

- Nessuna

# **API Rimosse:**

- Nessuna

## **Esempi di utilizzo:**

**PSDJAVA-635. Eccezione "Caricamento immagine non riuscito" durante l'apertura di un documento AI**

{{< highlight java >}}

    String fileSorgente = "src/main/resources/[SA]_ID_card_template.ai";
    String fileOutput = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage immagine = (AiImage) Image.load(fileSorgente)) {
        immagine.save(fileOutput, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Testo renderizzato in modo errato nei file PDF di output**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage immaginePsd = (PsdImage) Image.load(src)) {
        PdfOptions opzioniSalvataggio = new PdfOptions();
        opzioniSalvataggio.setPdfCoreOptions(new PdfCoreOptions());

        immaginePsd.save(output, opzioniSalvataggio);
    }

{{< /highlight >}}

**PSDJAVA-637. Risoluzione del problema ImageSaveException: l'esportazione dell'immagine non riesce per il file specificato su Linux**

{{< highlight java >}}

    String fileSorgente = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String fileOutput = "src/main/resources/output.jpg";

    PsdLoadOptions opzioniCaricamentoPsd = new PsdLoadOptions();
    opzioniCaricamentoPsd.setLoadEffectsResource(true);

    try (var immaginePsd = (PsdImage) Image.load(fileSorgente, opzioniCaricamentoPsd)) {
        JpegOptions opzioniSalvataggio = new JpegOptions();
        opzioniSalvataggio.setQuality(70);
        immaginePsd.save(fileOutput, opzioniSalvataggio);
    }

{{< /highlight >}}

**PSDJAVA-638. Risoluzione del caricamento dei font quando si utilizza Aspose.Drawing**

{{< highlight java >}}

    final var collezioneFontInstallati = new InstalledFontCollection();
    try {
        System.out.println("- Prima dell'aggiornamento. Numero di font installati: " + collezioneFontInstallati.getFamilies().length);
        System.out.println("- Piattaforma: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Aggiorna la cache dei font cercando di ottenere il nome del font Adobe per 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Dopo l'aggiornamento. Numero di font installati: " + collezioneFontInstallati.getFamilies().length);

        assertAreEqual(collezioneFontInstallati.getFamilies().length, 1);
    } finally {
        collezioneFontInstallati.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'L'operazione aritmetica ha prodotto un overflow' durante la creazione di un livello di oggetto intelligente utilizzando un grande JPEG**

{{< highlight java >}}

    String fileSorgente = "src/main/resources/source.psd";
    String immagineJpg = "src/main/resources/test.jpg";

    PsdLoadOptions opzioniCaricamentoPsd = new PsdLoadOptions();
    opzioniCaricamentoPsd.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var immagine = (PsdImage) Image.load(fileSorgente, opzioniCaricamentoPsd)) {
        final FileStream stream = new FileStream(immagineJpg, FileMode.Open);
        try {
            var livelloAggiunto = new SmartObjectLayer(stream);
            livelloAggiunto.setName("Livello di prova");
            immagine.addLayer(livelloAggiunto);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. Il file AI non può essere convertito in un file JPG**

{{< highlight java >}}

    String fileSorgente = "src/main/resources/aaa.ai";
    String fileOutput = "src/main/resources/aaa.png";

    try (AiImage immagine = (AiImage) Image.load(fileSorgente)) {
        immagine.save(fileOutput, new PngOptions());
    }

{{< /highlight >}}

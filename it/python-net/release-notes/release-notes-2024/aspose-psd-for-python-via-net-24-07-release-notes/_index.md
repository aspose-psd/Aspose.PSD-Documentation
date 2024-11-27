---
title: Note sulla release di Aspose.PSD per Python via .NET 24.7
type: docs
weight: 10
url: /it/python-net/aspose-psd-per-python-via-net-24-7-note-sulla-release/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla release per [Aspose.PSD per Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**   | **Sommario**                                                                                                     | **Categoria** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Eccezione "Caricamento dell'immagine non riuscito." durante l'apertura di un documento AI                        | Bug      |
| PSDPYTHON-87 | Texto reso in modo incorretto nei file PDF di output                                                            | Bug      |
| PSDPYTHON-88 | Risolto ImageSaveException: esportazione dell'immagine fallita per il file specificato su Linux                 | Bug      |
| PSDPYTHON-89 | Risolto il caricamento dei font quando si utilizza Aspose.Drawing                                              | Bug      |
| PSDPYTHON-90 | 'L'operazione aritmetica ha prodotto un overflow' durante la creazione di uno smart object layer usando un JPEG grande | Bug      |
| PSDPYTHON-91 | Il file AI non può essere convertito in un file JPG                                                           | Bug      |

## **Modifiche all'API pubblica**
# **API Aggiunte:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDPYTHON-86. Eccezione "Caricamento dell'immagine non riuscito." durante l'apertura di un documento AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Testo reso in modo incorretto nei file PDF di output**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Risolto ImageSaveException: esportazione dell'immagine fallita per il file specificato su Linux**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        outputFile = self.GetFileInOutputFolder("output.jpg")

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        saveOpt = JpegOptions()
        saveOpt.quality = 70
        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputFile, saveOpt)
{{< /highlight >}}


**PSDPYTHON-89. Risolto il caricamento dei font quando si utilizza Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Prima dell'aggiornamento. Conteggio dei font installati: " + str(len(installedFonts.families)))
            print("- Aggiorna la cache dei font cercando di ottenere il nome del font Adobe per 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Dopo l'aggiornamento. Conteggio dei font installati: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'L'operazione aritmetica ha prodotto un overflow' durante la creazione di uno smart object layer usando un JPEG grande**
{{< highlight python >}}
        # La correzione è stata apportata, ma c'è un altro problema in Aspose.PSD per Python che limita questo test
        #srcFile = self.GetFileInBaseFolder("source.psd")
        #imageJpg = self.GetFileInBaseFolder("test.jpg")

        #loadOpt = PsdLoadOptions()
        #loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(srcFile, loadOpt) as image:
            #with open(imageJpg, "rb", buffering=0) as stream:
                #addedLayer = SmartObjectLayer(stream)
                #addedLayer.Name = "Test Layer"
                #image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Il file AI non può essere convertito in un file JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

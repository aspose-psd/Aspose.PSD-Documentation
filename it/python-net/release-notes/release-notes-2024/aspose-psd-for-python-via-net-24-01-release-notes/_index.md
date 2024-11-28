---
title: Note sulla versione di Aspose.PSD per Python via .NET 24.1
type: docs
weight: 10
url: /it/net/aspose-psd-per-python-via-net-24-1-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD per Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                             | **Categoria** |
|:-------------|:---------------------------------------------------------------------------------------------------------|:-------------|
|  PSDPYTHON-19| [Formato AI] Aggiunta gestione di base per immagini AI multipagina                                         | Feature      |
|  PSDPYTHON-22| L'effetto di testo deformabile non si applica al testo                                                     | Bug          |
|  PSDPYTHON-23| Rendering non corretto della maschera in un file specifico                                                 | Bug          |
|  PSDPYTHON-24| NullReferenceException in Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor           | Bug          |
|  PSDPYTHON-25| [Formato AI] Risoluzione del consumo di memoria in AiExporterUtils                                         | Bug          |


## Modifiche all'API pubblica
# API Aggiunte:
- P: Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# API Rimosse:
- Nessuna


## Esempi di utilizzo:

**PSDPYTHON-19. [Formato AI] Aggiunta gestione di base per immagini AI multipagina**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Carica l'immagine AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Per impostazione predefinita, ActivePageIndex è 0.
            # Quindi se si salva l'immagine AI senza cambiare questa proprietà, la prima pagina verrà renderizzata e salvata.
            image.save(firstPageOutputPng, PngOptions())

            # Cambia l'indice della pagina attiva alla seconda pagina.
            image.active_page_index = 1

            # Salva la seconda pagina dell'immagine AI come immagine PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Cambia l'indice della pagina attiva alla terza pagina.
            image.active_page_index = 2

            # Salva la terza pagina dell'immagine AI come immagine PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. L'effetto di testo deformabile non si applica al testo**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Rendering non corretto della maschera in un file specifico**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException in Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Formato AI] Risoluzione del consumo di memoria in AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Il consumo di memoria per C# è di 220, ma per Python non abbiamo accesso diretto alle attività di GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Carica l'immagine AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Salva la prima pagina dell'immagine AI come immagine PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Cambia l'indice della pagina attiva alla seconda pagina.
            image.active_page_index = 1

            # Salva la seconda pagina dell'immagine AI come immagine PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Cambia l'indice della pagina attiva alla terza pagina.
            image.active_page_index = 2

            # Salva la terza pagina dell'immagine AI come immagine PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("L'utilizzo della memoria è troppo elevato. {} anziché {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

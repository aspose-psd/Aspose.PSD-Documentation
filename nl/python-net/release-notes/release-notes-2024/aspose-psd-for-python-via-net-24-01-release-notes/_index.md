---
title: Aspose.PSD voor Python via .NET 24.1 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-python-via-net-24-1-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                                          | **Categorie** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:-------------|
|  PSDPYTHON-19 | [AI-indeling] Basisverwerking toevoegen voor multipage AI-afbeeldingen                                      |   Functie    |
|  PSDPYTHON-22 | Warp Teksteffect wordt niet toegepast op tekst                                                             |     Fout     |
|  PSDPYTHON-23 | Onjuiste weergave van masker in het specifieke bestand                                                     |     Fout     |
|  PSDPYTHON-24 | NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor          |     Fout     |
|  PSDPYTHON-25 | [AI-indeling] Geheugengebruik repareren in AiExporterUtils                                                 |     Fout     |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDPYTHON-19. [AI-indeling] Basisverwerking toevoegen voor multipage AI-afbeeldingen**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Laad de AI-afbeelding.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Standaard is de ActivePageIndex 0.
            # Dus als u de AI-afbeelding opslaat zonder deze eigenschap te wijzigen, wordt de eerste pagina weergegeven en opgeslagen.
            image.save(firstPageOutputPng, PngOptions())

            # Wijzig de actieve pagina-index naar de tweede pagina.
            image.active_page_index = 1

            # Sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(secondPageOutputPng, PngOptions())

            # Wijzig de actieve pagina-index naar de derde pagina.
            image.active_page_index = 2

            # Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Warp Teksteffect wordt niet toegepast op tekst**

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

**PSDPYTHON-23. Onjuiste weergave van masker in het specifieke bestand**

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

**PSDPYTHON-24. NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI-indeling] Geheugengebruik repareren in AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Het geheugengebruik voor C# is 220, maar voor Python hebben we geen directe toegang tot GC-activiteiten.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Laad de AI-afbeelding.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Sla de eerste pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(firstPageOutputPng, pngOpt)

            # Wijzig de actieve pagina-index naar de tweede pagina.
            image.active_page_index = 1

            # Sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(secondPageOutputPng, pngOpt)

            # Wijzig de actieve pagina-index naar de derde pagina.
            image.active_page_index = 2

            # Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Gebruik van geheugen is te groot. {} in plaats van {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

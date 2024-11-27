---
title: Aspose.PSD für Python via .NET 24.1 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-fur-python-uber-net-24-1-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                       | **Kategorie** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI-Format] Grundlegende Behandlung für mehrseitige AI-Bilder hinzufügen                                   |   Feature   |
|  PSDPYTHON-22 | Warp-Texteffekt wird nicht auf Text angewendet                                                              |     Bug     |
|  PSDPYTHON-23 | Fehlerhafte Darstellung der Maske in der spezifischen Datei                                                 |     Bug     |
|  PSDPYTHON-24 | NullReferenceException bei Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Bug     |
|  PSDPYTHON-25 | [AI-Format] Behebung des Speicherverbrauchs in AiExporterUtils                                              |     Bug     |



## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Entfernte APIs:**
- Keine


## **Verwendungsbeispiele:**

**PSDPYTHON-19. [AI-Format] Grundlegende Behandlung für mehrseitige AI-Bilder hinzufügen**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Laden des AI-Bildes.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Standardmäßig ist der ActivePageIndex 0.
            # Wenn Sie das AI-Bild ohne Änderung dieses Eigenschaft speichern, wird die erste Seite gerendert und gespeichert.
            image.save(firstPageOutputPng, PngOptions())

            # Ändern des aktiven Seitenindex auf die zweite Seite.
            image.active_page_index = 1

            # Speichern Sie die zweite Seite des AI-Bildes als PNG-Bild.
            image.save(secondPageOutputPng, PngOptions())

            # Ändern des aktiven Seitenindex auf die dritte Seite.
            image.active_page_index = 2

            # Speichern Sie die dritte Seite des AI-Bildes als PNG-Bild.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Warp-Texteffekt wird nicht auf Text angewendet**

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

**PSDPYTHON-23. Fehlerhafte Darstellung der Maske in der spezifischen Datei**

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

**PSDPYTHON-24. NullReferenceException bei Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI-Format] Behebung des Speicherverbrauchs in AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C#-Speicherverbrauch beträgt 220, aber für Python haben wir keinen direkten Zugriff auf die GC-Aktivitäten.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Laden des AI-Bildes.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Speichern Sie die erste Seite des AI-Bildes als PNG-Bild.
            image.save(firstPageOutputPng, pngOpt)

            # Ändern des aktiven Seitenindex auf die zweite Seite.
            image.active_page_index = 1

            # Speichern Sie die zweite Seite des AI-Bildes als PNG-Bild.
            image.save(secondPageOutputPng, pngOpt)

            # Ändern des aktiven Seitenindex auf die dritte Seite.
            image.active_page_index = 2

            # Speichern Sie die dritte Seite des AI-Bildes als PNG-Bild.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Speicherüberlastung ist zu groß. {} anstatt von {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

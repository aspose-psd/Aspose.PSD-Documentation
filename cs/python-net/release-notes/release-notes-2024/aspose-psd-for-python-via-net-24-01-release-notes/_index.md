---
title: Aspose.PSD pro Python via .NET 24.1 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-pro-python-pres-dotnet-24-1-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Python via .NET 24.1](https://pypi.org/project/aspose-psd/).

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                                | **Kategorie** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI Formát] Přidání základního zpracování vícestránkových obrázků AI                                       |   Funkce    |
|  PSDPYTHON-22 | Efekt zakřivení textu se neaplikuje na text                                                               |     Chyba    |
|  PSDPYTHON-23 | Nesprávné vykreslování masky ve specifickém souboru                                                        |     Chyba    |
|  PSDPYTHON-24 | NullReferenceException u Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Chyba    |
|  PSDPYTHON-25 | [AI Formát] Oprava využití paměti v AiExporterUtils                                                        |     Chyba    |



## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Odebraná API:**
- Žádné


## **Příklady použití:**

**PSDPYTHON-19. [AI Formát] Přidání základního zpracování vícestránkových obrázků AI**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Načtěte obrázek AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Výchozí hodnota ActivePageIndex je 0.
            # Pokud tedy uložíte obrázek AI bez změny této vlastnosti, bude vykreslena a uložena první stránka.
            image.save(firstPageOutputPng, PngOptions())

            # Změňte aktivní index stránky na druhou stránku.
            image.active_page_index = 1

            # Uložte druhou stránku obrázku AI jako obrázek PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Změňte aktivní index stránky na třetí stránku.
            image.active_page_index = 2

            # Uložte třetí stránku obrázku AI jako obrázek PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Efekt zakřivení textu se neaplikuje na text**

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

**PSDPYTHON-23. Nesprávné vykreslování masky ve specifickém souboru**

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

**PSDPYTHON-24. NullReferenceException u Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI Formát] Oprava využití paměti v AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Využití paměti v C# je 220, ale pro Python nemáme přímý přístup k aktivitám GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Načtěte obrázek AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Uložte první stránku obrázku AI jako obrázek PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Změňte aktivní index stránky na druhou stránku.
            image.active_page_index = 1

            # Uložte druhou stránku obrázku AI jako obrázek PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Změňte aktivní index stránky na třetí stránku.
            image.active_page_index = 2

            # Uložte třetí stránku obrázku AI jako obrázek PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Použití paměti je příliš velké. {} místo {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

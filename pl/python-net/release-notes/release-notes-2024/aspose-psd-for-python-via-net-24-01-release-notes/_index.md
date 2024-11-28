---
title: Aspose.PSD dla Python via .NET 24.1 - Notatki wydania
type: docs
weight: 10
url: /pl/net/aspose-psd-dla-python-za-posrednictwem-net-24-1-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                           | **Kategoria** |
|:-------------|:-----------------------------------------------------------------------------------------------------------|:--------------|
|  PSDPYTHON-19 | [Format AI] Dodano podstawową obsługę obrazów AI z wieloma stronami                                          | Funkcja       |
|  PSDPYTHON-22 | Efekt deformacji tekstu nie jest stosowany do tekstu                                                         | Błąd          |
|  PSDPYTHON-23 | Niepoprawne renderowanie maski w określonym pliku                                                          | Błąd          |
|  PSDPYTHON-24 | Wyjątek NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor      | Błąd          |
|  PSDPYTHON-25 | [Format AI] Naprawa zużycia pamięci w AiExporterUtils                                                       | Błąd          |



## **Zmiany w API publicznym**
# **Dodane interfejsy API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Usunięte interfejsy API:**
- Brak


## **Przykłady użycia:**

**PSDPYTHON-19. [Format AI] Dodanie podstawowej obsługi obrazów AI z wieloma stronami**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Wczytaj obraz AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # Domyślnie ActivePageIndex wynosi 0.
            # Jeśli zapiszesz obraz AI bez zmiany tej właściwości, pierwsza strona zostanie wyrenderowana i zapisana.
            image.save(firstPageOutputPng, PngOptions())

            # Zmień indeks aktywnej strony na drugą stronę.
            image.active_page_index = 1

            # Zapisz drugą stronę obrazu AI jako obraz PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Zmień indeks aktywnej strony na trzecią stronę.
            image.active_page_index = 2

            # Zapisz trzecią stronę obrazu AI jako obraz PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Efekt deformacji tekstu nie jest stosowany do tekstu**

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

**PSDPYTHON-23. Niepoprawne renderowanie maski w określonym pliku**

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

**PSDPYTHON-24. Wyjątek NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Format AI] Naprawa zużycia pamięci w AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Zużycie pamięci w C# wynosi 220, ale dla Pythona nie mamy bezpośredniego dostępu do aktywności GC.
        LimitPamięci = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Wczytaj obraz AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Zapisz pierwszą stronę obrazu AI jako obraz PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Zmień indeks aktywnej strony na drugą stronę.
            image.active_page_index = 1

            # Zapisz drugą stronę obrazu AI jako obraz PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Zmień indeks aktywnej strony na trzecią stronę.
            image.active_page_index = 2

            # Zapisz trzecią stronę obrazu AI jako obraz PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        użytaPamięć = (endMemory - startMemory) / 1024 / 1024

        jeśli użytaPamięć > LimitPamięci:
            raise Exception("Zbyt duże zużycie pamięci. {} zamiast {:.1f}".format(użytaPamięć, LimitPamięci))
{{< /highlight >}}

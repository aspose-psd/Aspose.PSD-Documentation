---
title: Aspose.PSD за Python via .NET 24.1 - Бележки за версията
type: docs
weight: 10
url: /bg/net/aspose-psd-за-python-чрез-net-24-1-бележки-за-версията/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**     | **Резюме**                                                                                                | **Категория** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI Формат] Добавяне на основно обработване за многoстранични AI изображения                         |   Функционал   |
|  PSDPYTHON-22 | Ефектът за извиване на текста не се прилага за текста                                                     |     Проблем     |
|  PSDPYTHON-23 | Некоректно възпроизвеждане на маската в конкретния файл                                                  |     Проблем     |
|  PSDPYTHON-24 | NullReferenceException в Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor           |     Проблем     |
|  PSDPYTHON-25 | [AI Формат] Оптимизиране на използването на паметта в AiExporterUtils                                 |     Проблем     |



## **Промени в публичното API**
# **Добавени API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Премахнати API:**
- Никакви


## **Примери за използване:**

**PSDPYTHON-19. [AI Формат] Добавяне на основно обработване за многoстранични AI изображения**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Зареждане на AI изображението.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # По подразбиране, ActivePageIndex е 0.
            # Така че, ако запазите AI изображението без да променяте тази стойност, ще бъде възпроизведена и запазена първата страница.
            image.save(firstPageOutputPng, PngOptions())

            # Промяна на активния индекс на страницата на втората страница.
            image.active_page_index = 1

            # Запазване на втората страница на AI изображението като PNG изображение.
            image.save(secondPageOutputPng, PngOptions())

            # Промяна на активния индекс на страницата към третата страница.
            image.active_page_index = 2

            # Запазване на третата страница на AI изображението като PNG изображение.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Ефектът за извиване на текста не се прилага за текста**

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

**PSDPYTHON-23. Некоректно възпроизвеждане на маската в конкретния файл**

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

**PSDPYTHON-24. NullReferenceException в Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI Формат] Оптимизиране на използването на паметта в AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Паметта за C# използвана е 220, но за Python нямаме директен достъп до дейностите на GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Зареждане на AI изображението.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Запазване на първата страница на AI изображението като PNG изображение.
            image.save(firstPageOutputPng, pngOpt)

            # Промяна на активния индекс на страницата на втората страница.
            image.active_page_index = 1

            # Запазване на втората страница на AI изображението като PNG изображение.
            image.save(secondPageOutputPng, pngOpt)

            # Промяна на активния индекс на страницата към третата страница.
            image.active_page_index = 2

            # Запазване на третата страница на AI изображението като PNG изображение.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Използването на паметта е твърде голямо. {} вместо {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

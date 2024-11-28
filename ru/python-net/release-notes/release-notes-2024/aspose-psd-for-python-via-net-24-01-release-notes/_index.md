---
title: Aspose.PSD для Python via .NET 24.1 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-dlya-python-cherez-net-24-1-primechaniya-k-vypusku/
---

{{% alert color="primary" %}}

Эта страница содержит примечания о выпуске для [Aspose.PSD для Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**     | **Краткое описание**                                                                                                | **Категория** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | Добавлена базовая обработка многостраничных изображений AI                                                    |   Функция   |
|  PSDPYTHON-22 | Эффект искажения текста не применяется к тексту                                                                    |     Ошибка     |
|  PSDPYTHON-23 | Неверная отрисовка маски в конкретном файле                                                          |     Ошибка     |
|  PSDPYTHON-24 | NullReferenceException при Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Ошибка     |
|  PSDPYTHON-25 | Исправление использования памяти в AiExporterUtils                                                    |     Ошибка     |



## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDPYTHON-19. [AI Format] Добавление базовой обработки многостраничных изображений AI**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Загрузить изображение AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # По умолчанию, ActivePageIndex равен 0.
            # Поэтому, если вы сохраните изображение AI без изменения этого свойства, будет отрисована и сохранена первая страница.
            image.save(firstPageOutputPng, PngOptions())

            # Изменить индекс активной страницы на вторую.
            image.active_page_index = 1

            # Сохранить вторую страницу изображения AI в виде PNG-изображения.
            image.save(secondPageOutputPng, PngOptions())

            # Изменить индекс активной страницы на третью.
            image.active_page_index = 2

            # Сохранить третью страницу изображения AI в виде PNG-изображения.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Эффект искажения текста не применяется к тексту**

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

**PSDPYTHON-23. Неверная отрисовка маски в конкретном файле**

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

**PSDPYTHON-24. NullReferenceException при Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. Исправление использования памяти в AiExporterUtils**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Использование памяти в C# составляет 220, но для Python у нас нет прямого доступа к действиям GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Загрузить изображение AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Сохранить первую страницу изображения AI в виде PNG-изображения.
            image.save(firstPageOutputPng, pngOpt)

            # Изменить индекс активной страницы на вторую.
            image.active_page_index = 1

            # Сохранить вторую страницу изображения AI в виде PNG-изображения.
            image.save(secondPageOutputPng, pngOpt)

            # Изменить индекс активной страницы на третью.
            image.active_page_index = 2

            # Сохранить третью страницу изображения AI в виде PNG-изображения.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Использование памяти слишком велико. {} вместо {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

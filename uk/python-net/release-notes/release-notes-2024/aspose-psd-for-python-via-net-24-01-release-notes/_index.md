---
title: Оновлення для Aspose.PSD для Python via .NET 24.1
type: docs
weight: 10
url: /uk/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить замітки про випуск [Aspose.PSD для Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                                                                | **Категорія** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [Формат AI] Додано основну обробку багатосторінкових зображень AI                                                    |   Функціонал   |
|  PSDPYTHON-22 | Ефект текстового зведення не застосовується до тексту                                                                    |     Помилка     |
|  PSDPYTHON-23 | Некоректне відображення маски в конкретному файлі                                                          |     Помилка     |
|  PSDPYTHON-24 | Помилка NullReferenceException у Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Помилка     |
|  PSDPYTHON-25 | [Формат AI] Виправлення використання пам'яті в AiExporterUtils                                                    |     Помилка     |



## **Зміни у публічному API**
# **Нові API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDPYTHON-19. [Формат AI] Додано основну обробку багатосторінкових зображень AI**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Завантажити зображення AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # За замовчуванням, ActivePageIndex дорівнює 0.
            # Тому, якщо ви збережете зображення AI без зміни цієї властивості, буде відображено і збережено першу сторінку.
            image.save(firstPageOutputPng, PngOptions())

            # Змінити активний індекс сторінки на другу сторінку.
            image.active_page_index = 1

            # Зберегти другу сторінку зображення AI як зображення PNG.
            image.save(secondPageOutputPng, PngOptions())

            # Змінити активний індекс сторінки на третю сторінку.
            image.active_page_index = 2

            # Зберегти третю сторінку зображення AI як зображення PNG.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Ефект текстового зведення не застосовується до тексту**

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

**PSDPYTHON-23. Некоректне відображення маски в конкретному файлі**

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

**PSDPYTHON-24. Помилка NullReferenceException у Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [Формат AI] Виправлення використання пам'яті в AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Використання пам'яті в C# - 220, але для Python ми не маємо прямого доступу до діяльності GC.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Завантажити зображення AI.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Зберегти першу сторінку зображення AI як зображення PNG.
            image.save(firstPageOutputPng, pngOpt)

            # Змінити активний індекс сторінки на другу сторінку.
            image.active_page_index = 1

            # Зберегти другу сторінку зображення AI як зображення PNG.
            image.save(secondPageOutputPng, pngOpt)

            # Змінити активний індекс сторінки на третю сторінку.
            image.active_page_index = 2

            # Зберегти третю сторінку зображення AI як зображення PNG.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Використання пам'яті занадто велике. {} замість {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}


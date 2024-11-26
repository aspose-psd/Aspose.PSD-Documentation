---
title: Релизные заметки Aspose.PSD для Python via .NET 24.7
type: документация
weight: 10
url: /ru/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит релизные заметки для [Aspose.PSD для Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Краткое описание**                                                                                              | **Категория** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Исключение "Ошибка загрузки изображения." при открытии документа AI                           | Ошибка      |
| PSDPYTHON-87 | Неправильное отображение текста в выходных файлах PDF                                  | Ошибка      |
| PSDPYTHON-88 | Исправлена ошибка ImageSaveException: Сбой экспорта изображения в указанный файл на Linux | Ошибка      |
| PSDPYTHON-89 | Исправлено загрузку шрифтов при использовании Aspose.Drawing                               | Ошибка      |
| PSDPYTHON-90 | 'Арифметическая операция привела к переполнению' при создании слоя умного объекта с большим JPEG | Ошибка      |
| PSDPYTHON-91 | Файл AI не может быть преобразован в файл JPG                                            | Ошибка      |

## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Удаленные API:**
- Ни одного

## **Примеры использования:**

**PSDPYTHON-86. Исключение "Ошибка загрузки изображения." при открытии документа AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Неправильное отображение текста в выходных файлах PDF**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Исправлена ошибка ImageSaveException: Сбой экспорта изображения в указанный файл на Linux**
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


**PSDPYTHON-89. Исправлено загрузку шрифтов при использовании Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Перед обновлением. Количество установленных шрифтов: " + str(len(installedFonts.families)))
            print("- Обновление кэша шрифтов путем попытки получить название шрифта Adobe для 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- После обновления. Количество установленных шрифтов: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Арифметическая операция привела к переполнению' при создании слоя умного объекта с большим JPEG**
{{< highlight python >}}
        # Исправление осуществлено, но есть другая проблема в Aspose.PSD для Python, которая ограничивает этот тест
        # srcFile = self.GetFileInBaseFolder("source.psd")
        # imageJpg = self.GetFileInBaseFolder("test.jpg")

        # loadOpt = PsdLoadOptions()
        # loadOpt.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        # with PsdImage.load(srcFile, loadOpt) as image:
            # with open(imageJpg, "rb", buffering=0) as stream:
                # addedLayer = SmartObjectLayer(stream)
                # addedLayer.Name = "Test Layer"
                # image.AddLayer(addedLayer)
{{< /highlight >}}


**PSDPYTHON-91. Файл AI не может быть преобразован в файл JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

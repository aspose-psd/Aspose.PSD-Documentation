---
title: Освідчення Aspose.PSD для Python via .NET 24.7 - Нові версії
type: docs
weight: 10
url: /uk/python-net/aspose-psd-for-python-via-net-24-7-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить оновлення для [Aspose.PSD для Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Опис**                                                                                                       | **Категорія** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Виняток "Помилка завантаження зображення." при відкритті документу AI                                | Помилка      |
| PSDPYTHON-87 | Текст неправильно відображується в вихідних файлах PDF                                                     | Помилка      |
| PSDPYTHON-88 | Виправлено виняток ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux      | Помилка      |
| PSDPYTHON-89 | Виправлено завантаження шрифтів при використанні Aspose.Drawing                                           | Помилка      |
| PSDPYTHON-90 | 'Арифметична операція призвела до переповнення' при створенні шару розумних об'єктів з великим JPEG | Помилка      |
| PSDPYTHON-91 | Файл AI не може бути конвертований в файл JPG                                                          | Помилка      |

## **Зміни у публічному API**
# **Додані API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Вилучені API:**
- Немає

## **Приклади використання:**

**PSDPYTHON-86. Виняток "Помилка завантаження зображення." при відкритті документу AI**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Текст неправильно відображується в вихідних файлах PDF**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Виправлено виняток ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux**
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


**PSDPYTHON-89. Виправлено завантаження шрифтів при використанні Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Перед оновленням. Кількість встановлених шрифтів: " + str(len(installedFonts.families)))
            print("- Оновіть кеш шрифтів, спробувавши отримати назву шрифта Adobe для 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Після оновлення. Кількість встановлених шрифтів: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Арифметична операція призвела до переповнення' при створенні шару розумних об'єктів з великим JPEG**
{{< highlight python >}}
        # Виправлено, але є інша проблема в Aspose.PSD для Python, яка обмежує цей тест
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


**PSDPYTHON-91. Файл AI не може бути конвертований в файл JPG**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

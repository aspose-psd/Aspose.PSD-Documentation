---
title: Aspose.PSD за Python via .NET 24.7 - Бележки за изданието
type: docs
weight: 10
url: /bg/python-net/aspose-psd-za-python-chrez-net-24-7-belezhki-za-izdaniyeto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за Python via .NET 24.7](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Резюме**                                                                                                       | **Категория** |
|:-------------|:------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-86 | Изключение "Зареждането на изображението не беше успешно." при отваряне на AI документ                                          | Проблем      |
| PSDPYTHON-87 | Текстът се визуализира неправилно в изходните PDF файлове                                                  | Проблем      |
| PSDPYTHON-88 | Оправяне на ImageSaveException: Изнес на изображение неуспешен за дадения файл на Linux                          | Проблем      |
| PSDPYTHON-89 | Оправяне на зареждането на шрифтовете при използване на Aspose.Drawing                                     | Проблем      |
| PSDPYTHON-90 | 'Аритметичната операция доведе до преливане' при създаване на слой с умни обекти, използвайки голям JPEG | Проблем      |
| PSDPYTHON-91 | Файлът AI не може да бъде конвертиран в JPG файл                                                    | Проблем      |

## **Промени в общественото API**
# **Добавени API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDPYTHON-86. Изключение "Зареждането на изображението не беше успешно." при отваряне на AI документ**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        outputFile = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Текстът се визуализира неправилно в изходните PDF файлове**
{{< highlight python >}}
        src = self.GetFileInBaseFolder("CVFlor.psd")
        output = self.GetFileInOutputFolder("output.pdf")

        with PsdImage.load(src) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(output, saveOptions)
{{< /highlight >}}


**PSDPYTHON-88. Оправяне на ImageSaveException: Изнес на изображение неуспешен за дадения файл на Linux**
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


**PSDPYTHON-89. Оправяне на зареждането на шрифтовете при използване на Aspose.Drawing**
{{< highlight python >}}
        with InstalledFontCollection() as installedFonts:
            print("- Преди актуализацията. Брой инсталирани шрифтове: " + str(len(installedFonts.families)))
            print("- Обновяване на кеша с шрифтове, като се опитва да се получи име на Adobe шрифт за 'Arial': ")
            FontSettings.get_adobe_font_name("Arial")
            print("- След актуализацията. Брой инсталирани шрифтове: " + str(len(installedFonts.families)))

            assert len(installedFonts.families) > 1
{{< /highlight >}}


**PSDPYTHON-90. 'Аритметичната операция доведе до преливане' при създаване на слой с умни обекти, използвайки голям JPEG**
{{< highlight python >}}
        # Оправянето е направено, но има друг проблем в Aspose.PSD за Python, който ограничава този тест
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


**PSDPYTHON-91. Файлът AI не може да бъде конвертиран в JPG файл**
{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("aaa.ai")
        outputFile = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(sourceFile) as image:
            image.save(outputFile, PngOptions())
{{< /highlight >}}

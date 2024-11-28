---
title: Оголошення про випуск Aspose.PSD для Python via .NET 24.2
type: docs
weight: 10
url: /uk/net/aspose-psd-for-python-via-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить огляд випуску для [Aspose.PSD для Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**     | **Огляд**                                                                  | **Категорія** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | Обробка властивості кута для налаштувань заповнення візерунки               |   Функціонал   |
| PSDPYTHON-29 | Підтримка вертикального та горизонтального масштабу для шару тексту          |   Функціонал   |
| PSDPYTHON-33 | [Формат AI] Реалізація правильного відображення фону в форматі AI на основі PDF.|   Функціонал   |
| PSDPYTHON-34 | Зміна механізму дисторсії у вибиванні                                        | Вдосконалення |
| PSDPYTHON-35 | Прискорення процесу вибивання                                                | Вдосконалення |
| PSDPYTHON-36 | Виняток "Помилка завантаження зображення" під час відкриття документа          |     Помилка     |
| PSDPYTHON-37 | Виправлення збереження файлів psd із шаблоном обводки                         |     Помилка     |
| PSDPYTHON-38 | Стиль тексту неправильний в розумному об'єкті при використанні ReplaceContents|     Помилка     |
| PSDPYTHON-39 | [Формат AI] Виправлення рендерингу кубічної кривої у файлі AI                |     Помилка     |



## **Зміни у публічному API**
# **Додані API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Вилучені API:**
- Немає


## **Приклади використання**

## **Приклади використання:**

**PSDPYTHON-28. Обробка властивості кута для налаштувань заповнення візерунки**

{{< highlight python >}}

	    fileName = "PatternFillLayerWide_0"
        sourceFile = fileName + ".psd"
        outputFile = fileName + "_output.psd"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True
        with PsdImage.load(sourceFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings
            fillSettings.angle = 70
            fillLayer.update()
            image.save(outputFile, PsdOptions())

        with PsdImage.load(outputFile, loadOpt) as img:
            image = cast(PsdImage, img)
            fillLayer = cast(FillLayer, image.layers[1])
            fillSettings = fillLayer.fill_settings

            assert fillSettings.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. Підтримка вертикального та горизонтального масштабу для шару тексту**

{{< highlight python >}}

           sourceFile = "1719_src.psd"
           outputFile = "output.png"

           # Додати декілька шрифтів
           fontsFolder = "1719_Fonts"
           fontFolders = list(FontSettings.get_fonts_folders())
           fontFolders.append(fontsFolder)
           FontSettings.set_fonts_folders(fontFolders, True)

           with PsdImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-33. [Формат AI] Реалізація правильного відображення фону в форматі AI на основі PDF**

{{< highlight python >}}

           sourceFile = "pineapples.ai"
           outputFile  = "pineapples.png"

           with AiImage.load(sourceFile) as image:
               image.save(outputFile, PngOptions())

{{< /highlight >}}

**PSDPYTHON-34. Зміна механізму дисторсії у вибиванні**

{{< highlight python >}}

        sourceFile = "crow_grid.psd"       
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

**PSDPYTHON-35. Прискорення процесу вибивання**

{{< highlight python >}}

        sourceFile = "output.psd"
        outputFile = "export.png"

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        start_time = time.time()

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)

        elapsed_time = time.time() - start_time

        # Старе значення = 193300
        # Нове значення =  55500
        time_in_sec = int(elapsed_time * 1000)
        if time_in_sec > 100000:
            raise Exception("Час обробки занадто великий")        
			
{{< /highlight >}}

**PSDPYTHON-36. Виняток "Помилка завантаження зображення" під час відкриття документа**

{{< highlight python >}}
        sourceFile1 = "PRODUCT.ai"
        outputFile1 = "PRODUCT.png"

        with AiImage.load(sourceFile1) as image:
            image.save(outputFile1, PngOptions())

        sourceFile2 = "Dolota.ai"
        outputFile2 = "Dolota.png"

        with AiImage.load(sourceFile2) as image:
            image.save(outputFile2, PngOptions())       	

        sourceFile3 = "ARS_novelty_2108_out_01(1).ai"
        outputFile3 = "ARS_novelty_2108_out_01(1).png"

        with AiImage.load(sourceFile3) as image:
            image.save(outputFile3, PngOptions())

        sourceFile4 = "bit_gear.ai"      
        outputFile4 = "bit_gear.png"

        with AiImage.load(sourceFile4) as image:
            image.save(outputFile4, PngOptions())

        sourceFile5 = "test.ai"
        outputFile5 = "test.png"

        with AiImage.load(sourceFile5) as image:
            image.save(outputFile5, PngOptions())
{{< /highlight >}}

**PSDPYTHON-37. Виправлення збереження файлів psd із шаблоном обводки**

{{< highlight python >}}
	    sourceFile = "StrokeShapePattern.psd"
        outputFile = "StrokeShapePattern_output.psd"

        newPatternBounds = Rectangle(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        newPattern = [
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.white.to_argb(), Color.white.to_argb(), Color.aqua.to_argb(),
            Color.aqua.to_argb(), Color.red.to_argb(), Color.red.to_argb(), Color.aqua.to_argb(),
        ]

        with PsdImage.load(sourceFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            pattResource = None
            for globalLayerResource in image.global_layer_resources:	


                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # Дані внутрішнього малюнка обводки

                    patternItem.pattern_id = guid
                    patternItem.name = newPatternName
                    patternItem.set_pattern(newPattern, newPatternBounds)
                    break


            strokeInternalFillSettings.pattern_name = newPatternName
            strokeInternalFillSettings.pattern_id = guid + "\0"

            shapeLayer.update()

            image.save(outputFile)

        # Перевірка змінених даних.
        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            shapeLayer = cast(ShapeLayer, image.layers[1])
            strokeInternalFillSettings = shapeLayer.fill

            assert guid.upper() == strokeInternalFillSettings.pattern_id
            assert newPatternName == strokeInternalFillSettings.pattern_name + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. Стиль тексту неправильний в розумному об'єкті при використанні ReplaceContents**

{{< highlight python >}}
        inputFile = "source.psd"
        output2 = "output.png"

        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True

        with PsdImage.load(inputFile, psdLoadOptions) as image:
            psdImage = cast(PsdImage, image)
            smartObject = cast(SmartObjectLayer, psdImage.layers[1])

            smartObjectImage = cast(PsdImage, smartObject.load_contents(psdLoadOptions))

            with smartObjectImage:
                smartObject.replace_contents(smartObjectImage)

            pngOpt = PngOptions()
            pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            psdImage.save(output2, pngOpt)

{{< /highlight >}}

**PSDPYTHON-39. [Формат AI] Виправлення рендерингу кубічної кривої у файлі AI**

{{< highlight python >}}

        sourceFile = "Typography.ai"
        outputFilePath = "Typography.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

---
title: Выпуск Aspose.PSD для Python via .NET 24.4 - Примечания к выпуску
type: docs
weight: 10
url: /ru/python-net/aspose-psd-dlya-python-cherez-net-24-4-primechaniya-k-vypusku/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**      | **Описание**                                                          | **Категория**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [Формат AI] Добавлена обработка ресурсов XObjectForm                        | Функция     |
| PSDPYTHON-51 | Добавить Конструктор для ShapeLayer                                   | Функция     |
| PSDPYTHON-52 | Исправление конвертации файла Psd из RGB в CMYK                          | Ошибка         |
| PSDPYTHON-53 | Определенный файл PSD не может быть экспортирован с использованием Aspose.PSD               | Ошибка         |



## **Изменения в общедоступном API**
# **Добавленные API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Удаленные API:**
- Нет


## **Примеры использования:**


**PSDPYTHON-50. [Формат AI] Добавлена обработка ресурсов XObjectForm**

{{< highlight python >}}
        ИмяИсходногоФайла = "пример.ai"
        ПутьКВыходномуФайлу = "пример_output.png"

        с aiКартинка.load(ИмяИсходногоФайла) как картинка:
            картинка.save(ПутьКВыходномуФайлу, ПараметрыPng())
{{< /highlight >}}

**PSDPYTHON-51. Добавить Конструктор для ShapeLayer**

{{< highlight python >}}
     def проверить ShapeLayerConstructor():
        файлРезультат = "ДобавитьShapeLayer_output.psd"

        с PsdImage(600, 400) как новыйPsd:
            shapeLayer = newPsd.add_shape_layer()

            новаяФорма = generate_new_shape(newPsd.size)
            новыеФормы = [новаяФорма]
            shapeLayer.path.set_items(новыеФормы)

            shapeLayer.update()

            newPsd.save(файлРезультат)

        с PsdImage.load(файлРезультат) как img:
            изображение = cast(PsdImage, img)
            утверждать len(image.layers) == 2

            shapeLayer = cast(ShapeLayer, image.layers[1])
            internalFill = shapeLayer.fill
            strokeSettings = shapeLayer.stroke
            strokeFill = shapeLayer.stroke.fill

            утверждать len(shapeLayer.path.get_items()) == 1
            утверждать len(shapeLayer.path.get_items()[0].get_items()) == 3

            утверждать internalFill.color.to_argb() == -16127182

            утверждать strokeSettings.size == 7.41
            утверждать not strokeSettings.enabled
            утверждать strokeSettings.line_alignment == StrokePosition.CENTER
            утверждать strokeSettings.line_cap == LineCapType.BUTT_CAP
            утверждать strokeSettings.line_join == LineJoinType.MITER_JOIN
            утверждать strokeFill.color.to_argb() == -16777216
			

    def generate_new_shape(imageSize):
        новаяФорма = PathShape()

        точка1 = PointF(20, 100)
        точка2 = PointF(200, 100)
        точка3 = PointF(300, 10)

        узел1 = BezierKnotRecord()
        узел1.is_linked = True
        узел1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(точка1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка1, imageSize)
                ]

        узел2 = BezierKnotRecord()
        узел2.is_linked = True
        узел2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(точка2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка2, imageSize)
                ]

        узел3 = BezierKnotRecord()
        узел3.is_linked = True
        узел3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(точка3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(точка3, imageSize)
                ]

        bezierKnots = [
            узел1,
            узел2,
            узел3
        ]

        новаяФорма.set_items(bezierKnots)

        return новаяФорма
		
    def PointFToResourcePoint(point, imageSize):
        ImgToPsdRatio = 256 * 65535
        вернуть Point(
            int(round(point.y * (ImgToPsdRatio / imageSize.height))),
            int(round(point.x * (ImgToPsdRatio / imageSize.width)))
        )

    def assert_are_equal(expected, actual, message=None):
        если ожидаемое != фактическое:
            возбудить Исключение(message or "Объекты не равны.")
			
{{< /highlight >}}

**PSDPYTHON-52. Исправление конвертации файла Psd из RGB в CMYK**

{{< highlight python >}}
     def проверитьКонвертациюИзRgbВCmyk():
        исходныйФайл = "frog_nosymb.psd"
        выходнойФайл = "frog_nosymb_output.psd"

        с PsdImage.load(исходныйФайл) как изображение:
            psdImage = cast(PsdImage, изображение)
            psdImage.has_transparency_data = False

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.CMYK
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4

            psdImage.save(выходнойФайл, psdOptions)

        с PsdImage.load(выходнойФайл) как изображение:
            psdImage = cast(PsdImage, изображение)
            утверждать not psdImage.has_transparency_data
            утверждать psdImage.layers[0].channels_count == 4

        def утверждатьСовпадают(ожидаемое, фактическое, сообщение=None):
            если ожидаемое != фактическое:
                возбудить Исключение(message or "Объекты не равны.")			

    def утверждатьСовпадают(ожидаемое, фактическое, сообщение=None):
        если ожидаемое != фактическое:
            возбудить Исключение(message or "Объекты не равны.")
				
{{< /highlight >}}

**PSDPYTHON-53. Определенный файл PSD не может быть экспортирован с использованием Aspose.PSD**

{{< highlight python >}}
        исходныйФайл = "1966source.psd"
        выходнойPng = "output.png"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True

        с PsdImage.load(исходныйФайл, loadOpt) как psdImage:
            psdImage.save(выходнойPng, ПараметрыPng())
			
{{< /highlight >}}

---
title: Aspose.PSD для .NET 23.6 - Примечания к выпуску
type: docs
weight: 70
url: /ru/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к выпуску для [Aspose.PSD для .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                                                                         | **Категория** |
|:------------|:----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Перестройка TimeLine API                                                                                                                   | Улучшение    |
| PSDNET-1517 | Устранение артефактов при отрисовке изгиба                                                                                               | Улучшение    |
| PSDNET-1528 | Оптимизация отрисовки искажений                                                                                                            | Улучшение    |
| PSDNET-147  | Поддержка слоя коррекции порога                                                                                                            | Функция      |
| PSDNET-149  | Поддержка слоя коррекции выборочного цвета                                                                                                 | Функция      |
| PSDNET-801  | Возможность экспорта PSD TimeLine в файл GIF с анимацией                                                                                  | Функция      |
| PSDNET-1555 | Добавлена поддержка TextLayer без прямоугольных границ                                                                                    | Функция      |
| PSDNET-1582 | Поддержка ShapeLayer                                                                                                                       | Функция      |
| PSDNET-864  | При замене изображения в умном объекте не происходит обновление                                                                          | Ошибка       |
| PSDNET-1404 | Невозможно сохранить файл PSD в формате PSD с ошибкой: Режимы Rgb и Lab не могут содержать менее 3 каналов и более 4 каналов         | Ошибка       |
| PSDNET-1546 | Выравнивание текста теряется, если открывать слой TextLayer в режиме редактирования Photoshop                                           | Ошибка       |
| PSDNET-1548 | Исключение Null Reference при сохранении файла PSD                                                                                       | Ошибка       |
| PSDNET-1578 | Исключение при загрузке ShapeLayer: Точки для исходных границ вектора пока не поддерживаются                                                | Ошибка       |
| PSDNET-1579 | Исключение при загрузке VogkResource: Точки сохранены как DoubleStructures, мы читаем как UnitStructures                                    | Ошибка       |
| PSDNET-1581 | LayerType ShapeLayer пуст                                                                                                                  | Ошибка       |


## **Изменения в общедоступном API**
# **Добавленные API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Удаленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Примеры использования:**

**PSDNET-147. Поддержка слоя коррекции порога**

{{< highlight csharp >}}
string исходныйФайлССлойПорога = "цветы_исходный_файл_с_пороговым_слоем.psd";
string выходнойPsdСПороговымСлоем = "цветы_выходной_psd_с_пороговым_слоем.psd";
string выходPngСПороговымСлоем = "цветы_выход_png_с_пороговым_слоем.png";

string исходныйФайлБезПороговогоСлоя = "цветы_исходный_файл_без_порогового_слоя.psd";
string выходнойPsdБезПороговогоСлоя = "цветы_выходной_psd_без_порогового_слоя.psd";
string выходPngБезПороговогоСлоя = "цветы_выход_png_без_порогового_слоя.png";

void ПроверкаРавенства(object ожидаемый, object фактический)
{
    if (!object.Equals(ожидаемый, фактический))
    {
        throw new Exception("Объекты не равны.");
    }
}

// Получить, проверить и изменить слой коррекции порога на изображении.
using (var image = (PsdImage)Image.Load(исходныйФайлССлойПорога))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Получить слой коррекции порога.
            ThresholdLayer слойПорога = (ThresholdLayer)layer;
            var уровень = слойПорога.Level;

            // Проверить параметры слоя.
            ПроверкаРавенства(уровень, (short)115);

            // Установить параметры слоя.
            слойПорога.Level = 50;

            image.Save(выходнойPsdСПороговымСлоем);
            image.Save(выходPngСПороговымСлоем, new PngOptions());
        }
    }
}

// Добавить и установить слой коррекции порога на изображении.
using (var image = (PsdImage)Image.Load(исходныйФайлБезПороговогоСлоя))
{
    // Добавить слой коррекции порога.
    ThresholdLayer пороговыйСлой = image.AddThresholdAdjustmentLayer();

    // Установить параметры слоя.
    пороговыйСлой.Level = 115;

    image.Save(выходнойPsdБезПороговогоСлоя);
    image.Save(выходPngБезПороговогоСлоя, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Поддержка слоя коррекции выборочного цвета**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-149 goes here
{{< /highlight >}}

**PSDNET-801. Возможность экспорта PSD TimeLine в файл GIF с анимацией**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-801 goes here
{{< /highlight >}}

**PSDNET-864. При замене изображения в умном объекте не происходит обновление**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-864 goes here
{{< /highlight >}}

**PSDNET-1401. Перестройка TimeLine API**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1401 goes here
{{< /highlight >}}

**PSDNET-1404. Невозможно сохранить файл PSD в формате PSD с ошибкой: Режимы Rgb и Lab не могут содержать менее 3 каналов и более 4 каналов**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1404 goes here
{{< /highlight >}}

**PSDNET-1517. Устранение артефактов при отрисовке изгиба**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1517 goes here
{{< /highlight >}}

**PSDNET-1528. Оптимизация отрисовки искажений**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1528 goes here
{{< /highlight >}}

**PSDNET-1546. Выравнивание текста теряется, если открывать слой TextLayer в режиме редактирования Photoshop**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1546 goes here
{{< /highlight >}}

**PSDNET-1548. Исключение Null Reference при сохранении файла PSD**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1548 goes here
{{< /highlight >}}

**PSDNET-1555. Добавлена поддержка TextLayer без прямоугольных границ**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1555 goes here
{{< /highlight >}}

**PSDNET-1578. Исключение при загрузке ShapeLayer: Точки для исходных границ вектора пока не поддерживаются**

**PSDNET-1579. Исключение при загрузке VogkResource: Точки сохранены как DoubleStructures, мы читаем как UnitStructures**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1578 and PSDNET-1579 goes here
{{< /highlight >}}

**PSDNET-1581. LayerType ShapeLayer пуст**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1581 goes here
{{< /highlight >}}

**PSDNET-1582. Поддержка ShapeLayer**

{{< highlight csharp >}}
// Translation of the usage examples for PSDNET-1582 goes here
{{< /highlight >}}
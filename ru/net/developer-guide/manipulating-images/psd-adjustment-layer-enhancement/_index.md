---
title: Использование слоя коррекции для улучшения PSD
weight: 100
type: docs
description: Примеры использования слоев коррекции с помощью Aspose.PSD для C#
keywords: [слой коррекции, улучшение фотографий, коррекция кривых, улучшение уровней, инвертирование, фотофильтр, PSD API, C#, csharp, образец кода]
url: ru/net/adjustment-layer-enhancement/
---

## Обзор

В этой статье мы рассмотрим редактирование слоев коррекции в Aspose.PSD для C#. Слои коррекции - это мощная функция в редактировании изображений, которая позволяет вносить неуничтожающие изменения в ваши изображения. Aspose.PSD предоставляет обширный набор классов слоев коррекции, которые можно использовать для изменения различных аспектов ваших изображений.

Для демонстрации редактирования слоев коррекции мы используем фрагмент кода в конце страницы, который загружает изображение PSD и применяет различные коррекции к его слоям.

В приведенном ниже фрагменте кода мы начинаем с загрузки изображения PSD с использованием метода `PsdImage.Load()`. Затем настраиваем параметры сохранения выходных файлов PNG. Класс `PngOptions` позволяет указать тип цвета для выходного изображения.

Затем мы перебираем каждый слой на изображении PSD и проверяем его тип с помощью метода `IsAssignable()`. Если слой имеет определенный тип, мы приводим его к этому типу с помощью метода `Cast()` и применяем необходимую коррекцию. Например, мы изменяем яркость и контрастность `BrightnessContrastLayer`, модифицируем уровни `LevelsLayer`, добавляем точку кривой `CurvesLayer` и т. д.

Вы можете добавить дополнительный код для применения других коррекций к соответствующим слоям. Aspose.PSD предоставляет широкий выбор классов слоев коррекции, таких как [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) и другие.

Наконец, мы сохраняем измененное изображение с помощью метода `Save()` класса `PsdImage`.

Этот код предоставляет базовый обзор того, как редактировать слои коррекции в Aspose.PSD для C#. Вы можете настраивать коррекции в соответствии с вашими требованиями и изучать различные варианты, доступные в документации API.

## Пример

Приведен ниже фрагмент кода, демонстрирующий использование слоев коррекции с помощью Aspose.PSD для C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Для получения более подробной информации и примеров посетите [документацию Aspose.PSD для C#](https://docs.aspose.com/psd/net/).


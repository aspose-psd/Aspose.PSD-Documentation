---
title: Использование слоя коррекции для улучшения PSD
weight: 100
type: docs
description: Примеры использования слоя коррекции через Aspose.PSD для Python
keywords: [слой коррекции, улучшение фотографий, коррекция кривых, улучшение уровней, инвертирование, фотофильтр,  psd api, python, образец кода]
url: ru/python-net/adjustment-layer-enhancement/
---

## **Обзор**

В этой статье мы исследуем редактирование слоев коррекции в Aspose.PSD для Python. Слои коррекции - это мощная функция в редактировании изображений, которая позволяет вносить неразрушающие изменения в ваши изображения. Aspose.PSD предоставляет обширный набор классов слоев коррекции, которые вы можете использовать для модификации различных аспектов ваших изображений.

Чтобы продемонстрировать редактирование слоев коррекции, мы воспользуемся образцом кода в конце страницы, который загружает изображение PSD и применяет различные коррекции к его слоям.

В приведенном ниже образце кода мы начинаем с загрузки изображения PSD с помощью метода PsdImage.load(). Затем настраиваем параметры для сохранения выходных PNG файлов. Класс PngOptions позволяет нам указать тип цвета для выходного изображения.

Далее мы перебираем каждый слой в изображении PSD и проверяем его тип с помощью метода is_assignable(). Если слой имеет определенный тип, мы приводим его к этому типу с помощью метода cast() и применяем необходимую коррекцию. Например, мы меняем яркость и контрастность BrightnessContrastLayer, изменяем уровни LevelsLayer, добавляем точку кривой CurvesLayer и т. д.

Вы можете добавить дополнительный код для применения других коррекций к соответствующим слоям. Aspose.PSD предоставляет широкий спектр классов слоев коррекции, таких как [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) и другие.

Наконец, мы сохраняем измененное изображение с помощью метода save() класса PsdImage.

Этот код предоставляет базовый обзор того, как редактировать слои коррекции в Aspose.PSD для Python. Вы можете настраивать коррекции в соответствии с вашими требованиями и изучать различные доступные опции в документации API.

Пожалуйста, посмотрите полный пример.

## **Пример**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}

---
title: Использование слоя настройки для улучшения PSD
weight: 100
type: docs
description: Примеры использования слоя настройки через Aspose.PSD для Java
keywords: [слой настройки, улучшение фото, коррекция кривых, улучшение уровней, инвертирование, фотофильтр,  psd api, java, образец кода]
url: ru/java/adjustment-layer-enhancement/
---

## **Обзор**

В этой статье исследуется редактирование слоев настройки в Aspose.PSD для Java. Слои настройки - это мощная функция в редактировании изображений, которая позволяет вносить неуничтожающие изменения в ваши изображения. Aspose.PSD предоставляет обширный набор классов слоя настройки, которые можно использовать для изменения различных аспектов изображений.

Чтобы продемонстрировать редактирование слоев настройки, мы предоставим образец кода в конце страницы, который загружает изображение PSD и применяет различные настройки к его слоям.

В следующем фрагменте кода мы начинаем с загрузки изображения PSD с помощью метода PsdImage.load(). Затем мы настраиваем параметры для сохранения выходных файлов PNG. Класс PngOptions позволяет нам указать тип цвета для выходного изображения.

Затем мы перебираем каждый слой изображения PSD и проверяем его тип с помощью метода isAssignable(). Если слой является определенного типа, мы преобразуем его в этот тип с помощью метода cast() и применяем требуемую настройку. Например, мы корректируем яркость и контрастность BrightnessContrastLayer, изменяем уровни LevelsLayer, добавляем точку кривой к CurvesLayer и т. д.

Вы можете добавить дополнительный код для применения других настроек к соответствующим слоям. Aspose.PSD предоставляет широкий выбор классов слоя настройки, такие как [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) и многое другое.

Наконец, мы сохраняем измененное изображение с помощью метода save() класса PsdImage.

Это предоставляет базовый обзор того, как редактировать слои настройки в Aspose.PSD для Java. Вы можете настроить настройки в соответствии с вашими требованиями и изучить различные доступные параметры в документации API.

Пожалуйста, ознакомьтесь с полным примером ниже.

## **Пример**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}

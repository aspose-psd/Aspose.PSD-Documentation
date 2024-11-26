---
title: Кривая Коррекции Слоя
type: docs
weight: 30
url: /ru/java/layer-types/adjustment-layer/curves/
---

# Работа с кривой коррекции Photoshop в Java

Цель этой статьи - продемонстрировать возможности библиотеки Aspose.PSD для Java при **работе с кривыми слоями коррекции** в документах Adobe® Photoshop®. Библиотека полностью автономна. Поэтому она работает без установки редактора изображений Photoshop. Полный список функций можно найти в нашей базе знаний. Итак, вернемся к кривым.

## Обзор API

Инструмент Кривые можно представить в виде диагональной линии (кривой) на графике с высветлением в верхнем правом углу и тенями в нижнем правом углу.

Библиотека предоставляет API для работы с кривой, а именно с классом [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Однако у этого класса есть **два совершенно разных подхода** к работе с кривой. Поэтому ее можно редактировать в одном из двух режимов:

- Непрерывный (кривая представлена как путь с точками в местах изгиба)
- Дискретный (кривая представлена пунктирной линией)

Таким образом, библиотека имеет два способа изменения кривой с использованием менеджера [непрерывной](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) и [дискретной работы с кривыми](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) соответственно. Далее мы объясним, как использовать каждый из них на конкретном примере.

## Изменение цвета и тона с помощью менеджера непрерывных Кривых

[Непрерывный менеджер Кривых](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **настраивает точки изгиба непрерывной кривой** для смешанного канала (RGB), а также для каждого отдельного цветового канала. Для демонстрации некоторого изменения кривых (a) будет применено к затемненному изображению оркестра (b) для получения светлого изображения с более теплыми цветами (c):

![Рисунок 1 с кривой коррекции слоя](curves-psd-adjustment-layer-figure-1.png)

Поскольку существует два менеджера, необходимо явно выбрать один (непрерывный менеджер в данном случае), прежде чем получить к нему доступ. Затем мы можем непосредственно добавлять точки кривой в определенные координаты для желаемых цветовых каналов (композитный RGB, красный и синий соответственно), чтобы воссоздать форму кривой:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Начало координат находится в нижнем левом углу. Максимальное значение координаты точки ограничено типом данных (byte) и равно 255 (127 для знакового типа).

Также есть несколько [других методов](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager), которые можно использовать.

## Изменение тона с помощью менеджера дискретных Кривых

Менеджер дискретных Кривых также позволяет размещать точки кривой (фактически изменяя цвет и тон), но отличие в том, что они делают это по-другому. Во-первых, **кривая состоит из точек** или точек (а не сплошной линии). Во-вторых, этот менеджер **не размещает точку** в любом месте на графике. Вместо этого **точка передвигается вверх или вниз** в диапазоне значений между 255 и 0 соответственно. По умолчанию значения точек кривой увеличиваются инкрементно для формирования кривой, находящейся под углом 45 градусов.

Имея это в виду, легко воссоздать пресет Photoshop "Отрицательный (RBG)" (a) и применить его к полутоновому изображению долины (b), чтобы в конечном итоге получить негативное представление долины (c).

![Рисунок 2 с кривой коррекции слоя](curves-psd-adjustment-layer-figure-2.png) Прежде всего не забудьте выбрать соответствующий менеджер, чтобы иметь возможность использовать его, а затем установите значения точек кривой в порядке убывания, начиная с 255 вниз до 0 для каждой точки кривой (всего 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Менеджер также предоставляет несколько [других методов](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) для управления кривой.

## Заключение

В этой статье мы узнали, как работать с кривыми слоями коррекции в документах Photoshop, используя Aspose.PSD для Java в двух совершенно разных способах (непрерывные и дискретные менеджеры).

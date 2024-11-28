---
title: Слой за коригиране на криви
type: docs
weight: 30
url: /bg/java/layer-types/adjustment-layer/curves/
---

# Работа с корекция на криви в Photoshop в Java

Целта на тази статия е да демонстрира възможностите на библиотеката Aspose.PSD за Java, докато **работим с корекция на криви** в документи на Adobe® Photoshop®. Библиотеката е напълно автономна. Следователно работи без необходимост от инсталиране на редактора за снимки Photoshop. Пълният списък с [функции](https://docs.aspose.com/psd/java/features/) може да бъде намерен в нашия база от знания. Е, сега обратно към кривите.

## Преглед на API

Инструментът за криви може да бъде представен като диагонална линия (крива) на графика с високи светлини в горния десен ъгъл и сенките в долните два ъгъла.

Библиотеката предоставя API за работа с кривата, а именно, класа [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Въпреки това, този клас има **два напълно различни подхода** за работа с кривата. Следователно, тя може да бъде редактирана в един от двата режима по едно и също време:

- Постоянен (кривата е представена като път с точки на местата на извиване)
- Дискретен (кривата е представена като пунктирана линия)

И така, библиотеката предлага два начина за модифициране на кривата, използвайки съответно [непрекъснат(продължителен) мениджър](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) и [дискретен мениджър](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager). След това ще обясним как да използвате всеки от тях на конкретен пример.

## Коригиране на цветове и тон с помощта на продължителния мениджър за криви

[Продължителният мениджър за криви](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **конфигурира точките за извиване на продължителната крива** за комбинирания канал (RGB) както и за всяка отделна цветна канали. За демонстрационни цели, някакви (а) корекции на криви ще бъдат приложени към затъмнена снимка на оркестър (б), за да се получи осветена снимка с по-топли цветове (в):

![Фигура 1 на слоя за коригиране с криви](curves-psd-adjustment-layer-figure-1.png)

Понеже има два мениджъра, е необходимо ясно да се избере единият (продължителен мениджър в този случай), преди да го получи. След това можем директно да добавим точки на кривата на определени координати за желаните цветни канали (комбиниран RGB, червен и син съответно), за да възстановим формата на кривата:

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Началото на координатите е в долния ляв ъгъл. Максималната стойност на координата на точка е ограничена от типа данни (byte) и е равна на 255 (за знаков тип 127).

Съществуват и няколко [други методи](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager), които можете да използвате.

## Коригиране на тон с помощта на дискретният мениджър за криви

Дискретният мениджър за криви също позволява позициониране на точките на крива (фактически промяна на цвета и тона), но разликата е, че го прави по различен начин. Първо, **кривата се състои от точки** или точки (а не от сплошна линия). Второ, този мениджър **не поставя точка никъде** на графика. Вместо това той **премества точката нагоре или надолу** със стойности в диапазона от 255 до 0 съответно. По подразбиране стойностите на точките на кривата се увеличават инкрементално, за да създадат крива, която е под ъгъл от 45 градуса.

И така, с тази представа, е лесно да се пресъздаде настройката на Photoshop за "Отрицателен (RBG)" (а) и да се приложи към монохромно изображение на долина (б), за да се получи като крайен резултат отрицателно представяне на долината (в).

![Фигура 2 на слоя за коригиране с криви](curves-psd-adjustment-layer-figure-2.png) Първоначално, не забравяйте да изберете съответния мениджър, за да може да го използвате, и след това да зададете стойностите на точките на кривата в низходящ ред, започвайки от 255 надолу до 0 за всяка точка на кривата (общо 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Мениджърът също предоставя няколко [други методи](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) за управление на кривата.

## Заключение

В тази статия научихме как да работим с коригиране на криви в документи на Photoshop, използвайки Aspose.PSD за Java по два напълно различни начина (продължителен и дискретен мениджъри).

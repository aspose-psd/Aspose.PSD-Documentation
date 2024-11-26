---
title: Криві вирівнювання шару
type: docs
weight: 30
url: /uk/java/layer-types/adjustment-layer/curves/
---

# Робота з кривими вирівнювання Photoshop у Java

Метою цієї статті є демонстрація можливостей бібліотеки Aspose.PSD для Java під час **роботи з кривими вирівнювання** в документах Adobe® Photoshop®. Бібліотека є повністю автономною. Тому вона працює без встановлення редактора фотографій Photoshop. Повний список функцій можна знайти в нашому [базі знань](https://docs.aspose.com/psd/java/features/). Добре, тепер повернемося до кривих.

## Огляд API

Інструмент Криві можуть бути представлені у вигляді діагональної лінії (кривої) на графіку з підсвіткою у верхньому правому куті і тінями у нижньому правому куті.

Бібліотека надає API для роботи з кривою, а саме з класом [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Однак цей клас має **два абсолютно різних підходи** щодо роботи з кривою. Тому її можна редагувати в одному з двох режимів одночасно:

- Постійний (крива представлена як шлях з точками у місцях згину)
- Дискретний (крива представлена як пунктирна лінія)

Отже, у бібліотеці є два способи модифікувати криву за допомогою [постійного](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) та [дискретного менеджерів](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager) відповідно. Далі ми пояснимо, як використовувати кожен з них на конкретному прикладі.

## Налаштування кольору та тону за допомогою постійного менеджера кривих

[Постійний менеджер кривих](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **налаштовує точки згину постійної кривої** для композитного каналу (RGB) а також для кожного окремого кольорового каналу. Для демонстрації деякі налаштування кривих (a) будуть застосовані до затемненого зображення оркестру (b), щоб отримати зображення з яскравішими кольорами (c):

![Рис. 1 Шар кривих вирівнювання](curves-psd-adjustment-layer-figure-1.png)

Оскільки є два менеджери, потрібно явно вибрати один (у цьому випадку - постійний менеджер), перед тим як отримати його. Після цього можна безпосередньо додавати точки кривої в певні координати для бажаних кольорових каналів (композитний RGB, червоний і синій відповідно), щоб відтворити форму кривої:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

Початок координат знаходиться в нижньому лівому куті. Максимальне значення координати точки обмежено типом даних (байт) і дорівнює 255 (127 для знакового типу).

Також є кілька [інших методів](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager), якими можна скористатися.

## Налаштування тону за допомогою дискретного менеджера кривих

Дискретний менеджер кривих також дозволяє розташовувати точки кривої (фактично змінюючи колір та тон), але відмінність полягає в тому, що вони роблять це по-іншому. По-перше, **крива складається з точок** або крапок (а не суцільної лінії). По-друге, цей менеджер **не розміщує точку в будь-якому місці** на графіку. Замість цього він **переміщає точку вгору або вниз** з діапазоном значень між 255 та 0 відповідно. За замовчуванням значення точок кривої збільшуються поступово, щоб створити криву, яка перебуває під кутом 45 градусів.

Отже, маючи це на увазі, легко відтворити темне зображення Photoshop, що зберігає негатив (RBG) (a) та застосувати його до відтінкового зображення долини (b), щоб у кінці отримати негативне представлення долини (c).

![Рис. 2 Шар кривих вирівнювання](curves-psd-adjustment-layer-figure-2.png)

По-перше, не забудьте вибрати відповідний менеджер, щоб мати змогу використовувати його, а потім встановіть значення точок кривої в порядку зменшення, розпочинаючи з 255 вниз до 0 для кожної точки кривої (всього 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Менеджер також надає декілька [інших методів](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) для управління кривою.

## Висновок

У цій статті ми дізналися, як працювати з кривими вирівнювання в Photoshop, використовуючи Aspose.PSD для Java двома абсолютно різними способами (постійний та дискретний менеджери).

---
title: Використання слою коригування для покращення PSD
weight: 100
type: docs
description: Приклади використання слоїв коригування через Aspose.PSD для C#
keywords: [слою коригування, покращення фото, коригування кривих, підвищення рівнів, інверсія, фільтр фото, psd api, C#, csharp, зразок коду]
url: uk/net/adjustment-layer-enhancement/
---

## Огляд

У цій статті ми розглянемо редагування слоїв коригування в Aspose.PSD для C#. Слої коригування - це потужна функція в редагуванні зображень, яка дозволяє вносити неруйнівні зміни до ваших зображень. Aspose.PSD надає повний набір класів слоїв коригування, які можна використовувати для зміни різних аспектів вашого зображення.

Для демонстрації редагування слоїв коригування ми використаємо фрагмент коду у кінці сторінки, який завантажує зображення PSD та застосовує різні корекції до його слоїв.

У фрагменті коду нижче ми починаємо з завантаження зображення PSD за допомогою методу `PsdImage.Load()`. Потім налаштовуємо параметри для збереження вихідних файлів PNG. Клас `PngOptions` дозволяє нам вказати тип кольору для вихідного зображення.

Далі ми перебираємо кожний шар на зображенні PSD та перевіряємо його тип за допомогою методу `IsAssignable()`. Якщо шар є конкретного типу, ми кастуємо його до цього типу за допомогою методу `Cast()` та застосовуємо потрібну корекцію. Наприклад, ми коригуємо яскравість і контрастність в `BrightnessContrastLayer`, змінюємо рівні в `LevelsLayer`, додаємо точку кривої в `CurvesLayer` та інше.

Ви можете додати додатковий код для застосування інших покращень до відповідних шарів. Aspose.PSD надає широкий спектр класів слоїв коригування, таких як [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) та інші.

Наприкінці ми зберігаємо змінене зображення за допомогою методу `Save()` класу `PsdImage`.

Цей код надає базовий огляд того, як редагувати слої коригування в Aspose.PSD для C#. Ви можете налаштовувати корекції відповідно до ваших вимог та досліджувати різноманітні опції, доступні в документації API.

## Приклад

Ось зразок коду, демонструючи, як використовувати слої коригування за допомогою Aspose.PSD для C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Для більш детальної інформації та прикладів відвідайте [документацію з Aspose.PSD для C#](https://docs.aspose.com/psd/net/).

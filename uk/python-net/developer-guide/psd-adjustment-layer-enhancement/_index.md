---
title: Використання Adjustment Layer для покращення PSD
weight: 100
type: docs
description: Приклади використання adjustment layer через Aspose.PSD для Python
keywords: [adjustment layer, покращення фото, криві коригування, підвищення рівнів, інвертування, фото фільтр,  psd api, python, зразок коду]
url: /uk/python-net/adjustment-layer-enhancement/
---

## **Огляд**

У цій статті ми дослідимо редагування adjustment layers в Aspose.PSD для Python. Шари коригування - це потужна функція в редагуванні зображень, яка дозволяє вам вносити недеструктивні зміни до зображень. Aspose.PSD надає повний набір класів adjustment layer, які можна використовувати для модифікації різних аспектів зображень.

Для демонстрації редагування adjustment layers ми використовуємо фрагмент коду на кінці сторінки, який завантажує зображення PSD та застосовує різні корекції до його шарів.

У наведеному нижче фрагменті коду ми починаємо з завантаження зображення PSD за допомогою методу PsdImage.load(). Потім ми налаштовуємо параметри для збереження вихідних файлів PNG. Клас PngOptions дозволяє нам визначити тип кольору для вихідного зображення.

Далі ми перебираємо кожний шар в зображенні PSD та перевіряємо його тип за допомогою методу is_assignable(). Якщо шар є певного типу, ми приводимо його до цього типу за допомогою методу cast() та застосовуємо потрібне коригування. Наприклад, ми налаштовуємо яскравість та контрастність шару BrightnessContrastLayer, модифікуємо рівні шару LevelsLayer, додаємо точку кривої шару CurvesLayer та інше.

Ви можете додати додатковий код для застосування інших коригувань до відповідних шарів. Aspose.PSD надає широкий спектр класів шарів коригування, таких як [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) та ін.

Наприкінці ми зберігаємо змінене зображення за допомогою методу save() класу PsdImage.

Цей код надає базовий огляд того, як редагувати adjustment layers в Aspose.PSD для Python. Ви можете налаштувати корекції відповідно до своїх вимог та досліджувати різні опції, що доступні в документації API.

Будь ласка, перевірте повний приклад.

## **Приклад**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}

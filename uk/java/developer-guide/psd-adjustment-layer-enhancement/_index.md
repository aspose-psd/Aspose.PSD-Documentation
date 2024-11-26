---
title: Використання слою коригування для покращення PSD
weight: 100
type: docs
description: Приклади використання слою коригування через Aspose.PSD для Java
keywords: [слід коригування, покращення фото, корекція кривих, підвищення рівнів, інвертування, фільтр фото,  psd api, java, зразок коду]
url: uk/java/adjustment-layer-enhancement/
---

## **Огляд**

Ця стаття досліджує редагування слоїв коригування в Aspose.PSD для Java. Слої коригування - це потужна функція у відредагування зображень, яка дозволяє вам здійснювати неруйнівні зміни у ваших зображеннях. Aspose.PSD надає комплексний набір класів слоїв коригування, які можна використовувати для модифікації різних аспектів ваших зображень.

Для демонстрації редагування слоїв коригування ми надамо фрагмент коду для прикладу в кінці сторінки, який завантажує зображення PSD та застосовує різні корекції до його слоїв.

У наступному фрагменті коду ми починаємо з завантаження зображення PSD за допомогою методу PsdImage.load(). Потім ми налаштовуємо параметри для збереження вихідних файлів PNG. Клас PngOptions дозволяє вказати тип кольорів для вихідного зображення.

Далі ми проходимо через кожен шар в зображенні PSD і перевіряємо його тип за допомогою методу isAssignable(). Якщо шар має певний тип, ми приводимо його до цього типу за допомогою методу cast() та застосовуємо бажану корекцію. Наприклад, ми коригуємо яскравість та контрастність BrightnessContrastLayer, модифікуємо рівні LevelsLayer, додаємо точку кривої CurvesLayer і так далі.

Ви можете додати додатковий код для застосування інших корекцій до відповідних шарів. Aspose.PSD надає широкий спектр класів слоїв коригування, таких як [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) та інші.

Наприкінці ми зберігаємо змінене зображення за допомогою методу save() класу PsdImage.

Це надає базовий огляд того, як редагувати слої коригування в Aspose.PSD для Java. Ви можете налаштувати корекції відповідно до своїх вимог та дослідити різноманітні опції, доступні в документації API.

Будь ласка, перевірте повний приклад нижче.

## **Приклад**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}

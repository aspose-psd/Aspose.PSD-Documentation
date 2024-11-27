---
title: Използване на слой за приспособяване за подобряване на PSD
weight: 100
type: docs
description: Примери за използване на слой за приспособяване чрез Aspose.PSD за Python
keywords: [слой за приспособяване, подобряване на снимки, коригиране на кривки, подобряване на нивата, инверсия, филтър за снимки, psd api, python, примерен код]
url: /bg/python-net/подобряване-на-слой-за-приспособяване/
---

## **Преглед**

В тази статия ще изследваме редактирането на слоевете за приспособяване в Aspose.PSD за Python. Слоевете за приспособяване са мощна функционалност в редактирането на изображения, която ви позволява да направите неразрушителни промени върху вашите изображения. Aspose.PSD предоставя обширен набор от класове за слоевете за приспособяване, които можете да използвате, за да модифицирате различни аспекти на вашите изображения.

За да демонстрираме редактирането на слоевете за приспособяване, ще използваме фрагмент код към края на страницата, който зарежда PSD изображение и прилага различни настройки към неговите слоеве.

В следния фрагмент код започваме с зареждането на PSD изображението с помощта на метода PsdImage.load(). След това настройваме опциите за запазване на изходните PNG файлове. Класът PngOptions ни позволява да укажем типа цвят за изходното изображение.

След това итерираме през всеки слой в PSD изображението и проверяваме неговия тип чрез използването на метода is_assignable(). Ако слоят е от определен тип, го преобразуваме към този тип, използвайки метода cast() и прилагаме желаната приспособяване. Например, коригираме яркостта и контраста на BrightnessContrastLayer, променяме нивата на LevelsLayer, добавяме точка на крива към CurvesLayer и т.н.

Можете да добавите допълнителен код, за да приложите други корекции към съответните си слоеве. Aspose.PSD предоставя разнообразие от класове за слоеве за приспособяване, като [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) и други.

Накрая, запазваме модифицираното изображение с помощта на save() метода на класа PsdImage.

Този код предоставя основен преглед на начина на редактиране на слоевете за приспособяване в Aspose.PSD за Python. Можете да персонализирате корекциите според вашите изисквания и да изследвате различните налични опции в документацията на API.

Моля, проверете пълния пример.

## **Пример**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Документация- Python-Aspose-подобряване-на-слой-за-приспособяване.py" >}}
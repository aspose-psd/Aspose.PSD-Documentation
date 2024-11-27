---
title: Използване на слой за корекции за подобряване на PSD
weight: 100
type: docs
description: Примери за използване на слой за корекции чрез Aspose.PSD за Java
keywords: [слой за корекции, подобряване на снимка, корекции на криви, подобряване на нивата, обръщане, филтър за снимки,  psd api, java, примерен код]
url: bg/java/настройка-слой-подобряване/
---

## **Преглед**

Тази статия разглежда редактирането на слоеве за корекции в Aspose.PSD за Java. Слоевете за корекции са мощна функционалност в редактирането на изображения, която ви позволява да правите неунищожителни промени върху вашите изображения. Aspose.PSD предоставя обширен набор от класове на слоеве за корекции, които можете да използвате, за да промените различни аспекти на вашите изображения.

За да демонстрираме редактирането на слоеве за корекции, ще предоставим откъс от примерен код в края на страницата, който зарежда PSD изображение и прилага различни корекции към неговите слоеве.

В следващия откъс от код започваме с зареждането на PSD изображението с помощта на метода PsdImage.load(). След това настройваме опциите за запазване на изходните PNG файлове. Класът PngOptions ни позволява да зададем цветовия тип за изходното изображение.

След това итерираме през всеки слой в PSD изображението и проверяваме неговия тип, използвайки метода isAssignable(). Ако слоят е от определен тип, го преобразуваме към този тип, използвайки метода cast() и прилагаме желаната корекция. Например регулираме яркостта и контраста на BrightnessContrastLayer, модифицираме нивата на LevelsLayer, добавяме точка на крива на CurvesLayer и така нататък.

Можете да добавите допълнителен код, за да приложите други корекции към съответните слоеве. Aspose.PSD предоставя широка гама от класове на слоеве за корекции, като [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) и други.

Накрая, запазваме промененото изображение с помощта на метода save() на класа PsdImage.

Това осигурява основен преглед на това как да редактирате слоевете за корекции в Aspose.PSD за Java. Можете да персонализирате корекциите съобразно своите изисквания и да изследвате различните налични опции в документацията на API.

Моля, проверете пълния пример по-долу.

## **Пример**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
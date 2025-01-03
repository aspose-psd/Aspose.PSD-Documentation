---
title: Слой за коригиране на изложението
type: docs
weight: 30
url: /bg/java/layer-types/adjustment-layer/exposure/
---

# Работа със слоя за коригиране на изложението в Photoshop с Java

В тази статия ще добавим слой за коригиране на изложението в документ на Adobe® Photoshop®, използвайки Aspose.PSD за Java - библиотека за манипулиране на файловия формат PSD. Библиотеката работи без инсталиран Photoshop редактор, защото използва собствени алгоритми за обработка на изображения. Също така сме научили някои подробности свързани с API за коригиране на изложението на библиотеката.

## Преглед на API

Слоят за коригиране на изложението се конфигурира чрез класа [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), който съдържа следните свойства, за работа с коригирането на изложението:

- Той дефинира колко светлина има снимката чрез стягане или разтягане на цялата хистограма относно черните. Така влияе основно на светлините.
- За разлика от изложбения отмества се отнася основно до сенките.
- Корекция на гама. Тя коригира светлото на изображението.

## Коригиране на изложението

Коригирането на изложението и свързаните свойства се извършват чрез промяна на няколко свойства на класа. Нека приложим някои корекции на изложението (a) на под-експонирана снимка на библиотека (b), за да я направим забележима за човешкото око (c).

![Пример за слой за коригиране на изложението](exposure-adjustment-layer-figure-1.png)

Цялата корекция се извършва главно чрез корекция на гамата. Все пак, изложението и отместването също се коригират малко. Всичко, което трябва да направите, е да зададете подходящи стойности на вече споменатите свойства:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Обърнете внимание, че изложението трябва да бъде в обхват от -20.0 до 20.0, стойността на отместването трябва да бъде в обхват от -0.5 до 0.5, а обхватът на стойността на корекцията на гамата трябва да бъде между 9.99 и 0.01.

Вижте [API-то на слоя за коригиране на изложението](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) за повече подробности.

## Заключение

В тази статия сме научили как да добавим слой за коригиране на изложението в PSD файл, за да осветим изображението, както и някои подробности за API-то.

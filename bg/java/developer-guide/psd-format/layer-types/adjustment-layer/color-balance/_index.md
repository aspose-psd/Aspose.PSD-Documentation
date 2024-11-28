---
title: Слой за коригиране на цветовете в Java
type: docs
weight: 30
url: /bg/java/layer-types/adjustment-layer/color-balance/
---

# Работа с Photoshop Color Balance слой за коригиране в Java

В тази статия ще **коригираме баланса на цветовете на изображението** във формат на PSD файл в Java. Ще използваме специална библиотека на име Aspose.PSD за Java, която е инструмент за манипулиране на Photoshop документи.

Тъй като библиотеката работи с формата на файл PSD, тя съдържа почти [всички функции](https://docs.aspose.com/psd/java/features/), достъпни в редактора на Photoshop и **слоя на коригиране на цветовете** , което е напълно подходящо за тази задача, не е изключение.

Слоят за коригиране на цветовете прави възможно промяната на баланса между основните (RGB) и субтрактивните (CMY) цветове за сенките, средните тонове и осветленията по лесен и бърз начин.

## Коригиране на Баланса на Цветовете

Както споменахме по-рано, слоят за коригиране на цветовете в Aspose.PSD за Java е просто **балансьор между основни и субтрактивни цветове**. Това означава, че има три скали за всяка двойка цветове (циан/червено, маджента/зелено, жълто/синьо). Интензитетът на конкретния цвят в двойката ще се увеличи, ако стойността се движи към него и обратно. Освен това, тези три двойки са характерни за всеки диапазон от тонове (сенките, средните тонове и осветленията), което увеличава гъвкавостта на този вид коригиране.

И така, нека приложим този баланс на практика. За пример избираме червена снимка на лицето на жена (b). Лицето е толкова червено и ние ще оправим това, като **добавим слой за коригиране на цветовете** за намаляване на червено и увеличаване на циана основно (a), за да получим лице, което изглежда по-естествено (c). Отново, има много работа за този образ, но в рамките на тази статия това е всичко, което ще направим.

![Пример за слой за коригиране на цветовете](color-balance-adjustment-layer-example-figure-1.png) API на слоя за коригиране на цветовете има плосък дизайн. Следователно, [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) класът е всичко от което се нуждаете. Първоначално, запазете яркостта, защото тя е деактивирана по подразбиране. След това добавете малко зелено и повече жълто за сенките, използвайки съответните методи (чиито имена съдържат името на конкретната област от тонове и цветовете в двойката цветове), след това добавете повече циан и малко синьо за средните тонове и накрая добавете повече циан освен малко маджента и синьо:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Сега имаме снимката, която искахме! Толкова е просто, нали?

Обърнете внимание, че _стойността на всяка двойка цветове трябва да бъде в обхвата от -100 до 100_ , което са отрицателни стойности за субтрактивните цветове и положителни за основните цветове съответно, точно както в редактора на Photoshop.

За повече технически подробности относно [слоя за коригиране на цветовете](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), обърнете се към нашето API ръководство.

## Заключение

В тази статия разгледахме как да коригираме баланса на цветовете на изображението програмно в Java, използвайки библиотеката Aspose.PSD за Java. Библиотеката съдържа напълно функционален API за работа със слоеве за коригиране на цветовете в Photoshop документи.

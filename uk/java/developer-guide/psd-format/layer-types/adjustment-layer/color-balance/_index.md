---
title: Пласт шармів кольорового балансу
type: docs
weight: 30
url: /uk/java/layer-types/adjustment-layer/color-balance/
---

# Робота з пластом шармів кольорового балансу Photoshop у Java

У цій статті ми збираємося **налаштувати кольоровий баланс зображення** у форматі файлу PSD у Java. Ми будемо використовувати спеціальну бібліотеку під назвою Aspose.PSD для Java, яка є інструментом для маніпулювання документами Photoshop.

Оскільки бібліотека працює з форматом файлів PSD, вона містить практично [всі функції](https://docs.aspose.com/psd/java/features/), доступні в редакторі Photoshop, і **пласт шармів кольорового балансу** не є винятком.

Пласт шармів кольорового балансу дозволяє змінювати баланс між основними (RGB) та віднімними (CMY) кольорами для тіней, півтонів та світлин швидким та простим способом.

## Налаштуйте кольоровий баланс

Як було вказано раніше, пласт шармів кольорового балансу в Aspose.PSD для Java це саме **балансер між основними та віднімними кольорами**. Це означає, що є три шкали для кожної пари кольорів (циан/червоний, пурпурний/зелений, жовтий/синій). Інтенсивність конкретного кольору в парі збільшиться, якщо значення буде рухатися в його бік, і навпаки. Крім того, ці три пари притаманні кожній області тонального діапазону (тіні, півтони та світлини), що збільшує гнучкість такого виду налаштування.

Тож давайте застосуємо ці знання на практиці. Для прикладу ми виберемо фотографію жіночого обличчя з виглядом на червоне (b). Обличчя має велику червоність, і ми збираємося виправити це, **додаючи пласт шармів кольорового балансу**, щоб зменшити червоний та збільшити ціан в основному (a), щоб отримати обличчя, яке виглядає природніше (c). Знову, з цим зображенням потрібно багато працювати, але в межах цієї статті ми обговоримо саме це.

![Приклад пласту шармів кольорового балансу](color-balance-adjustment-layer-example-figure-1.png) API пласту шармів кольорового балансу має плаский дизайн. Тому [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) клас - все, що вам потрібно. По-перше, збережіть яскравість, оскільки вона вимкнена за замовчуванням. Потім додайте трохи зеленого і більше жовтого для тіней, використовуючи відповідні методи (назви яких складаються з імені конкретної області тонального діапазону та назв кольорів в парі кольорів), додайте більше ціану та трохи синього для півтонів, і, нарешті, додайте більше ціану, крім трохи пурпурного та синього:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Тепер ми отримали бажане зображення! Так просто, чи не так?

Зверніть увагу, що _значення кожної пари кольорів повинно бути в діапазоні від -100 до 100_ - це від'ємні значення для віднімних кольорів та позитивні для основних кольорів відповідно, так само як у редакторі Photoshop.

Зверніться до нашої API-довідки, щоб дізнатися більше технічних деталей про [пласт шармів кольорового балансу](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Висновок

У цій статті ми розглянули, як налаштувати кольоровий баланс зображення програмно в Java за допомогою бібліотеки Aspose.PSD для Java. Бібліотека містить повнофункціональне API для роботи з пластами шармів кольорового балансу в документах Photoshop.

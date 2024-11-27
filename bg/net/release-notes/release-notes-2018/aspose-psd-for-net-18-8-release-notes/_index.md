---
title: Aspose.PSD за .NET 18.8 - Забележки за версията
type: docs
weight: 50
url: /bg/net/aspose-psd-za-net-18-8-zabezhki-za-versiyata/
---

| **Ключ** | **Резюме** | **Категория** |
| :- | :- | :- |
|PSDNET-68|Поддръжка на свойството LayerCreationDateTime.|Функционалност|
|PSDNET-67|Поддръжка на SheetColor Highlighting|Функционалност|
|PSDNET-66|Способност за сливане на слоевете един в друг|Функционалност|
|PSDNET-65|Добавяне на частична поддръжка на свойството Text Layer BoundBox|Функционалност|
|PSDNET-64|Добавяне на поддръжка за IopaResource|Функционалност|
|PSDNET-56|Поддръжка за Layer Effects за формата PSD|Функционалност|
|PSDNET-55|Поддръжка на InterruptMonitor за .Net|Функционалност|
|PSDNET-50|Възможност за слепване на слоевете|Функционалност|
|PSDNET-49|Добавяне на рендериране на свойството за пълното запълване в слоевете.|Функционалност|
|PSDNET-43|Изпълнение на рендиране на Curves Adjustment Layer|Функционалност|
|PSDNET-42|Добавяне на поддръжка на Curves Adjustment Layer|Функционалност|
|PSDNET-41|Изпълнение на рендиране на Levels Adjustment Layer|Функционалност|
|PSDNET-40|Добавяне на поддръжка на Levels Adjustment Layer|Функционалност|
|PSDNET-37|Добавяне на поддръжка на Channel Mixer Adjustment Layer|Функционалност|
|PSDNET-35|Добавяне на поддръжка на Hue/Saturation Adjustment Layer|Функционалност|
|PSDNET-34|Изпълнение на рендиране на Exposure Adjustment Layer за експорт.|Функционалност|
|PSDNET-31|Добавяне на поддръжка за рендиране за експорт на ChannelMixer adjustment layer|Функционалност|
|PSDNET-26|Добавяне на поддръжка на Clipping mask|Функционалност|
|PSDNET-13|Добавяне на поддръжка на слоя за отрязване|Функционалност|
|PSDNET-9|Добавяне на поддръжка на Photo Filter adjustment layer|Функционалност|
|PSDNET-8|Добавяне на поддръжка на Channel mixer adjustment layer|Функционалност|
|PSDNET-7|Добавяне на поддръжка на Exposure adjustment layer|Функционалност|
|PSDNET-6|Добавяне на поддръжка на Brightness/Contrast adjustment layer|Функционалност|
|PSDNET-5|Добавяне на частична поддръжка на слоеве за промени|Функционалност|
|PSDNET-3|Добавяне на поддръжка за PSD опция за NoBreak текст|Функционалност|
|PSDNET-2|Способност за добавяне на Text Layer през времето на работа|Функционалност|
|PSDNET-62|TIFF Codec не може да запази 16-битово канално изображение|Подобрение|
|PSDNET-61|Запазването на PSD изображение произвежда невалидни цветове на изображението|Подобрение|
|PSDNET-60|Координатата на горния ляв ъгъл е некоректна при актуализация|Подобрение|
|PSDNET-59|Грешка при актуализация на текстови слоеве|Подобрение|
|PSDNET-58|Изложете Codec свойството на JPEG2000 изображение на публика|Подобрение|
|PSDNET-57|Поправи настройките на 24bpp за експорт към BMP|Подобрение|
|PSDNET-46|Корекция на пренебрегването на слоя за приспособяване при конвертиране на CMYK PSD в TIFF или JPG|Подобрение|

## **Примери за използване:**
**PSDNET-68 Поддръжка на свойството LayerCreationDateTime**

{{< highlight java >}}
   
 // Пример за свойството LayerCreationDateTime
  
string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Проверка дали датата на създаване се актуализира за новосъздадените слоеве

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Поддръжка на SheetColor Highlighting**

{{< highlight java >}}
   
 // Пример за свойството SheetColorHighlight

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);

    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;

    im.Save(exportPath);	

}

{{< /highlight >}}

...

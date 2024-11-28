---
title: Aspose.PSD для .NET 18.10 - Примітки до випуску
type: docs
weight: 30
url: /uk/net/aspose-psd-dlya-net-18-10-prymitky-do-vypusku/
---

|**Ключ**|**Короткий опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-14|Додано підтримку режимів змішування окрім звичайного|Функціонал|
|PSDNET-69|Додано підтримку ефекту Накладення кольору|Функціонал|
|PSDNET-70|Додано підтримку ефекту Падаюча тінь|Функціонал|
|PSDNET-71|Обробка для експорту ефекту Накладення кольору|Функціонал|
|PSDNET-72|Обробка для експорту ефекту Падаюча тінь|Функціонал|
|PSDNET-74|Підтримка додавання ефектів шарів під час виконання|Функціонал|
|PSDNET-73|Оптимізація швидкості завантаження ресурсів, які містять структури osTypeStructures|Помилка|
|PSDNET-79|Рефакторінг та виправлення витоків пам'яті в LayerAndMaskInfo|Покращення|

## **Приклади використання:**
**PSDNET-14 Додано підтримку режимів змішування окрім звичайного**

{{< highlight java >}}

 var files = new string[]

{

    "Звичайний",

    "Розподіл",

    "Затемнення",

    "Множення",

    "Опалення кольору",

    "Лінійне згортання",

    "Темніший колір",

    "Світліше",

    "Екран",

    "Опалення кольору",

    "Лінійне додавання",

    "Світліше колір",

    "Наложення",

    "М'яке світло",

    "Тверде світло",

    "Яскраве світло",

    "Лінійне світло",

    "Закріплене світло",

    "Тверде змішування",

    "Різниця",

    "Виключення",

    "Вирахувати",

    "Розділити",

    "Відтінок",

    "Насиченість",

    "Колір",

    "Яскравість",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // Експорт у PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "РежимЗмішування" + fileName + "_Тест100.png";

        im.Save(pngExportPath100, saveOptions);

        // Встановлення непрозорості 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "РежимЗмішування" + fileName + "_Тест50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Додано підтримку ефекту Накладення кольору**

{{< highlight java >}}

     // Редагування ефекту Накладення кольору

    string sourceFileName = "НакладенняКольору.psd";

    string psdPathAfterChange = "НакладенняКольоруЗмінено.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlay)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       colorOverlay.Color = Color.Green;

       colorOverlay.Opacity = 128;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}

**PSDNET-70 Додано підтримку ефекту Падаюча тінь**

{{< highlight java >}}

     // Редагування ефекту Падаюча тінь

    string sourceFileName = "Тінь.psd";

    string psdPathAfterChange = "ТіньЗмінено.psd";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       shadowEffect.Color = Color.Green;

       shadowEffect.Opacity = 128;

       shadowEffect.Distance = 11;

       shadowEffect.UseGlobalLight = false;

       shadowEffect.Size = 9;

       shadowEffect.Angle = 45;

       shadowEffect.Spread = 3;

       shadowEffect.Noise = 50;

       im.Save(psdPathAfterChange);

    }

{{< /highlight >}}


**PSDNET-71 Обробка для експорту ефекту Накладення кольору**

{{< highlight java >}}

    // Редагування ефекту Накладення кольору

    string sourceFileName = "НакладенняКольору.psd";

    string pngExportPath = "НакладенняКольору.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // Збереження у PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Обробка для експорту ефекту Падаюча тінь**

{{< highlight java >}}

     // Експорт Падаючої тіні

    string sourceFileName = "Тінь.psd";

    string pngExportPath = "Тінь.png";

    using (var im = LoadFile(sourceFileName))

    {

       var shadowEffect = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Black, shadowEffect.Color);

       Assert.AreEqual(255, shadowEffect.Opacity);

       Assert.AreEqual(3, shadowEffect.Distance);

       Assert.AreEqual(7, shadowEffect.Size);

       Assert.AreEqual(true, shadowEffect.UseGlobalLight);

       Assert.AreEqual(90, shadowEffect.Angle);

       Assert.AreEqual(0, shadowEffect.Spread);

       Assert.AreEqual(0, shadowEffect.Noise);

       // Збереження у PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Підтримка додавання ефектів шарів під час виконання**

{{< highlight java >}}

     // Додавання ефекту накладання кольору на шарі під час виконання

    string sourceFileName = "ТриЗвичайніШариЗЕфектомШару.psd";

    string psdExportPath = "ТриЗвичайніШариЗЕфектомШаруЗмінено.psd";

    string pngExportPath = "ТриЗвичайніШариЗЕфектомШаруЗмінено.psd";

    var loadOptions = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };



    var testFolder = string.Empty;

    var im = (PsdImage)Image.Load(testPath, loadOptions) 

    using (im)

    {

        var effect = im.Layers[1].BlendingOptions.AddColorOverlay();

        effect.Opacity = 128;

        effect.Color = Color.Green;

        effect.BlendMode = BlendMode.Normal;

        var effect = im.Layers[1].BlendingOptions.AddDropShadow();

        effect.Color = Color.Red;

        effect.Opacity = 128;

        effect.BlendMode = BlendMode.Normal;



        // Збереження у PSD    

        im.Save(psdExportPath);



        // Збереження у PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}



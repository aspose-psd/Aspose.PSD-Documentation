---
title: Aspose.PSD за .NET 18.10 - Забележки за изданието
type: docs
weight: 30
url: /bg/net/aspose-psd-za-net-18-10-zabezhki-za-izdaniyeto/
---

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-14|Добавяне на поддръжка на режимите на смесване освен Нормален|Функционалност|
|PSDNET-69|Добавяне на поддръжка на ефекта Цветен Оверлей|Функционалност|
|PSDNET-70|Добавяне на поддръжка на ефекта Сянка при падащата светлина|Функционалност|
|PSDNET-71|Визуализация за експортиране на ефекта Цветен Оверлей|Функционалност|
|PSDNET-72|Визуализация за експортиране на ефекта Сянка при падащата светлина|Функционалност|
|PSDNET-74|Поддръжка за добавяне на ефекти на слой по време на изпълнение|Функционалност|
|PSDNET-73|Оптимизиране на производителността при зареждане на ресурси, които съдържат osTypeStructures|Проблем|
|PSDNET-79|Преработка и оправяне на изтичането на памет в LayerAndMaskInfo|Подобрение|

## **Примери за използване:**
**PSDNET-14 Добавяне на поддръжка на режимите на смесване освен Нормален**

{{< highlight java >}}

 var files = new string[]

{

    "Нормален",

    "Разпери",

    "Затъмни",

    "Умножи",

    "Оцветяване на цвят",

    "Линеен затъмняващ",

    "По-тъмен цвят",

    "Осветяване",

    "Екран",

    "Оцветяване на цвят",

    "Линеен умножаващ",

    "Цвят за осветяване",

    "Наложение",

    "Мека светлина",

    "Твърда светлина",

    "Ярка светлина",

    "Линеен светлинен",

    "Бутон за светлина",

    "Смесване на цвят",

    "Разлика",

    "Изключване",

    "Изваждане",

    "Раздели",

    "Оттенък",

    "Насищане",

    "Цвят",

    "Светлина",

};

foreach (var fileName in files)

{

    using (var im = LoadFile(fileName + ".psd"))

    {

        // Изнесете към PNG

        var saveOptions = new PngOptions();

        saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

        var pngExportPath100 = "BlendMode" + fileName + "_Test100.png";

        im.Save(pngExportPath100, saveOptions);

        // Задайте прозрачност 50%

        im.Layers[1].Opacity = 127;

        var pngExportPath50 = "BlendMode" + fileName + "_Test50.png";

        im.Save(pngExportPath50, saveOptions);

    }

}

{{< /highlight >}}

**PSDNET-69 Добавяне на поддръжка на ефекта Цветен Оверлей**

{{< highlight java >}}

     // Редакция на ефекта за цветен оверлей

    string sourceFileName = "ЦветенОверлей.psd";

    string psdPathAfterChange = "ПромененЦветенОверлей.psd";

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

**PSDNET-70 Добавяне на поддръжка на ефекта Сянка при падащата светлина**

{{< highlight java >}}

     // Редакция на ефекта за сянка при падащата светлина

    string sourceFileName = "Сянка.psd";

    string psdPathAfterChange = "ПромененаСянка.psd";

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



**PSDNET-71 Визуализация за експортиране на ефекта Цветен Оверлей**

{{< highlight java >}}

    // Редакция на ефекта за цветен оверлей

    string sourceFileName = "ЦветенОверлей.psd";

    string pngExportPath = "ЦветенОверлей.png";

    using (var im = LoadFile(sourceFileName))

    {

       var colorOverlay = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Red, colorOverlay.Color);

       Assert.AreEqual(153, colorOverlay.Opacity);

       // Запазете PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-72 Визуализация за експортиране на ефекта Сянка при падащата светлина**

{{< highlight java >}}

     // Експортиране на сянката

    string sourceFileName = "Сянка.psd";

    string pngExportPath = "Сянка.png";

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

       // Запазете PNG

       var saveOptions = new PngOptions();

       saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

       im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}

**PSDNET-74 Поддръжка за добавяне на ефекти на слой по време на изпълнение**

{{< highlight java >}}

     // Добавете ефект на слоя с цветен оверлей по време на изпълнение

    string sourceFileName = "ТриРедовиСлойСЕфект.psd";

    string psdExportPath = "ТриРедовиСлойСЕфектПроменен.psd";

    string pngExportPath = "ТриРедовиСлойСЕфектПроменен.psd";

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



        // Запазете PSD    

        im.Save(psdExportPath);



        // Запазете PNG

        var saveOptions = new PngOptions();

        im.Save(pngExportPath, saveOptions);

    }

{{< /highlight >}}
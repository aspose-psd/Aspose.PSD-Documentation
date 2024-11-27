---
title: Aspose.PSD за .NET 23.3 - Бележки за изданието
type: docs
weight: 100
url: /bg/net/aspose-psd-za-net-23-3-belezhki-za-izdaniyeto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Обобщение**|**Категория**|
| :- | :- | :- |
|PSDNET-146|Поддръжка на слой за настройка на постеризация|Функционалност|
|PSDNET-1366|Имплементиране на поддръжка на VscgResource|Функционалност|
|PSDNET-1437|Добавяне на поддръжка на ресурс PostResource за данните на слоя за настройка на постеризация|Функционалност|
|PSDNET-931|Некоректен експорт към PNG слой с корекции на криви и режим на цветове CMYK|Проблем|
|PSDNET-1403|Стилът на параграфа липсва след запазването на файла и актуализацията му от страна на PS|Проблем|
|PSDNET-1453|Нарушено визуализиране на ефектите на светлина и сянка върху текст|Проблем|


## **Промени в обществения API**
# **Добавени API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **Премахнати API:**
- Нито едно


## **Примери за употреба:**

**PSDNET-146. Поддръжка на слой за настройка на постеризация**

{{< highlight csharp >}}
string изходенФайл = "zendeya_posterize.psd";
string изходенФайл = "zendeya_posterize_10.psd";

using (var изображение = (PsdImage)Image.Load(изходенФайл, new PsdLoadOptions()))
{
    foreach (Layer слой in изображение.Layers)
    {
        if (слой is PosterizeLayer)
        {
            ((PosterizeLayer)слой).Levels = 10;
            изображение.Save(изходенФайл);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. Некоректен експорт към PNG слой с корекции на криви и режим на цветове CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // the ', new PsdOptions()' provocating a bug.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Имплементиране на поддръжка на VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Стойностите не са равни.\nОчаквано:{expected}\nРезултат:{current}\nРазлика:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Червено
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Зелено
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Синьо

    image.Save(outputFile);
}

// Проверяване на промените
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Стилът на параграфа липсва след запазването на файла и актуализацията му от страна на PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] новТекст = new string[]
{
    "Заглавие \r",
    "Лорем ипсум долор сит амет, консектетур адиписицинг елит. Кви дикта минус молестиае вел беатае натуc"
};

using (PsdImage изображение = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer слой2 = изображение.AddTextLayer("Нов слой", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var текстовиДанни = слой2.TextData;

    ITextStyle стилТекст = текстовиДанни.ProducePortion().Style;

    ITextParagraph параграф = текстовиДанни.ProducePortion().Paragraph;
    ITextPortion[] новиПорции = текстовиДанни.ProducePortions(новТекст, стилТекст, параграф);

    новиПорции[0].Style.FontSize = 14;
    новиПорции[0].Style.FontName = "TwCenMT-Bold";

    новиПорции[1].Style.Leading = 20;
    новиПорции[1].Style.FontSize = 10;
    новиПорции[1].Style.FontName = "TwCenMT-Bold";

    // Премахване на стария текст
    текстовиДанни.RemovePortion(0);

    // Добавяне на нови текстови порции
    foreach (var новаПорция in новиПорции)
    {
        текстовиДанни.AddPortion(новаПорция);
    }

    текстовиДанни.UpdateLayerData();

    изображение.Save(outputFile);
}

using (PsdImage изображениеPSD = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)изображениеPSD.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string ключ0 = @" >> /6 0 >> >> /1 "; // префикс за дължина на параграф 0
    string ключ1 = @" >> /6 1 >> >> /1 "; // префикс за дължина на параграф 1
    int индекс0 = txt2Data.IndexOf(ключ0);
    int индекс1 = txt2Data.IndexOf(ключ1);

    string дължПар0 = txt2Data.Substring(индекс0 + ключ0.Length, 1);
    string дължПар1 = txt2Data.Substring(индекс1 + ключ1.Length, 3);

    string очакваноПар0 = новТекст[0].Length.ToString();
    string очакваноПар1 = (новТекст[1].Length + 1).ToString();

    if (дължПар0 != очакваноПар0 || дължПар1 != очакваноПар1)
    {
        throw new Exception(
            $"Дължината на параграфите е грешна.\nОчаквано: {очакваноПар0} и {очакваноПар1}\nРезултат: {дължПар0} и {дължПар1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Добавяне на поддръжка на ресурс PostResource за данните на слоя за настройка на постеризация**

{{< highlight csharp >}}
string изходенФайл = "zendeya_posterize.psd";
string изходенФайл = "zendeya_posterize_10.psd";

using (var изображение = (PsdImage)Image.Load(изходенФайл, new PsdLoadOptions()))
{
    Layer слой = изображение.Layers[1];

    foreach (LayerResource ресурс in слой.Resources)
    {
        if (ресурс is PostResource)
        {
            ((PostResource)ресурс).Levels = 10;
            изображение.Save(изходенФайл);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Нарушено визуализиране на ефектите на светлина и сянка върху текст**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Добавяне на текстови слоеве
    Aspose.PSD.Rectangle текстОбласт1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle текстОбласт2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle текстОбласт3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer текстСлой1 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт1);
    TextLayer текстСлой2 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт2);
    TextLayer текстСлой3 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт3);

    // Модифициране на текстовите слоеве
    текстСлой1.TextData.Items[0].Style.FontSize = 150;
    текстСлой1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой1.TextData.UpdateLayerData();

    текстСлой2.TextData.Items[0].Style.FontSize = 150;
    текстСлой2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой2.TextData.UpdateLayerData();

    текстСлой3.TextData.Items[0].Style.FontSize = 150;
    текстСлой3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой3.TextData.UpdateLayerData();

    // добавяне на ефекти
    OuterGlowEffect светкавица = текстСлой1.BlendingOptions.AddOuterGlow(); // нарушава
    светкавица.Spread = 15;
    ((ColorFillSettings)светкавица.FillColor).Color = Color.Red;

    var сянка = текстСлой2.BlendingOptions.AddDropShadow(); // нарушава с дълъг текст
    сянка.Distance = 25;
    сянка.Color = Color.DarkBlue;

    var вътрешнаСянка = текстСлой3.BlendingOptions.AddInnerShadow(); // нарушава с дълъг текст
    вътрешнаСянка.UseGlobalLight = false;
    вътрешнаСянка.Angle = -179;
    вътрешнаСянка.Distance = 10;
    вътрешнаСянка.Size = 8;
    вътрешнаСянка.Color = Color.HotPink;

    // експорт
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}```
**PSDNET-931. Некоректен експорт към PNG слой с корекции на криви и режим на цветове CMYK**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // ', new PsdOptions()' поражда грешка.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. Имплементиране на поддръжка на VscgResource**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"Стойностите не са равни.\nОчаквано:{expected}\nРезултат:{current}\nРазлика:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // Червено
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // Зелено
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // Синьо

    image.Save(outputFile);
}

// Проверка на промените
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. Стилът на параграфа липсва след запазването на файла и актуализацията му от страна на PS**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] новТекст = new string[]
{
    "Заглавие \r",
    "Лорем ипсум долор сит амет, консектетур адиписицинг елит. Кви дикта минус молестиае вел беатае натуc"
};

using (PsdImage изображение = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer слой2 = изображение.AddTextLayer("Нов слой", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var текстовиДанни = слой2.TextData;

    ITextStyle стилТекст = текстовиДанни.ProducePortion().Style;

    ITextParagraph параграф = текстовиДанни.ProducePortion().Paragraph;
    ITextPortion[] новиПорции = текстовиДанни.ProducePortions(новТекст, стилТекст, параграф);

    новиПорции[0].Style.FontSize = 14;
    новиПорции[0].Style.FontName = "TwCenMT-Bold";

    новиПорции[1].Style.Leading = 20;
    новиПорции[1].Style.FontSize = 10;
    новиПорции[1].Style.FontName = "TwCenMT-Bold";

    // Премахване на стария текст
    текстовиДанни.RemovePortion(0);

    // Добавяне на нови текстови порции
    foreach (var новаПорция in новиПорции)
    {
        текстовиДанни.AddPortion(новаПорция);
    }

    текстовиДанни.UpdateLayerData();

    изображение.Save(outputFile);
}

using (PsdImage изображениеPSD = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)изображениеPSD.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string ключ0 = @" >> /6 0 >> >> /1 "; // префикс за дължина на параграф 0
    string ключ1 = @" >> /6 1 >> >> /1 "; // префикс за дължина на параграф 1
    int индекс0 = txt2Data.IndexOf(ключ0);
    int индекс1 = txt2Data.IndexOf(ключ1);

    string дължПар0 = txt2Data.Substring(индекс0 + ключ0.Length, 1);
    string дължПар1 = txt2Data.Substring(индекс1 + ключ1.Length, 3);

    string очакваноПар0 = новТекст[0].Length.ToString();
    string очакваноПар1 = (новТекст[1].Length + 1).ToString();

    if (дължПар0 != очакваноПар0 || дължПар1 != очакваноПар1)
    {
        throw new Exception(
            $"Дължината на параграфите е грешна.\nОчаквано: {очакваноПар0} и {очакваноПар1}\nРезултат: {дължПар0} и {дължПар1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Добавяне на поддръжка на ресурс PostResource за данните на слоя за настройка на постеризация**

{{< highlight csharp >}}
string изходенФайл = "zendeya_posterize.psd";
string изходенФайл = "zendeya_posterize_10.psd";

using (var изображение = (PsdImage)Image.Load(изходенФайл, new PsdLoadOptions()))
{
    Layer слой = изображение.Layers[1];

    foreach (LayerResource ресурс in слой.Resources)
    {
        if (ресурс is PostResource)
        {
            ((PostResource)ресурс).Levels = 10;
            изображение.Save(изходенФайл);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. Нарушено визуализиране на ефектите на светлина и сянка върху текст**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // Добавяне на текстови слоеве
    Aspose.PSD.Rectangle текстОбласт1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle текстОбласт2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle текстОбласт3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer текстСлой1 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт1);
    TextLayer текстСлой2 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт2);
    TextLayer текстСлой3 = psdImage.AddTextLayer("Текст с ефекти", текстОбласт3);

    // Модифициране на текстовите слоеве
    текстСлой1.TextData.Items[0].Style.FontSize = 150;
    текстСлой1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой1.TextData.UpdateLayerData();

    текстСлой2.TextData.Items[0].Style.FontSize = 150;
    текстСлой2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой2.TextData.UpdateLayerData();

    текстСлой3.TextData.Items[0].Style.FontSize = 150;
    текстСлой3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    текстСлой3.TextData.UpdateLayerData();

    // добавяне на ефекти
    OuterGlowEffect светкавица = текстСлой1.BlendingOptions.AddOuterGlow(); // нарушава
    светкавица.Spread = 15;
    ((ColorFillSettings)светкавица.FillColor).Color = Color.Red;

    var сянка = текстСлой2.BlendingOptions.AddDropShadow(); // нарушава с дълъг текст
    сянка.Distance = 25;
    сянка.Color = Color.DarkBlue;

    var вътрешнаСянка = текстСлой3.BlendingOptions.AddInnerShadow(); // нарушава с дълъг текст
    вътрешнаСянка.UseGlobalLight = false;
    вътрешнаСянка.Angle = -179;
    вътрешнаСянка.Distance = 10;
    вътрешнаСянка.Size = 8;
    вътрешнаСянка.Color = Color.HotPink;

    // експорт
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
```
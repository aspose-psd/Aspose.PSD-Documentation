---
title: Aspose.PSD за .NET 23.6 - Бележки за версията
type: docs
weight: 70
url: /bg/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Рефакториране API за времева линия                                                                                                               | Подобрение   |
| PSDNET-1517 | Премахване на артефакти при рендиране на изкривяване                                                                                              | Подобрение   |
| PSDNET-1528 | Оптимизация на рендиране на изкривяването                                                                                                        | Подобрение   |
| PSDNET-147  | Поддръжка на Слой за корекция на прага                                                                                                            | Функционалност|
| PSDNET-149  | Поддръжка на Селективен слой за корекция на цвета                                                                                                  | Функционалност|
| PSDNET-801  | Възможност за експортиране на PSD времева линия към анимиран файл GIF                                                                               | Функционалност|
| PSDNET-1555 | Добавяне на поддръжка за TextLayer без правоъгълни граници                                                                                         | Функционалност|
| PSDNET-1582 | Поддръжка на ShapeLayer                                                                                                                          | Функционалност|
| PSDNET-864  | Замяна на изображение в Умния обект не се актуализира                                                                                               | Грешка       |
| PSDNET-1404 | PSD файл не може да бъде запазен като PSD със следното изключение: Rgb и Lab режимите не могат да съдържат по-малко от 3 канала и повече от 4 канала | Грешка       |
| PSDNET-1546 | Оправяне на оправдание на текста, ако се отвори TextLayer чрез режима за редактиране на Photoshop                                                  | Грешка       |
| PSDNET-1548 | Изключение за нулева референция при запазване на PSD файл                                                                                           | Грешка       |
| PSDNET-1578 | Изключение при зареждане на ShapeLayer: Точки за началния вектор на границите не се поддържат още                                               | Грешка       |
| PSDNET-1579 | Изключение при зареждане на VogkResource: Точките са запазени като DoubleStructures, ние ги четем като UnitStructures                            | Грешка       |
| PSDNET-1581 | LayerType на ShapeLayer е празен                                                                                                                | Грешка       |


## **Промени в публичния API**
# **Добавени API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Премахнати API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Примери за употреба:**

**PSDNET-147. Поддръжка на Слой за корекция на прага**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
string outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
string outputPngWithThresholdLayer = "flowers_threshold_output.png";

string sourceFileWithoutThresholdLayer = "flowers_source.psd";
string outputPsdWithoutThresholdLayer = "flowers_output.psd";
string outputPngWithoutThresholdLayer = "flowers_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}

// Получаване, проверка и промяна на Слоя за корекция на прага от изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Получаване на Слоя за корекция на прага.
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // Проверка на параметрите на слоевете.
            AssertAreEqual(level, (short)115);

            // Задаване на параметрите на слоевете.
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// Добавяне и задаване на Слоя за корекция на прага към изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // Добавяне на Слой за корекция на прага.
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // Задаване на параметрите на слоевете.
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Поддръжка на Селективен слой за корекция на цвета**

{{< highlight csharp >}}
string sourceFileWithSelectiveColorLayer = "houses_selectiveColor_source.psd";
string outputPsdWithSelectiveColorLayer = "houses_selectiveColor_output.psd";
string outputPngWithSelectiveColorLayer = "houses_selectiveColor_output.png";

string sourceFileWithoutSelectiveColorLayer = "houses_source.psd";
string outputPsdWithoutSelectiveColorLayer = "houses_output.psd";
string outputPngWithoutSelectiveColorLayer = "houses_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}

// Получаване, проверка и промяна на Селективния слой за корекцията на цвета от изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithSelectiveColorLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is SelectiveColorLayer)
        {
            // Получаване на Селективния слой за корекция на цвета.
            SelectiveColorLayer selcLayer = (SelectiveColorLayer)layer;
            var redCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Reds);
            var yellowCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Yellows);
            var greenCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Greens);
            var blueCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Blues);

            // Проверка на параметрите на слоевете.
            AssertAreEqual(CorrectionMethodTypes.Absolute, selcLayer.CorrectionMethod);

            AssertAreEqual(redCorrection.Cyan, (short)-31);
            AssertAreEqual(redCorrection.Magenta, (short)-12);
            AssertAreEqual(redCorrection.Yellow, (short)27);
            AssertAreEqual(redCorrection.Black, (short)33);

            AssertAreEqual(yellowCorrection.Cyan, (short)-22);
            AssertAreEqual(yellowCorrection.Magenta, (short)-19);
            AssertAreEqual(yellowCorrection.Yellow, (short)8);
            AssertAreEqual(yellowCorrection.Black, (short)0);

            AssertAreEqual(greenCorrection.Cyan, (short)0);
            AssertAreEqual(greenCorrection.Magenta, (short)0);
            AssertAreEqual(greenCorrection.Yellow, (short)0);
            AssertAreEqual(greenCorrection.Black, (short)0);

            AssertAreEqual(blueCorrection.Cyan, (short)58);
            AssertAreEqual(blueCorrection.Magenta, (short)18);
            AssertAreEqual(blueCorrection.Yellow, (short)1);
            AssertAreEqual(blueCorrection.Black, (short)7);

            // Промяна на параметрите на слоевете.
            selcLayer.CorrectionMethod = CorrectionMethodTypes.Relative;
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Reds, new CmykCorrection { Cyan = 12, Magenta = -20, Yellow = 10, Black = -15 });
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 15, Magenta = 20, Yellow = -75, Black = 42 });

            image.Save(outputPsdWithSelectiveColorLayer);
            image.Save(outputPngWithSelectiveColorLayer, new PngOptions());
        }
    }
}

// Добавяне и задаване на Селективния слой за корекция на цвета към изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithoutSelectiveColorLayer))
{
    // Добавяне на Селективен слой за корекция на цвета.
    SelectiveColorLayer selectiveColorLayer = image.AddSelectiveColorAdjustmentLayer();

    // Задаване на параметрите на слоевете.
    selectiveColorLayer.CorrectionMethod = CorrectionMethodTypes.Absolute;
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 100, Magenta = -100, Yellow = 100, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Blacks, new CmykCorrection { Cyan = 10, Magenta = 15, Yellow = 17, Black = -3 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Neutrals, new CmykCorrection { Cyan = 45, Magenta = 21, Yellow = -14, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Magentas, new CmykCorrection { Cyan = 8, Magenta = -10, Yellow = -14, Black = 25 });

    image.Save(outputPsdWithoutSelectiveColorLayer);
    image.Save(outputPngWithoutSelectiveColorLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-801. Възможност за експортиране на PSD времева линия към анимиран файл GIF**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}}

**PSDNET-864. Замяна на изображение в Умния обект не се актуализира**

{{< highlight csharp >}}
string sourceFile = "neiyi.psd";
string changeFile = "bg6.png";

string exportFile = "export.psd";
string exportImgBefore = "export_before.png";
string exportImgAfter = "export_after.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is SmartObjectLayer && layer.Name== "sucai1")
        {
            SmartObjectLayer smartObjectLayer = (SmartObjectLayer)layer;
            smartObjectLayer.ReplaceContents(changeFile);
            smartObjectLayer.EmbedLinked();

            break;                                                
        }
    }

    psdImage.Save(exportFile, new PsdOptions());
    psdImage.Save(exportImgBefore, new PngOptions());
}

using (var psdImage = (PsdImage)Image.Load(exportFile))
{
    psdImage.Save(exportImgAfter, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1401. Рефакториране API за времева линия**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output_edited.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    Timeline timeline = psdImage.Timeline;

    // Добавяне на още един кадър
    List<Frame> frames = new List<Frame>(timeline.Frames);
    frames.Add(new Frame());
    timeline.Frames = frames.ToArray();

    timeline.SwitchActiveFrame(4);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1404. PSD файл не може да бъде запазен като PSD със следното изключение: Rgb и Lab режимите не могат да съдържат по-малко от 3 канала и повече от 4 канала**

{{< highlight csharp >}}
string sourceFile = "Ex3_B1H1_Dave_Arthur.psd";
string exportPath = "export.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // Взема стандартни опции за запазване от заглавката, но заглавката има грешен брой канали.
    try
    {
        image.Save(exportPath);
    }
    catch (PsdImageException ex)
    {
        if (ex.Message != "Rgb and Lab modes can not contain less than 3 channels and more than 4 channels")
        {
            throw new Exception("Грешно изключение на PsdImageException");
        }
    }

    // Без грешка
    image.Save(exportPath, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1517. Премахване на артефакти при рендиране на изкривяване**

{{< highlight csharp >}}
string sourceFile = "smart_Test.psd";
string changeFile = "newImage.png";

string exportFile = "export.psd";
string exportImg = "export_new.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is SmartObjectLayer)
        {
            SmartObjectLayer smartObjectLayer = (SmartObjectLayer)layer;
            smartObjectLayer.ReplaceContents(changeFile);
            smartObjectLayer.EmbedLinked();

            break;
        }
    }

    psdImage.Save(exportFile, new PsdOptions());
}

using (var psdImage = (PsdImage)Image.Load(exportFile, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    psdImage.Save(exportImg, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1528. Оптимизация на рендиране на изкривяването**

{{< highlight csharp >}}
string sourceFile = "Bottom_Right.psd";
string exportFile = "output.png";

DateTime dtStart = DateTime.Now;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    psdImage.Save(exportFile, new PngOptions());
}

DateTime dtFinish = DateTime.Now;

double totalSeconds = TimeSpan.FromTicks(dtFinish.Ticks).TotalSeconds - TimeSpan.FromTicks(dtStart.Ticks).TotalSeconds;

const int MaxAllowableSecunds = 5;

// Старото време за рендиране беше около 1 минута
if (totalSeconds > MaxAllowableSecunds)
{
    throw new Exception("Рендирането е прекалено бавно и е " + totalSeconds.ToString());
}
{{< /highlight >}}

**PSDNET-1546. Оправдание на текста се губи, ако се отвори TextLayer чрез режима за редактиране на Photoshop**

{{< highlight csharp >}}
string sourceFile = "input-test.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    var textData = ((TextLayer)psdImage.Layers[2]).TextData;

    ITextStyle defaultStyle = textData.Items[0].Style;
    ITextParagraph defaultParagraph = textData.Items[0].Paragraph;
    defaultParagraph.Justification = JustificationMode.Center;
    textData.RemovePortion(0);

    AddTextPortion("Lorem Ipsum", textData, defaultStyle, defaultParagraph);
    AddTextPortion("\r", textData, defaultStyle, defaultParagraph);
    AddTextPortion(
        "Lorem ipsum is placeholder text commonly used in the graphic, print, and publishing industries for previewing layouts and visual mockups.",
        textData,
        defaultStyle,
        defaultParagraph);

    textData.UpdateLayerData();

    psdImage.Save(outputFile);
}

using (var psdImage = (PsdImage)Image.Load(outputFile))
{
    // Получаване на стойността на оправданието от Txt2Resource
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];

    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);
    string search = ") /5 << /0 "; // специфичен набор от символи, за да намерим стойността на оправданието в този файл.

    // Намиране на последната стойност на режима на оправданието в характеристиките на текстовия параграф
    int index = textData.LastIndexOf(search);
    string lastJustificationResult = textData.Substring(index + search.Length, 1);
    JustificationMode justificationValue = (JustificationMode)Int32.Parse(lastJustificationResult);

    // Проверка на коригирането на Оправданието
    if (JustificationMode.Center != justificationValue)
    {
        throw new Exception("Некоректна стойност на оправданието.");
    }
}

void AddTextPortion(string text, IText textData, ITextStyle style, ITextParagraph paragraph)
{
    ITextPortion newPortion = textData.ProducePortion();
    newPortion.Style.Apply(style);
    newPortion.Paragraph.Apply(paragraph);
    newPortion.Text = text;
    textData.AddPortion(newPortion);
}
{{< /highlight >}}

**PSDNET-1548. Изключение за нулева референция при запазване на PSD файл**

{{< highlight csharp >}}
string sourceFile = "test.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer textLayer = (TextLayer)psdImage.Layers[1];
    textLayer.UpdateText("save");

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1555. Добавяне на поддръжка за TextLayer без правоъгълни граници**

{{< highlight csharp >}}
string sourceFile = "textNoBounds.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TextLayer noBoundsTextLayer = (TextLayer)psdImage.Layers[1];
    TextLayer boundsTextLayer = (TextLayer)psdImage.Layers[2];

    boundsTextLayer.TextBoundBox = RectangleF.Empty;
    noBoundsTextLayer.TextBoundBox = new RectangleF(0, 0, 200, 100);

    TextLayer newTextLayerNoTextBox = psdImage.AddTextLayer(
        "New text - no text box",
        new Rectangle(10, 300, 0, 0)
    );

    TextLayer newTextLayerWithTextBox = psdImage.AddTextLayer(
        "New text - with text box",
        new Rectangle(10, 400, 400, 100)
    );

    boundsTextLayer.TextData.UpdateLayerData();
    noBoundsTextLayer.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1578. Изключение при зареждане на ShapeLayer: Точки за началния вектор на границите не се поддържат още**

**PSDNET-1579. Изключение при зареждане на VogkResource: Точките са запазени като DoubleStructures, ние ги четем като UnitStructures**

{{< highlight csharp >}}
string sourceFile = "PointsVectorOrigin.psd";
string outputFile = "PointsVectorOrigin.out.psd";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Тук не трябва да има изключение.

    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1581. LayerType на ShapeLayer е празен**

{{< highlight csharp >}}
string sourceFile = "StrokeShapeTest1.psd";
string outputFile = "StrokeShapeTest1.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer = image.Layers[1];

    AssertAreEqual("ShapeLayer", layer.GetType().Name);

    image.Save(outputFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}

**PSDNET-1582. Поддръжка на ShapeLayer**

{{< highlight csharp >}}
string srcFile = "ShapeLayerTest.psd";
string outFile = "ShapeLayerTest-out.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    IPath layerPath = shapeLayer.Path;

    IPathShape[] pathShapeSource = layerPath.GetItems();
    List<IPathShape> pathShapesDest = new List<IPathShape>(pathShapeSource);

    // Изходният файл съдържа 2 фигури. Премахване на втората.
    pathShapesDest.RemoveAt(1);

    layerPath.SetItems(pathShapesDest.ToArray());

    shapeLayer.Update();

    image.Save(outFile);
}
{{< /highlight >}}--- 
title: Aspose.PSD за .NET 23.6 - Бележки за версията
type: docs
weight: 70
url: /bg/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD за .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Рефакториране API за времева линия                                                                                                               | Подобрение   |
| PSDNET-1517 | Премахване на артефакти при рендиране на изкривяване                                                                                              | Подобрение   |
| PSDNET-1528 | Оптимизация на рендиране на изкривяването                                                                                                        | Подобрение   |
| PSDNET-147  | Поддръжка на Слой за корекция на прага                                                                                                            | Функционалност|
| PSDNET-149  | Поддръжка на Селективен слой за корекция на цвета                                                                                                  | Функционалност|
| PSDNET-801  | Възможност за експортиране на PSD времева линия към анимиран файл GIF                                                                               | Функционалност|
| PSDNET-1555 | Добавяне на поддръжка за TextLayer без правоъгълни граници                                                                                         | Функционалност|
| PSDNET-1582 | Поддръжка на ShapeLayer                                                                                                                          | Функционалност|
| PSDNET-864  | Замяна на изображение в Умния обект не се актуализира                                                                                               | Грешка       |
| PSDNET-1404 | PSD файл не може да бъде запазен като PSD със следното изключение: Rgb и Lab режимите не могат да съдържат по-малко от 3 канала и повече от 4 канала | Грешка       |
| PSDNET-1546 | Оправяне на оправдание на текста, ако се отвори TextLayer чрез режима за редактиране на Photoshop                                                  | Грешка       |
| PSDNET-1548 | Изключение за нулева референция при запазване на PSD файл                                                                                           | Грешка       |
| PSDNET-1578 | Изключение при зареждане на ShapeLayer: Точки за началния вектор на границите не се поддържат още                                               | Грешка       |
| PSDNET-1579 | Изключение при зареждане на VogkResource: Точките са запазени като DoubleStructures, ние ги четем като UnitStructures                            | Грешка       |
| PSDNET-1581 | LayerType на ShapeLayer е празен                                                                                                                | Грешка       |


## **Промени в публичния API**
# **Добавени API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Премахнати API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Примери за употреба:**

**PSDNET-147. Поддръжка на Слой за корекция на прага**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
string outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
string outputPngWithThresholdLayer = "flowers_threshold_output.png";

string sourceFileWithoutThresholdLayer = "flowers_source.psd";
string outputPsdWithoutThresholdLayer = "flowers_output.psd";
string outputPngWithoutThresholdLayer = "flowers_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}

// Получаване, проверка и промяна на Слоя за корекция на прага от изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Получаване на Слоя за корекция на прага.
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // Проверка на параметрите на слоевете.
            AssertAreEqual(level, (short)115);

            // Задаване на параметрите на слоевете.
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// Добавяне и задаване на Слоя за корекция на прага към изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // Добавяне на Слой за корекция на прага.
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // Задаване на параметрите на слоевете.
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Поддръжка на Селективен слой за корекция на цвета**

{{< highlight csharp >}}
string sourceFileWithSelectiveColorLayer = "houses_selectiveColor_source.psd";
string outputPsdWithSelectiveColorLayer = "houses_selectiveColor_output.psd";
string outputPngWithSelectiveColorLayer = "houses_selectiveColor_output.png";

string sourceFileWithoutSelectiveColorLayer = "houses_source.psd";
string outputPsdWithoutSelectiveColorLayer = "houses_output.psd";
string outputPngWithoutSelectiveColorLayer = "houses_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}

// Получаване, проверка и промяна на Селективния слой за корекцията на цвета от изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithSelectiveColorLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is SelectiveColorLayer)
        {
            // Получаване на Селективния слой за корекция на цвета.
            SelectiveColorLayer selcLayer = (SelectiveColorLayer)layer;
            var redCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Reds);
            var yellowCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Yellows);
            var greenCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Greens);
            var blueCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Blues);

            // Проверка на параметрите на слоевете.
            AssertAreEqual(CorrectionMethodTypes.Absolute, selcLayer.CorrectionMethod);

            AssertAreEqual(redCorrection.Cyan, (short)-31);
            AssertAreEqual(redCorrection.Magenta, (short)-12);
            AssertAreEqual(redCorrection.Yellow, (short)27);
            AssertAreEqual(redCorrection.Black, (short)33);

            AssertAreEqual(yellowCorrection.Cyan, (short)-22);
            AssertAreEqual(yellowCorrection.Magenta, (short)-19);
            AssertAreEqual(yellowCorrection.Yellow, (short)8);
            AssertAreEqual(yellowCorrection.Black, (short)0);

            AssertAreEqual(greenCorrection.Cyan, (short)0);
            AssertAreEqual(greenCorrection.Magenta, (short)0);
            AssertAreEqual(greenCorrection.Yellow, (short)0);
            AssertAreEqual(greenCorrection.Black, (short)0);

            AssertAreEqual(blueCorrection.Cyan, (short)58);
            AssertAreEqual(blueCorrection.Magenta, (short)18);
            AssertAreEqual(blueCorrection.Yellow, (short)1);
            AssertAreEqual(blueCorrection.Black, (short)7);

            // Промяна на параметрите на слоевете.
            selcLayer.CorrectionMethod = CorrectionMethodTypes.Relative;
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Reds, new CmykCorrection { Cyan = 12, Magenta = -20, Yellow = 10, Black = -15 });
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 15, Magenta = 20, Yellow = -75, Black = 42 });

            image.Save(outputPsdWithSelectiveColorLayer);
            image.Save(outputPngWithSelectiveColorLayer, new PngOptions());
        }
    }
}

// Добавяне и задаване на Селективния слой за корекция на цвета към изображението.
using (var image = (PsdImage)Image.Load(sourceFileWithoutSelectiveColorLayer))
{
    // Добавяне на Селективен слой за корекция на цвета.
    SelectiveColorLayer selectiveColorLayer = image.AddSelectiveColorAdjustmentLayer();

    // Задаване на параметрите на слоевете.
    selectiveColorLayer.CorrectionMethod = CorrectionMethodTypes.Absolute;
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 100, Magenta = -100, Yellow = 100, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Blacks, new CmykCorrection { Cyan = 10, Magenta = 15, Yellow = 17, Black = -3 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Neutrals, new CmykCorrection { Cyan = 45, Magenta = 21, Yellow = -14, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Magentas, new CmykCorrection
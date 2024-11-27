---
title: Aspose.PSD за .NET 23.10 - Бележки към версията
type: docs
weight: 30
url: /bg/net/aspose-psd-za-net-23-10-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към версията на [Aspose.PSD за .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**   | **Резюме**                                                                                                                 | **Категория** |
|:------------|:------------------------------------------------------------------------|:--------|
| PSDNET-692 | Поддръжка на вертикална посока на текста | Функционалност |
| PSDNET-1402 | Използване на настройките за удар от vstk ресурса в рисуването на облици | Функционалност |
| PSDNET-1607 | Изпълнение на рисуването на вътрешната част на облиците на линията | Функционалност |
| PSDNET-1644 | Не рисувайте слой на облика, ако не е бил променен | Функционалност |
| PSDNET-1696 | [AI Формат] Добавяне на поддръжка за четене на заглавната част от PDF базирани AI файлове | Функционалност |
| PSDNET-1560 | Различни начини за задаване на резолюция на Psd файлове не работят | Грешка |
| PSDNET-1728 | FontSettings.SetFontsFolders не работи или Aspose.PSD използва неправилния шрифт | Грешка |
| PSDNET-1739 | Регресия. Оправяне на изключение Null reference, повдигнато при PsdImage.Save когато има слой на облика | Грешка |


## **Промени в публичното API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **Премахнати API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Примери за използване:**

**PSDNET-692. Поддръжка на вертикална посока на текста**

{{< highlight csharp >}}
string sourceFile = "692_lt1.psd";
string outputFile = "692_output.png";
string fontsFolder = "692_Fonts";

var fontFolders = new List<string>(FontSettings.GetFontsFolders());
fontFolders.Add(fontsFolder);
FontSettings.SetFontsFolders(fontFolders.ToArray(), true);

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    psdImage.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Използване на настройките за удар от vstk ресурса в рисуването на облици**

{{< highlight csharp >}}
string sourceFile = "StrokeShapeTest.psd";
string outputFilePsd = "StrokeShapeTest.out.psd";
string outputFilePng = "StrokeShapeTest.out.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer = image.Layers[1];
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.GreenYellow;
    shapeLayer.Update();

    ShapeLayer shapeLayer2 = (ShapeLayer)image.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)shapeLayer2.Fill;
    gradientSettings.Dither = true;
    gradientSettings.Reverse = true;
    gradientSettings.AlignWithLayer = false;
    gradientSettings.Angle = 20;
    gradientSettings.Scale = 50;
    gradientSettings.ColorPoints[0].Location = 100;
    gradientSettings.ColorPoints[1].Location = 4000;
    gradientSettings.TransparencyPoints[0].Location = 200;
    gradientSettings.TransparencyPoints[1].Location = 3800;
    gradientSettings.TransparencyPoints[0].Opacity = 90;
    gradientSettings.TransparencyPoints[1].Opacity = 10;
    shapeLayer2.Update();

    ShapeLayer shapeLayer3 = (ShapeLayer)image.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)shapeLayer3.Stroke;
    strokeSettings.Size = 15;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    strokeFillSettings.Color = Color.GreenYellow;
    shapeLayer3.Update();

    image.Save(outputFilePsd);
    image.Save(outputFilePng, new PngOptions());
}

// Проверете променените данни.
using (PsdImage image = (PsdImage)Image.Load(outputFilePsd))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    AssertAreEqual(Color.GreenYellow, fillSettings.Color);

    ShapeLayer shapeLayer2 = (ShapeLayer)image.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)shapeLayer2.Fill;
    AssertAreEqual(true, gradientSettings.Dither);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(20.0, gradientSettings.Angle);
    AssertAreEqual(50, gradientSettings.Scale);
    AssertAreEqual(100, gradientSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, gradientSettings.ColorPoints[1].Location);
    AssertAreEqual(200, gradientSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, gradientSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, gradientSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, gradientSettings.TransparencyPoints[1].Opacity);

    ShapeLayer shapeLayer3 = (ShapeLayer)image.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)shapeLayer3.Stroke;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    AssertAreEqual(15.0, strokeSettings.Size);
    AssertAreEqual(Color.GreenYellow, strokeFillSettings.Color);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1607. Изпълнение на рисуването на вътрешната част на облици на линията**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalGradient.psd";
string outputFile = "ShapeInternalGradient.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)shapeLayer.Fill;
    fillSettings.Dither = true;
    fillSettings.Reverse = true;
    fillSettings.AlignWithLayer = false;
    fillSettings.Angle = 20.0;
    fillSettings.Scale = 50;
    fillSettings.ColorPoints[0].Location = 100;
    fillSettings.ColorPoints[1].Location = 4000;
    fillSettings.TransparencyPoints[0].Location = 200;
    fillSettings.TransparencyPoints[1].Location = 3800;
    fillSettings.TransparencyPoints[0].Opacity = 90.0;
    fillSettings.TransparencyPoints[1].Opacity = 10.0;

    shapeLayer.Update();

    image.Save(outputFile);
}

// Проверете промените в данните.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)shapeLayer.Fill;

    AssertAreEqual(true, fillSettings.Dither);
    AssertAreEqual(true, fillSettings.Reverse);
    AssertAreEqual(false, fillSettings.AlignWithLayer);
    AssertAreEqual(20.0, fillSettings.Angle);
    AssertAreEqual(50, fillSettings.Scale);
    AssertAreEqual(100, fillSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, fillSettings.ColorPoints[1].Location);
    AssertAreEqual(200, fillSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, fillSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, fillSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, fillSettings.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}



**PSDNET-1644. Не рисувайте слой на облика, ако не е бил променен**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";
string outputFile = "ShapeInternalSolid.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    // Не използвайте обновяване на слоя на облика преди запазване

    image.Save(outputFile);

    // Проверете за съхраненото рисуване на файл.
}

// Проверете, че данните за слоя на облика остават непроменени.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), fillSettings.Color);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1696. [AI Формат] Добавяне на поддръжка за четене на заглавната част от PDF базирани AI файлове**

{{< highlight csharp >}}
string sourceFile = "ai_source.ai";

void AssertIsNotNull(object expected)
{
    if (expected == null)
    {
        throw new Exception("Обектът е NULL.");
    }
}

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    AssertIsNotNull(image);
    AssertIsNotNull(image.Header);
    AssertIsNotNull(image.Header.BoundingBox);
}
{{< /highlight >}}


**PSDNET-1560. Различни начини за задаване на резолюция на Psd файлове не работят**

{{< highlight csharp >}}
string output1 = "1560_1_output.psd";
string output2 = "1560_2_output.psd";
string output3 = "1560_3_output.psd";

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    newPsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    newPsd.VerticalResolution = 100;
    newPsd.HorizontalResolution = 100;
    newPsd.Save(output1);
}

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    newPsd.SetResolution(200, 200);
    newPsd.Save(output2);
}

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions psdOptions = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    newPsd.Save(output3, psdOptions);
}

using (var psdImage1 = (PsdImage)Image.Load(output1))
{
    var resResource = psdImage1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(100, resResource.VDpi.Integer);
    AreEqual(100, resResource.HDpi.Integer);
}

using (var psdImage2 = (PsdImage)Image.Load(output2))
{
    var resResource = psdImage2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(200, resResource.VDpi.Integer);
    AreEqual(200, resResource.HDpi.Integer);
}

using (var psdImage3 = (PsdImage)Image.Load(output3))
{
    var resResource = psdImage3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(300, resResource.VDpi.Integer);
    AreEqual(300, resResource.HDpi.Integer);
}

void IsNotNull(object obj)
{
    if (obj == null)
    {
        throw new NullReferenceException();
    }
}

void AreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Обектите не са равни.");
    }
}
{{< /highlight >}}


**PSDNET-1728. FontSettings.SetFontsFolders не работи или Aspose.PSD използва неправилния шрифт**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Fonts";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            var textData = textLayer.TextData;
            textData.UpdateLayerData();
        }
    }

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1739. Регресия. Оправяне на изключение Null reference, повдигнато при PsdImage.Save когато има слой на облика**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    // Трябва да се зареди без изключение

    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[1];

    if (shapeLayer.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings не трябва да бъде null.");
    }
}
{{< /highlight >}}**PSDNET-1728. FontSettings.SetFontsFolders не работи или Aspose.PSD използва неправилния шрифт**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Шрифтове";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            var textData = textLayer.TextData;
            textData.UpdateLayerData();
        }
    }

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1739. Регресия. Оправяне на изключение Null reference, повдигнато при PsdImage.Save когато има слой на облика**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    // Трябва да се зареди без изключение

    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[1];

    if (shapeLayer.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings не трябва да бъде null.");
    }
}
{{< /highlight >}}
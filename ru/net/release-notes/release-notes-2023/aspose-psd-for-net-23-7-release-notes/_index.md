---
title: Aspose.PSD для .NET 23.7 - Примечания к выпуску
type: docs
weight: 60
url: /ru/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                                       | **Категория** |
|:------------|:------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Добавление возможности экспорта каждого слоя файла PSD в анимированный GIF файл                                | Функционал |
| PSDNET-1441 | Назначить свойство заполнения слоя формы формы vscg                                                         | Функционал |
| PSDNET-1534 | Добавление новых типов деформаций (дуга и арка)                                                              | Функционал |
| PSDNET-1543 | Изменение приложения, которое сохраняет файл PSD в Aspose.PSD, если установлено свойство UpdateMetadata       | Функционал |
| PSDNET-1567 | Увеличение зоны расчета изображения деформации                                                               | Функционал |
| PSDNET-1471 | Неправильная обработка слоя коррекции черного и белого оттенка полупрозрачности                            | Ошибка     |
| PSDNET-1505 | Замена содержимого SmartObject (когда установлена опция AllowWarpRepaint) завершается после 2 минут вычислений| Ошибка     |
| PSDNET-1585 | Добавление возможности получения реальной позиции слоя LayerGroup слева и сверху                              | Ошибка     |
| PSDNET-1589 | Неправильная работа изменения размера слоя, когда файл PSD содержит VogkResource с структурами в точках       | Ошибка     |
| PSDNET-1608 | TextBound не работает как ожидается                                                                         | Ошибка     |
| PSDNET-1612 | Добавление слоя, созданного с помощью конструктора по умолчанию, к изображению PSD не добавляет к нему ресурсы по умолчанию| Ошибка     |
| PSDNET-1623 | Timeline.LoopesCount игнорируется при экспорте в анимированный GIF                                           | Ошибка     |


## **Изменения в публичном API**
# **Добавленные API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Удаленные API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Примеры использования:**

**PSDNET-802. Добавление возможности экспортировать каждый слой файла PSD в анимированный GIF файл**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Создание кадров для каждого слоя.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // Обновление текущих состояний
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Назначение свойства заполнения слоя в форме ресурса vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Проверка сохраненных изменений
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Объекты не равны.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Слой коррекции черного и белого обрабатывает полупрозрачность неправильно**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Проверка сохраненных изменений
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("Слой 2 должен быть слоем коррекции черного и белого");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Объекты не равны");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (when the AllowWarpRepaint options is active) falls after 2 minutes of computing**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Add new types of warp (arc & arch)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Изменение приложения, которое сохраняет файл PSD в Aspose.PSD, если свойство UpdateMetadata установлено в true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // Если вы хотите изменить инструмент создателя, убедитесь, что свойство "UpdateMetadata" установлено в true. По умолчанию оно установлено в true.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Сохранение изображения. 
    image.Save(path, psdOptions);

    // Проверка инструмента создателя в коде.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Здесь будет обновлена информация об инструменте создателя.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Увеличение зоны расчета изображения деформации**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Добавление возможности получения реальной позиции слоев LayerGroup слева и сверху**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Объекты не равны.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // Получение LayerGroup.
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Вычисление реальных левой, верхней, правой и нижней позиций.
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // Позиции слева, сверху, справа и снизу для LayerGroup теперь рассчитаны правильно.
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Изменение размера слоя работает неправильно, когда файл PSD содержит VogkResource со структурами в точках**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Объекты не равны.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound не работает как ожидается**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //Шаг: Заменить текст
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Текст тест заменен";

    //Шаг: Обновить TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Проверка изменений
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // specific character set to find textBox value in this file.

    int startIndex = textData.IndexOf(search) + search.Length;
    int endIndex = textData.IndexOf("]", startIndex);
    string boxItems = textData.Substring(startIndex, endIndex - startIndex);

    string height = newTextBox.Height.ToString("0.0####").Replace(",", ".");
    string width = newTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("TextBox not updated.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Adding a layer created with default constructor to PSD image does not add default resources to it**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value; // Was NullReferenceException

    psdImage.Save(output);
}
    
LayerResource FindResource(int resType, LayerResource[] resources)
{
    if (resources != null)
    {
        foreach (var layerResource in resources)
        {
            if (layerResource.Key == resType)
            {
                return layerResource;
            }
        }
    }

    return null;
}
{{< /highlight >}}

**PSDNET-1623. Timeline.LoopesCount is ignored when exporting to animated GIF**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}}
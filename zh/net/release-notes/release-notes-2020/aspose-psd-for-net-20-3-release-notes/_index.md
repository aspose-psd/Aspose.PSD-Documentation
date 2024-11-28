---
title: Aspose.PSD for .NET 20.3 - 发行说明
type: docs
weight: 100
url: /zh/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

本页面包含了[Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-188|支持 .Net Core|功能|
|PSDNET-523|将Adobe Illustrator文件转换为PDF文件|功能|
|PSDNET-212|添加能力以在一个文本图层中呈现不同样式|功能|
|PSDNET-144|支持黑白调整图层|功能|
|PSDNET-233|添加支持将AI格式（版本8）导出为其他格式|功能|
|PSDNET-540|支持通过混合模式处理（仅用于图层组）|功能|
|PSDNET-539|异常：加载带有空Unicode Alpha名称资源的图像失败|错误|
|PSDNET-541|更改图层组可见性后输出不正确|错误|
|PSDNET-516|加载PSD图像时出现异常：颜色部分（DropShadow资源）必须包含RGB的3个颜色分量或CMYK的4个颜色分量|错误|
|PSDNET-536|如果使用简单版本的构造函数尝试在新创建的图层上绘制会出现异常|错误|

## **公共 API 更改**
# **已添加的 APIs:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **已移除的 APIs:**
- 无

## **用法示例:**
**PSDNET-523. 将Adobe Illustrator文件转换为PDF文件**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. 添加能力以在一个文本图层中呈现不同样式**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // 编辑文本样式 "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // 编辑文本样式 "2\r"

    newPortions[2].Style.FauxBold = true; // 编辑文本样式 "Bold"

    newPortions[3].Style.FauxItalic = true; // 编辑文本样式 "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // 编辑文本样式 "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // 编辑文本样式 "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. 添加支持将AI格式（版本8）导出为其他格式**

{{< highlight java >}}

 // 将AI文件导出为PSD和PNG格式的示例

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. 支持经过混合模式处理（仅用于图层组）**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "没有第23层。");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "第23层不是图层组。");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "第23层名称不是'AdjustmentGroup'。");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup 图层应该有'pass through'混合模式。");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. 更新文本图层文本时抛出异常**

{{< highlight java >}}

 // 更新文本图层文本时抛出异常

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "测试";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. 在RotateFlip操作后保存PSD图像会产生无法打开的损坏文件。**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// 应该在不出现异常的情况下执行

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // 什么也不做

}

{{< /highlight >}}

**PSDNET-539. 异常：加载带有空Unicode Alpha名称资源的图像失败**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // 这里不应该有异常

{

    // 什么也不做

}

{{< /highlight >}}

**PSDNET-541. 更改图层组可见性后输出不正确**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// 修改图层名称并保存

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // 关闭组内的所有内容

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. 加载PSD图像时出现异常：颜色部分（DropShadow资源）必须包含RGB的3个颜色分量或CMYK的4个颜色分量**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // 这里不应该有异常

{

    // 什么也不做

}

{{< /highlight >}}

**PSDNET-536. 如果使用简单版本的构造函数尝试在新创建的图层上绘制会出现异常**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // 使用 Pen 工具绘制矩形

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // 使用蓝色的 Solid Brush 绘制另一个矩形

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

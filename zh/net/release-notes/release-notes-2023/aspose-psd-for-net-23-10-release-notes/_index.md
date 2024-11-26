---
title: Aspose.PSD for .NET 23.10 - 发布说明
type: docs
weight: 30
url: /zh/net/aspose-psd-for-net-23-10-release-notes/
---

{{% alert color="primary" %}}

本页包含了 [Aspose.PSD for .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明

{{% /alert %}}

| **关键**     | **摘要**                                                                                                                | **分类** |
|:------------|:------------------------------------------------------------------------|:--------|
| PSDNET-692 | 支持垂直文字方向 | 新增功能 |
| PSDNET-1402 | 在形状描边渲染中使用来自 vstk 资源的描边设置 | 新增功能 |
| PSDNET-1607 | 实现描边形状内部区域的渲染 | 新增功能 |
| PSDNET-1644 | 如果未更改，不要重新绘制形状图层 | 新增功能 |
| PSDNET-1696 | [AI 格式] 增加对从基于 PDF 的 AI 文件中读取头文件的支持 | 新增功能 |
| PSDNET-1560 | 设置 Psd 文件分辨率的各种方式均无效 | 错误 |
| PSDNET-1728 | FontSettings.SetFontsFolders 无效或 Aspose.PSD 使用错误字体 | 错误 |
| PSDNET-1739 | 修复具有形状图层的 PsdImage.Save 时出现的空引用异常 | 错误 |


## **公共 API 更改**
# **新增 API:**
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


# **移除的 API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **使用示例:**

**PSDNET-692. 支持垂直文字方向**

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

**PSDNET-1402. 在形状描边渲染中使用来自 vstk 资源的描边设置**

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

// 检查更改的数据
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
        throw new Exception(message ?? "对象不相等。");
    }
}
{{< /highlight >}}

**PSDNET-1607. 实现描边形状内部区域的渲染**

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

// 检查更改的数据
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
        throw new Exception(message ?? "对象不相等。");
    }
}
{{< /highlight >}}

**PSDNET-1644. 如果未更改，不要重新绘制形状图层**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";
string outputFile = "ShapeInternalSolid.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    // 保存前不要更新形状图层

    image.Save(outputFile);

    // 检查已保存文件的渲染
}

// 检查形状图层数据保持不变。
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
        throw new Exception(message ?? "对象不相等。");
    }
}
{{< /highlight >}}

**PSDNET-1696. [AI 格式] 增加对从基于 PDF 的 AI 文件中读取头文件的支持**

{{< highlight csharp >}}
string sourceFile = "ai_source.ai";

void AssertIsNotNull(object expected)
{
    if (expected == null)
    {
        throw new Exception("对象为空。");
    }
}

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    AssertIsNotNull(image);
    AssertIsNotNull(image.Header);
    AssertIsNotNull(image.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. 设置 Psd 文件分辨率的各种方式均无效**

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
        throw new Exception("对象不相等。");
    }
}
{{< /highlight >}}

**PSDNET-1728. FontSettings.SetFontsFolders 无效或 Aspose.PSD 使用错误字体**

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

**PSDNET-1739. 修复具有形状图层的 PsdImage.Save 时出现的空引用异常**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    // 应该无异常加载

    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[1];

    if (shapeLayer.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings 不应为空。");
    }
}
{{< /highlight >}}
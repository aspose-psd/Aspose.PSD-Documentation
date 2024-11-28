---
title: Aspose.PSD for .NET 23.6 - 发布说明
type: docs
weight: 70
url: /zh/net/aspose-psd-for-net-23-6-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明。

{{% /alert %}}

| **关键**   | **摘要**                                                                                                                                              | **类别**    |
|:----------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|:-----------|
| PSDNET-1401 | 重构 TimeLine API                                                                                                                                       | 增强功能    |
| PSDNET-1517 | 渲染扭曲时移除伪影                                                                                                                                    | 增强功能    |
| PSDNET-1528 | 优化扭曲渲染                                                                                                                                          | 增强功能    |
| PSDNET-147  | 支持阈值调整图层                                                                                                                                      | 功能        |
| PSDNET-149  | 支持选择性颜色调整图层                                                                                                                                | 功能        |
| PSDNET-801  | 将 PSD 时间轴导出为动画 GIF 文件                                                                                                                        | 功能        |
| PSDNET-1555 | 支持无矩形边框的文本图层                                                                                                                              | 功能        |
| PSDNET-1582 | 支持形状图层                                                                                                                                          | 功能        |
| PSDNET-864  | 替换智能对象中的图像不会更新                                                                                                                          | 错误修复    |
| PSDNET-1404 | PSD 文件无法保存为 PSD，出现以下异常：Rgb 和 Lab 模式不能包含少于 3 个通道和多于 4 个通道                                                                         | 错误修复    |
| PSDNET-1546 | 如果通过 Photoshop 的编辑模式打开文本图层，则文本对齐会丢失                                                                                                | 错误修复    |
| PSDNET-1548 | 保存 PSD 文件时出现空引用异常                                                                                                                          | 错误修复    |
| PSDNET-1578 | 加载形状图层时出现异常：尚不支持矢量原点边界的点                                                                                                         | 错误修复    |
| PSDNET-1579 | 加载 VogkResource 时出现异常：点保存为 DoubleStructures，但我们读取为 UnitStructures                                                                    | 错误修复    |
| PSDNET-1581 | 形状图层的 LayerType 为空                                                                                                                            | 错误修复    |

## **公共 API 更改**
# **已添加的 API:**
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

# **已移除的 API:**
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


## **使用示例:**

**PSDNET-147. 支持阈值调整图层**

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
        throw new Exception("对象不相等。");
    }
}

// 获取、检查并更改图像中的阈值调整图层。
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // 获取阈值调整图层。
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // 检查图层参数。
            AssertAreEqual(level, (short)115);

            // 设置图层参数。
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// 添加并设置阈值调整图层到图像中。
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // 添加阈值调整图层。
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // 设置图层参数。
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. 支持选择性颜色调整图层**

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
        throw new Exception("对象不相等。");
    }
}

// 获取、检查并更改图像中的选择性颜色调整图层。
using (var image = (PsdImage)Image.Load(sourceFileWithSelectiveColorLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is SelectiveColorLayer)
        {
            // 获取选择性颜色调整图层。
            SelectiveColorLayer selcLayer = (SelectiveColorLayer)layer;
            var redCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Reds);
            var yellowCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Yellows);
            var greenCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Greens);
            var blueCorrection = selcLayer.GetCmykCorrection(SelectiveColorsTypes.Blues);

            // 检查图层参数。
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

            // 更改图层参数。
            selcLayer.CorrectionMethod = CorrectionMethodTypes.Relative;
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Reds, new CmykCorrection { Cyan = 12, Magenta = -20, Yellow = 10, Black = -15 });
            selcLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 15, Magenta = 20, Yellow = -75, Black = 42 });

            image.Save(outputPsdWithSelectiveColorLayer);
            image.Save(outputPngWithSelectiveColorLayer, new PngOptions());
        }
    }
}

// 添加并设置选择性颜色调整图层到图像中。
using (var image = (PsdImage)Image.Load(sourceFileWithoutSelectiveColorLayer))
{
    // 添加选择性颜色调整图层。
    SelectiveColorLayer selectiveColorLayer = image.AddSelectiveColorAdjustmentLayer();

    // 设置图层参数。
    selectiveColorLayer.CorrectionMethod = CorrectionMethodTypes.Absolute;
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Whites, new CmykCorrection { Cyan = 100, Magenta = -100, Yellow = 100, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Blacks, new CmykCorrection { Cyan = 10, Magenta = 15, Yellow = 17, Black = -3 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Neutrals, new CmykCorrection { Cyan = 45, Magenta = 21, Yellow = -14, Black = 0 });
    selectiveColorLayer.SetCmykCorrection(SelectiveColorsTypes.Magentas, new CmykCorrection { Cyan = 8, Magenta = -10, Yellow = -14, Black = 25 });

    image.Save(outputPsdWithoutSelectiveColorLayer);
    image.Save(outputPngWithoutSelectiveColorLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-801. 将 PSD 时间轴导出为动画 GIF 文件**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdImage.Timeline.Save(outputGif, new GifOptions());
}
{{< /highlight >}}

**PSDNET-864. 替换智能对象中的图像不会更新**

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
        if (layer is SmartObjectLayer && layer.Name == "sucai1")
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

**PSDNET-1401. 重构 TimeLine API**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output_edited.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    Timeline timeline = psdImage.Timeline;

    // 添加一帧
    List<Frame> frames = new List<Frame>(timeline.Frames);
    frames.Add(new Frame());
    timeline.Frames = frames.ToArray();

    timeline.SwitchActiveFrame(4);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1404. PSD 文件无法保存为 PSD，出现以下异常：Rgb 和 Lab 模式不能包含少于 3 个通道和多于 4 个通道**

{{< highlight csharp >}}
string sourceFile = "Ex3_B1H1_Dave_Arthur.psd";
string exportPath = "export.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    // 从标题获取默认保存选项，但是标题的通道数不正确。
    try
    {
        image.Save(exportPath);
    }
    catch (PsdImageException ex)
    {
        if (ex.Message != "Rgb 和 Lab 模
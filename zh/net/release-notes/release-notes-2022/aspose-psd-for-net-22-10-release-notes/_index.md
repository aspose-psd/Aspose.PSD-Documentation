---
title: Aspose.PSD for .NET 22.10 - 发布说明
type: docs
weight: 30
url: /zh/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

本页包含[Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)的发布说明

{{% /alert %}}

{{% alert color="warning" %}}

- 此版本在16位导出时存在回归问题，因此我们建议在使用此版本时谨慎使用此功能。
如果16位图像处理是您的主要功能，请不要将 Aspose.PSD 升级到 22.9-22.10。

我们正在努力解决这些问题。

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-1287|移除 Lfx2Resource 中的过时属性|增强|
|PSDNET-1071|Aspose.PSD 无法打开采用 ZipWithoutPrediction 压缩的 PSD(RGB/16位)|错误|
|PSDNET-1257|时间轴效果消失并以奇怪的方式显示。(在 Photoshop 中)|错误|
|PSDNET-1278|描边效果的内部位置不起作用的透明度|错误|
|PSDNET-1279|回归：打开 PSD 文件时出错|错误|
|PSDNET-1284|使用某些亚洲符号更新文本失败。解析特定符号时出错|错误|
|PSDNET-1291|使用某些亚洲符号更新文本失败。渲染特定符号时出错|错误|
|PSDNET-1292|保存特定亚洲符号后，通过 Photoshop 打开导出的文件时出错|错误|


## **公共 API 更改**
# **已添加的 API:**
- 无


# **已移除的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **使用示例:**

**PSDNET-1071. Aspose.PSD 无法打开采用 ZipWithoutPrediction 压缩的 PSD(RGB/16位)**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. 时间轴效果消失并以奇怪的方式显示。(在 Photoshop 中)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // 创建具有几个帧的时间轴。
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. 描边效果的内部位置不起作用的透明度**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. 回归：打开 PSD 文件时出错**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. 使用某些亚洲符号更新文本失败。解析特定符号时出错**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // 选择有问题的符号

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. 移除 Lfx2Resource 中的过时属性**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // 更新效果的混合模式选项
    effect.BlendMode = BlendMode.Darken;

    // 更新效果的不透明度选项
    effect.Opacity = 128; // 50%

    // 更新描边效果填充颜色选项
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. 使用某些亚洲符号更新文本失败。渲染特定符号时出错**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // 选择有问题的符号

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. 保存特定亚洲符号后，通过 Photoshop 打开导出的文件时出错**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}

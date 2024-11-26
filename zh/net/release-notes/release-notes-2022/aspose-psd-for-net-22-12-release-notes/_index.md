---
title: Aspose.PSD for .NET 22.12 - 发行说明
type: docs
weight: 10
url: /zh/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明。

{{% /alert %}}

{{% alert color="success" %}}

- 修复了一个关于 16 位导出的回归问题。

{{% /alert %}}

|**关键**|**概要**|**类别**|
| :- | :- | :- |
|PSDNET-1336|向 IText 接口添加可编辑的 TextOrientation 属性|功能|
|PSDNET-725|具有图层蒙版的指定 PSD 文件调整大小会产生不正确的蒙版|错误|
|PSDNET-1277|添加保存和加载 16 张图像蒙版的能力|错误|
|PSDNET-1281|将 16 位图像保存为 16 或 8 位图像时透明度不正确|错误|
|PSDNET-1375|修复 16 位颜色中的 CMYK|错误|


## **公共 API 更改**
# **已添加的 API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **已移除的 API:**
- 无


## **用法示例:**

**PSDNET-725. 具有图层蒙版的指定 PSD 文件调整大小会产生不正确的蒙版**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// 打开源 PSD 文件
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // 进行调整大小
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// 打开调整大小后的 PSD 文件
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // 渲染为 PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. 添加保存和加载 16 张图像蒙版的能力**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // 选项允许保存 16 位颜色
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // PSD 文件将带有透明度保存
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. 将 16 位图像保存为 16 或 8 位图像时透明度不正确**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16 位颜色 PSD 文件（带有透明度）将被打开并保存为 16 位颜色
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// 保存为 16 位颜色 PSD 文件将呈现为带透明度的 PNG 文件
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. 向 IText 接口添加可编辑的 TextOrientation 属性**

{{< highlight csharp >}}
// 以下代码演示了编辑 TextOrientation 属性的能力。
// 目前这不会影响渲染，而只允许您编辑属性值。

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // 正确读取
    }
    else
    {
        throw new Exception("TextOrientation 属性值读取不正确");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // 正确读取
    }
    else
    {
        throw new Exception("TextOrientation 属性值读取不正确");
    }
}
{{< /highlight >}}

**PSDNET-1375. 修复 16 位颜色中的 CMYK**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// 设置转换选项
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// 转换并保存
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// 打开转换后的文件并渲染为 PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

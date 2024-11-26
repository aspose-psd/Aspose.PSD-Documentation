---
title: Aspose.PSD for .NET 24.7发布说明
type: docs
weight: 60
url: /zh/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

此页面包含[Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)的发布说明。

{{% /alert %}}

| **关键字**   | **摘要**                                                                                    | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | 打开AI文档时出现“图像加载失败。”异常                                               | 错误      |
| PSDNET-2022 | 输出PDF文件中文本呈现不正确                                                           | 错误      |
| PSDNET-2061 | 修复ImageSaveException: 在Linux上给定文件的图像导出失败                     | 错误      |
| PSDNET-2080 | 使用Aspose.Drawing时修复加载字体                                                   | 错误      |
| PSDNET-2085 | 使用大JPEG创建智能对象图层时出现“算术运算导致溢出”                         | 错误      |
| PSDNET-2100 | AI文件无法转换为JPG文件                                                              | 错误      |

## **公共API更改**
# **新增API:**
- 无

# **删除API:**
- 无

## **使用示例:**

**PSDNET-1029. 打开AI文档时出现“图像加载失败。”异常**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. 输出PDF文件中文本呈现不正确**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. 修复ImageSaveException: 在Linux上给定文件的图像导出失败**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. 使用Aspose.Drawing时修复加载字体**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- 更新前。已安装的字体数量: " + installedFonts.Families.Length);
    Console.WriteLine("- 平台: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- 通过尝试获取'Arial'的Adobe字体名称来刷新字体缓存: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- 更新后。已安装的字体数量: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 使用大JPEG创建智能对象图层时出现“算术运算导致溢出”**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "测试图层";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. AI文件无法转换为JPG文件**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

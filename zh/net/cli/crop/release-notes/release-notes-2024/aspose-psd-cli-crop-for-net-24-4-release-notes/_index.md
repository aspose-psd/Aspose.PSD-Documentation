---
title: Aspose.PSD CLI截图工具 .NET 24.4 - 发行说明
type: docs
weight: 90
url: /zh/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD CLI截图工具 .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) 的发行说明

{{% /alert %}}

| **关键字**   | **摘要**                                                | **类别**     |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Aspose.PSD CLI截图工具 .NET 24.4的初始版本               |  增强功能      |


## **使用示例:**

**PSDNET-2023. Aspose.PSD CLI截图工具 .NET的初始版本**

**命令行使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**代码中使用:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};

if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

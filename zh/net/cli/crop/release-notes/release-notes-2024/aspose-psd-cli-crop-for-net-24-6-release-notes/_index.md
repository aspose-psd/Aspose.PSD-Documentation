---
title: Aspose.PSD CLI裁剪为.NET 24.6 - 发行说明
type: docs
weight: 90
url: /zh/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD CLI裁剪为.NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) 的发行说明

{{% /alert %}}

| **关键字**   | **摘要**                                                                                   | **类别**     |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI应用程序的初始版本: Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.Editor          |  增强功能      |


## **使用示例:**

**PSDNET-2110. Aspose.PSD CLI裁剪应用程序的初始版本**

**从命令行使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**从命令代码使用:**

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

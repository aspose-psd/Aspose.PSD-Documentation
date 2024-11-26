---
title: Aspose.PSD CLI调整大小用于.NET 24.6 - 发行说明
type: docs
weight: 90
url: /zh/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD CLI调整大小用于.NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) 的发行说明

{{% /alert %}}

| **关键**     | **摘要**                                                                                 | **类别** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI应用的初始版本: Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.Editor |  增强 |


## **使用示例:**

**PSDNET-2110. Aspose.PSD CLI调整大小应用的初始版本**

**从命令行使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**从代码中使用:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

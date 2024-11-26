---
title: Aspose.PSD CLI Export for .NET 24.6 - 发布说明
type: docs
weight: 90
url: /zh/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD CLI Export for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/) 的发布说明

{{% /alert %}}

| **关键**    | **摘要**                                                                                       | **分类**    |
|:------------|:-----------------------------------------------------------------------------------------------|:------------|
| PSDNET-2110 | Aspose.PSD CLI Apps 的初始发布：Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.Editor           |  功能增强   |


## **使用示例:**

**PSDNET-2110. Aspose.PSD CLI Export 应用程序的初始发布**

**在命令行中使用:**   

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**在代码中使用:**  

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "exported.png",
    OutputFormat = "png",
    LayerName = "Layer1"
};

if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(options);

{{< /highlight >}}

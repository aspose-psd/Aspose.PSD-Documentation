---
title: Aspose.PSD CLI Convert for .NET 24.6 - 发布说明
type: docs
weight: 90
url: /zh/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

本页面包含了 [Aspose.PSD CLI Convert for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) 的发布说明

{{% /alert %}}

| **关键字**     | **摘要**                                                                                   | **类别** |
|:------------|:----------------------------------------------------------------------------------------|:--------|
| PSDNET-2110 | Aspose.PSD CLI 应用程序的初始版本: Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.Editor  |  增强功能 |


## **使用示例:**

**PSDNET-2110. Aspose.PSD CLI 应用程序的初始版本: Aspose.PSD.CLI.Export 和 Aspose.PSD.CLI.NLP.Editor**

**从命令行使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**从命令代码使用:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    OutputPath = "result.zip",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(options);
{{< /highlight >}}

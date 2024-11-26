---
title: Aspose.PSD CLI转换.NET 24.4版本发布说明
type: docs
weight: 90
url: /zh/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD CLI转换.NET 24.4版本](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) 的发布说明

{{% /alert %}}

| **关键字**   | **摘要**                                                | **类别**     |
|:------------|:--------------------------------------------------------|:-------------|
| PSDNET-2023 | Aspose.PSD CLI转换应用的初始发布                  |  功能增强  |


## **使用示例:**

**PSDNET-2023. Aspose.PSD CLI转换应用的初始发布**

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

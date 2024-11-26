---
title: Aspose.PSD CLI 用于 .NET 24.4 的调整 - 发行说明
type: docs
weight: 90
url: /zh/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

本页面包含用于 [Aspose.PSD CLI 用于 .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) 的发行说明

{{% /alert %}}

| **键**       | **摘要**                                             | **类别**    |
|:-------------|:-----------------------------------------------------|:-----------|
| PSDNET-2026  | Aspose.PSD CLI 调整应用的初始发布                   | 增强功能      |


## **用法示例:**

**PSDNET-2026. Aspose.PSD CLI 调整应用的初始发布**

**从命令行使用：**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**从代码中使用：**

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

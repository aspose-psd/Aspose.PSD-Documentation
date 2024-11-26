---
title: Aspose.PSD CLI Convert for .NET 24.4 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD CLI Convert for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                 | **カテゴリ** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Aspose.PSD CLI Convert Applicationの初回リリース |  追加機能 |


## **使用例:**

**PSDNET-2023. Aspose.PSD CLI Convert Applicationの初回リリース**

**コマンドラインからの使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用:**

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

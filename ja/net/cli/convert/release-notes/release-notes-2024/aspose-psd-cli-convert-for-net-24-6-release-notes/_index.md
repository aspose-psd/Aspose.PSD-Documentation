---
title: Aspose.PSD CLI Convert for .NET 24.6 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD CLI Convert for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                                                       | **カテゴリ** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLIアプリの初版リリース: Aspose.PSD.CLI.Export および Aspose.PSD.CLI.NLP.Editor    |  機能追加 |


## **使用例:**

**PSDNET-2110. Aspose.PSD CLIアプリの初版リリース: Aspose.PSD.CLI.Export および Aspose.PSD.CLI.NLP.Editor**

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

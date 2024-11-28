---
title: Aspose.PSD CLIエクスポート .NET 24.6 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD CLIエクスポート .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**   | **概要**                                                                                    | **カテゴリ** |
|:-----------|:-------------------------------------------------------------------------------------------|:------------|
| PSDNET-2110| Aspose.PSD CLIアプリの最初のリリース: Aspose.PSD.CLI.Export および Aspose.PSD.CLI.NLP.Editor   |  拡張      |


## **使用例:**

**PSDNET-2110. Aspose.PSD CLIエクスポートアプリケーションの最初のリリース**

**コマンドラインからの使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用:**

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

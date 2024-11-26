---
title: Aspose.PSD CLI Resize for .NET 24.6 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには [Aspose.PSD CLI Resize for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                                                                  | **カテゴリ** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI アプリの初版リリース: Aspose.PSD.CLI.Export および Aspose.PSD.CLI.NLP.Editor |  拡張機能 |


## **使用例:**

**PSDNET-2110. Aspose.PSD CLI Resize アプリケーションの初版リリース**

**コマンドラインからの使用例:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用例:**

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

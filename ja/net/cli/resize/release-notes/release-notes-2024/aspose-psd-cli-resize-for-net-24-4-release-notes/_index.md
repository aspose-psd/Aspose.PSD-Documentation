---
title: Aspose.PSD CLI の .NET 24.4 のリリースノート
type: docs
weight: 90
url: /ja/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD CLI の .NET 24.4 のリリース](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**     | **概要**                                          | **カテゴリ** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Aspose.PSD CLI リサイズアプリケーションの初回リリース |  機能強化 |


## **使用例:**

**PSDNET-2026. Aspose.PSD CLI リサイズアプリケーションの初回リリース**

**コマンドラインからの使用方法:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用方法:**

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

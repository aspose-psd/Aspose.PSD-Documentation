---
title: Aspose.PSD CLI Crop for .NET 24.6 - リリースノート
type: docs
weight: 90
url: /ja/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD CLI Crop for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) のリリースノートが記載されています。

{{% /alert %}}

| **キー**     | **概要**                                                                                   | **カテゴリー** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI アプリの初回リリース: Aspose.PSD.CLI.Export および Aspose.PSD.CLI.NLP.Editor |  拡張機能 |


## **使用例:**

**PSDNET-2110. Aspose.PSD CLI Crop アプリケーションの初回リリース**

**コマンドラインからの使用例:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用例:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

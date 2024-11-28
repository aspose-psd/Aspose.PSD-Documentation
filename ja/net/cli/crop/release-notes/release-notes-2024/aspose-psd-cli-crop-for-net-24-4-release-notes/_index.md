---
title: Aspose.PSD CLI Crop for .NET 24.4 - リリースノート
type: docs
weight: 90
url: /ja/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

このページは [Aspose.PSD CLI Crop for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/) のリリースノートを含んでいます。

{{% /alert %}}

| **キー**     | **概要**                                                | **カテゴリ**  |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Aspose.PSD CLI Crop Application の最初のリリース   |  機能強化    |


## **使用例:**

**PSDNET-2023. Aspose.PSD CLI Crop Application の最初のリリース**

**コマンドラインからの使用:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**コードからの使用:**

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

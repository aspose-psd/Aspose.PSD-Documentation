---
title: Aspose.PSD CLI 크롭 for .NET 24.4 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

본 페이지는 [Aspose.PSD CLI 크롭 for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)의 릴리스 노트를 포함합니다.

{{% /alert %}}

| **키**       | **개요**                                               | **범주**     |
|:------------|:-------------------------------------------------------------|:-------------|
| PSDNET-2025 | Aspose.PSD CLI 크롭 애플리케이션의 첫 릴리스     |  향상 |

## **사용 예시:**

**PSDNET-2023. Aspose.PSD CLI 크롭 애플리케이션의 첫 릴리스**

**명령줄에서의 사용:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**코드에서의 사용:**

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

---
title: Aspose.PSD CLI Crop for .NET 24.6 - 릴리스 노트
type: docs
weight: 90
url: /psd/ko/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI Crop for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**     | **요약**                                                                                   | **범주**     |
|:-----------|:------------------------------------------------------------------------------------------|:------------|
| PSDNET-2110 | Aspose.PSD CLI 앱의 초기 릴리스: Aspose.PSD.CLI.Export 및 Aspose.PSD.CLI.NLP.Editor       |  향상      |


## **사용 예시:**

**PSDNET-2110. Aspose.PSD CLI Crop 애플리케이션의 초기 릴리스**

**명령줄에서 사용법:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**코드에서 사용법:**

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

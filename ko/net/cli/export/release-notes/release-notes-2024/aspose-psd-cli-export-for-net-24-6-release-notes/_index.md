---
title: Aspose.PSD CLI .NET 24.6 - 릴리스 노트
type: 문서
weight: 90
url: /ko/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**     | **요약**                                                                                 | **카테고리** |
|:------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI 앱의 초기 릴리스: Aspose.PSD.CLI.Export 및 Aspose.PSD.CLI.NLP.Editor |  기능 향상 |


## **사용 예시:**

**PSDNET-2110. Aspose.PSD CLI Export 애플리케이션의 초기 릴리스**

**명령줄에서의 사용법:**


{{< highlight bash >}}


Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic


{{< /highlight >}}


**코드에서의 사용법:**


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

---
title: Aspose.PSD CLI .NET 24.6에 대한 크기 조정 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI .NET 24.6의 릴리스 노트](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)가 포함되어 있습니다.

{{% /alert %}}

| **키**       | **요약**                                                                         | **카테고리** |
|:------------|:--------------------------------------------------------------------------------|:------------|
| PSDNET-2110 | Aspose.PSD CLI 앱의 초기 릴리스: Aspose.PSD.CLI.Export 및 Aspose.PSD.CLI.NLP.Editor | 개선        |


## **사용 예시:**

**PSDNET-2110. Aspose.PSD CLI 크기 조정 애플리케이션의 초기 릴리스**

**명령줄에서 사용:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**코드에서의 사용:**

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

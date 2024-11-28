---
title: Aspose.PSD CLI Convert for .NET 24.4 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI Convert for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**     | **요약**                                              | **카테고리** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Aspose.PSD CLI Convert 애플리케이션의 초기 릴리스 |  향상 |


## **사용 예시:**

**PSDNET-2023. Aspose.PSD CLI Convert 애플리케이션의 초기 릴리스**

**명령줄에서의 사용:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**코드에서의 사용:**

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

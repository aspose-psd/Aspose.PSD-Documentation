---
title: Aspose.PSD CLI Resize for .NET 24.4 - 릴리스 노트
type: docs
weight: 90
url: /ko/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD CLI Resize for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **Key**     | **Summary**                                          | **Category** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Aspose.PSD CLI Resize 어플리케이션의 최초 릴리스   |  개선사항 |

## **사용 예시:**

**PSDNET-2026. Aspose.PSD CLI Resize 어플리케이션의 최초 릴리스**

**커맨드 라인을 통한 사용 예시:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**코드를 통한 사용 예시:**

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

---
title: Aspose.PSD CLI Resize for .NET 24.4 - Release Notes
type: docs
weight: 90
url: /net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD CLI Resize for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Key**     | **Summary**                                          | **Category** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Initial release of Aspose.PSD CLI Resize Application |  Enhancement |


## **Usage examples:**

**PSDNET-2026. Initial release of Aspose.PSD CLI Resize Application**

**Usage from command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Usage from code:**

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
---
title: Aspose.PSD CLI Convert for .NET 24.4 - Release Notes
type: docs
weight: 90
url: /net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD CLI Convert for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Key**     | **Summary**                                              | **Category** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Initial release of Aspose.PSD CLI Convert Application |  Enhancement |


## **Usage examples:**

**PSDNET-2023. Initial release of Aspose.PSD CLI Convert Application**

**Usage from command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Usage from command code:**

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
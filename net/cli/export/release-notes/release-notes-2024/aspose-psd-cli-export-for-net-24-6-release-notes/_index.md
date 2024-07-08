```md
---
title: Aspose.PSD CLI Export for .NET 24.6 - Release Notes
type: docs
weight: 90
url: /net/cli/export/release-notes/aspose-psd-cli-export-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD CLI Export for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                 | **Category** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initial Release of Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export and Aspose.PSD.CLI.NLP.Editor |  Enhancement |


## **Usage examples:**

**PSDNET-2110. Initial release of Aspose.PSD CLI Export Application**

**Usage from command line:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Usage from code:**

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
```
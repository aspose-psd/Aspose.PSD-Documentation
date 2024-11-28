---
title: Aspose.PSD CLI Export for .NET 24.6 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Export for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/) için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                                 | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Editor |  Geliştirme |


## **Kullanım Örnekleri:**

**PSDNET-2110. Aspose.PSD CLI Export Uygulamasının İlk Sürümü**

**Komut satırından kullanım:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Koddan kullanım:**

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

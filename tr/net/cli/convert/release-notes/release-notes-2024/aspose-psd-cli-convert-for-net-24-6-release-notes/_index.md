---
title: Aspose.PSD CLI Convert for .NET 24.6 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD CLI Convert for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/) sürümü için yayın notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                                     | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Editor |  Geliştirme   |


## **Kullanım Örnekleri:**

**PSDNET-2110. Aspose.PSD CLI Uygulamalarının İlk Sürümü: Aspose.PSD.CLI.Export ve Aspose.PSD.CLI.NLP.Editor**

**Komut satırından kullanım:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Kod içerisinden kullanım:**

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

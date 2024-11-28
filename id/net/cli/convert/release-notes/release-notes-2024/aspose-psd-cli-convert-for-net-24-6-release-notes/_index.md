---
title: Catatan Rilis Aspose.PSD CLI Convert untuk .NET 24.6
type: docs
weight: 90
url: /id/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI Convert untuk .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                               | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilis Awal Aplikasi Aspose.PSD CLI: Aspose.PSD.CLI.Export dan Aspose.PSD.CLI.NLP.Editor  | Peningkatan  |


## **Contoh Penggunaan:**

**PSDNET-2110. Rilis Awal Aplikasi Aspose.PSD CLI: Aspose.PSD.CLI.Export dan Aspose.PSD.CLI.NLP.Editor**

**Penggunaan dari baris perintah:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Penggunaan dari kode perintah:**

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

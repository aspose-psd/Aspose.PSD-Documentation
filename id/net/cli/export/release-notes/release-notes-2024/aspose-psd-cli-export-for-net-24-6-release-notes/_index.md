---
title: Catatan Rilis Aspose.PSD CLI Ekspor untuk .NET 24.6
type: docs
weight: 90
url: /id/net/cli/ekspor/aplikasi-cli-aspose-psd-untuk-net-24-6-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI Ekspor untuk .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                 | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilis Awal Aplikasi Aspose.PSD CLI: Aspose.PSD.CLI.Export dan Aspose.PSD.CLI.NLP.Editor | Peningkatan |


## **Contoh Penggunaan:**

**PSDNET-2110. Rilis Awal Aplikasi Ekspor Aspose.PSD CLI**

**Penggunaan dari baris perintah:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Penggunaan dari kode:**


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

---
title: Catatan Rilis Aspose.PSD CLI Convert untuk .NET 24.4
type: docs
weight: 90
url: /id/net/cli/konversi/aspose-psd-konversi-cli-app-untuk-net-24-6-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI Convert untuk .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                | **Kategori** |
|:------------|:------------------------------------------------------------|:-------------|
| PSDNET-2023 | Rilis Awal Aplikasi Konversi Aspose.PSD CLI                 | Peningkatan  |


## **Contoh Penggunaan:**

**PSDNET-2023. Rilis Awal Aplikasi Konversi Aspose.PSD CLI**

**Penggunaan dari baris perintah:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input foto_1.jpg --output hasil.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Penggunaan dari kode perintah:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "foto_1.jpg", "foto_2.jpg", "foto_3.jpg", "foto_4.jpg", "foto_5.jpg", "foto_6.jpg" },
    OutputPath = "hasil.zip",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(options);
{{< /highlight >}}

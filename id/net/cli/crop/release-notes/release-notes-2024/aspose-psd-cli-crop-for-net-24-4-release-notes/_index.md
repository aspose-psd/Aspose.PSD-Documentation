---
title: Catatan Rilis Aspose.PSD CLI Crop untuk .NET 24.4
type: docs
weight: 90
url: /id/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI Crop untuk .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                         | **Kategori** |
|:------------|:------------------------------------------------------|:-------------|
| PSDNET-2025 | Rilis awal dari Aplikasi Pemangkasan Aspose.PSD CLI   | Peningkatan  |


## **Contoh Penggunaan:**

**PSDNET-2023. Rilis awal dari Aplikasi Pemangkasan Aspose.PSD CLI**

**Penggunaan dari baris perintah:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Penggunaan dari kode perintah:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

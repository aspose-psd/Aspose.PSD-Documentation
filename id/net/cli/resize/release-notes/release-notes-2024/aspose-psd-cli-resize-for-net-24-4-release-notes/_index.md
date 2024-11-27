---
title: Catatan Rilis Aspose.PSD CLI Resize untuk .NET 24.4
type: docs
weight: 90
url: /id/net/cli/resize/catatan-rilis/aspose-psd-cli-resize-untuk-net-24-4-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD CLI Resize untuk .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                 | **Kategori**  |
|:------------|:-------------------------------------------------------------|:--------------|
| PSDNET-2026 | Rilis awal Aplikasi Resize Aspose.PSD CLI                    | Peningkatan   |


## **Contoh Penggunaan:**

**PSDNET-2026. Rilis awal Aplikasi Resize Aspose.PSD CLI**

**Penggunaan dari baris perintah:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Penggunaan dari kode:**

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

---
title: Aspose.PSD CLI Crop pro .NET 24.4 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/crop/aspose-psd-cli-crop-pro-net-24-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI Crop pro .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                         | **Kategorie** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Počáteční vydání aplikace Aspose.PSD CLI Crop      | Vylepšení    |


## **Příklady použití:**

**PSDNET-2023. Počáteční vydání aplikace Aspose.PSD CLI Crop**

**Použití z příkazové řádky:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Použití z kódu:**

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

---
title: Notes de publication d'Aspose.PSD CLI Crop pour .NET 24.4
type: docs
weight: 90
url: /fr/net/cli/crop/aspose-psd-cli-crop-pour-net-24-4-notes-de-release/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD CLI Crop pour .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Clé**     | **Résumé**                                        | **Catégorie** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Première version de l'application Aspose.PSD CLI Crop | Amélioration |


## **Exemples d'utilisation:**

**PSDNET-2023. Première version de l'application Aspose.PSD CLI Crop**

**Utilisation à partir de la ligne de commande:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation à partir du code de commande:**

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

---
title: Aspose.PSD CLI Recadrage pour .NET 24.6 - Notes de publication
type: docs
weight: 90
url: /fr/psd/net/cli/recadrage/aspose-psd-recadrage-cli-app-pour-net-24-6-notes-de-publication/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD CLI Recadrage pour .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                                           | **Catégorie** |
|:------------|:--------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDNET-2110 | Première version des applications Aspose.PSD CLI: Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editor      |  Amélioration |

## **Exemples d'utilisation:**

**PSDNET-2110. Première version de l'application de recadrage Aspose.PSD CLI**

**Utilisation en ligne de commande:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation depuis le code de commande:**

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

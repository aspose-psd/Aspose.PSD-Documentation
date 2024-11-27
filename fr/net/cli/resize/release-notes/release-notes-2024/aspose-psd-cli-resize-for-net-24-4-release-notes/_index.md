---
title: Notes de version Aspose.PSD CLI Resize pour .NET 24.4
type: docs
weight: 90
url: /fr/net/cli/resize/notes-de-version/aspose-psd-cli-resize-pour-net-24-4-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD CLI Resize pour .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Clé**     | **Résumé**                                          | **Catégorie** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Première version de l'application de redimensionnement Aspose.PSD CLI |  Amélioration |


## **Exemples d'utilisation :**

**PSDNET-2026. Première version de l'application de redimensionnement Aspose.PSD CLI**

**Utilisation en ligne de commande :**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation depuis le code :**

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

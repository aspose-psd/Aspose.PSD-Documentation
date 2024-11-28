---
title: Notes de publication d'Aspose.PSD CLI Convert pour .NET 24.4
type: docs
weight: 90
url: /fr/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD CLI Convert pour .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Clé**     | **Résumé**                                            | **Catégorie** |
|:------------|:------------------------------------------------------|:-------------|
| PSDNET-2023 | Version initiale de l'application Aspose.PSD CLI Convert |  Amélioration |


## **Exemples d'utilisation :**

**PSDNET-2023. Version initiale de l'application Aspose.PSD CLI Convert**

**Utilisation en ligne de commande :**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation depuis le code :**

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

---
title: Aspose.PSD CLI Export for .NET 24.6 - Notes de version
type: docs
weight: 90
url: /fr/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD CLI Export for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                 | **Catégorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Première version des applications CLI Aspose.PSD : Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editor |  Amélioration |


## **Exemples d'utilisation:**

**PSDNET-2110. Première version de l'application CLI d'export Aspose.PSD**

**Utilisation depuis la ligne de commande:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation depuis le code :**

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

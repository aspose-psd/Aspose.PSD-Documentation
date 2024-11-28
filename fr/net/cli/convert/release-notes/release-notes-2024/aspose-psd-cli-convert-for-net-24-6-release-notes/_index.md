---
title: Notes de version de Aspose.PSD CLI Convert pour .NET 24.6
type: docs
weight: 90
url: /fr/net/cli/convert/aspose-psd-cli-convert-pour-net-24-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD CLI Convert pour .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                   | **Catégorie** |
|:------------|:---------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Version initiale des applications Aspose.PSD CLI : Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editor |  Amélioration |


## **Exemples d'utilisation:** 

**PSDNET-2110. Version initiale des applications Aspose.PSD CLI : Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editor**

**Utilisation en ligne de commande:** 

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilisation à partir du code source:** 

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

---
title: Notes de publication de Aspose.PSD CLI Resize pour .NET 24.6
type: docs
weight: 90
url: /fr/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD CLI Resize pour .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                      | **Catégorie** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Version initiale des applications Aspose.PSD CLI : Aspose.PSD.CLI.Export et Aspose.PSD.CLI.NLP.Editor |  Amélioration |


## **Exemples d'utilisation :**

**PSDNET-2110. Version initiale de l'application Aspose.PSD CLI Resize**

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

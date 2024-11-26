---
title: Aspose.PSD CLI Export voor .NET 24.6 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI Export voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                              | **Categorie** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initiële release van Aspose.PSD CLI-apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor |  Verbetering   |


## **Gebruik voorbeelden:**

**PSDNET-2110. Initiële release van de Aspose.PSD CLI Export-applicatie**

**Gebruik vanaf de opdrachtregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanaf de code:**

{{< highlight csharp >}}

var opties = nieuwe Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PadNaarInputAfbeelding = "photo1.jpg",
    PadNaarUitvoerAfbeelding = "exported.png",
    Uitvoerformaat = "png",
    Laagnaam = "Layer1"
};


if (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Toepassen(opties);

{{< /highlight >}}

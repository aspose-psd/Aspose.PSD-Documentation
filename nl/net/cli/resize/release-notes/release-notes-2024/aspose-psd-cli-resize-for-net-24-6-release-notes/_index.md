---
title: Aspose.PSD CLI Formaat wijzigen voor .NET 24.6 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/cli/resize/aspose-psd-formaat-wijzigen-cli-app-voor-net-24-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI Formaat wijzigen voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                            | **Categorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initiële vrijgave van Aspose.PSD CLI-apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor | Uitbreiding   |


## **Gebruik voorbeelden:**

**PSDNET-2110. Initiële vrijgave van Aspose.PSD CLI Formaat wijzigen Applicatie**

**Gebruik vanaf de commandoregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input foto1.jpg --output aangepast.png --breedte 200 --hoogte 340 --formaat png --licentie Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanaf de code:**

{{< highlight csharp >}}

var opties = nieuwe Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PadNaarInvoerAfbeelding = "foto1.jpg",
    PadNaarUitvoerAfbeelding = "aangepast.png",
    Schaal = 200,
    Uitvoerformaat = "png"
};


als (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Toepassen(opties);

{{< /highlight >}}

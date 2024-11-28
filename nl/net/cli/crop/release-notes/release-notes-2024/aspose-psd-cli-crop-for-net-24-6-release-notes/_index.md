---
title: Aspose.PSD CLI Bijsnijden voor .NET 24.6 - Release-opmerkingen
type: docs
weight: 90
url: /psd/nl/net/cli/bijsnijden/aspose-psd-bijsnijd-cli-app-voor-net-24-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI Bijsnijden voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                              | **Categorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Initiële release van Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor |  Verbetering |

## **Gebruik voorbeelden:**

**PSDNET-2110. Initiële release van de Aspose.PSD CLI Bijsnijd toepassing**

**Gebruik vanaf de commandoregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Bijsnijden --input foto1.jpg --output bijgesneden_foto.png --formaat png --links 10 --boven 35 --breedte 250 --hoogte 300 --bijsnijdType rechthoekig --licentie Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanaf de code in de opdracht:**

{{< highlight csharp >}}
var opties = nieuwe Aspose.PSD.CLI.CommandLineOpties.BijsnijdOpties
{
    InputPad = "foto1.jpg",
    BijsnijdType = BijsnijdType.Rechthoek,
    Links = 10,
    Boven = 35,
    Breedte = 250,
    Hoogte = 300,
    OutputPad = "bijgesneden_foto.png",
    OutputFormaat = "png"
};


if (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Bijsnijden.Toepassen(opties);
{{< /highlight >}}

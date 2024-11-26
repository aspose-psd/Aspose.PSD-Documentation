---
title: Aspose.PSD CLI Converteren voor .NET 24.4 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/cli/conversie/aspose-psd-converter-cli-app-voor-net-24-6-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI Converteren voor .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                         | **Categorie** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Eerste release van de Aspose.PSD CLI Converteren Applicatie |  Verbetering |


## **Gebruik voorbeelden:**

**PSDNET-2023. Eerste release van de Aspose.PSD CLI Converteren Applicatie**

**Gebruik vanaf de opdrachtregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input foto_1.jpg --output resultaat.zip --indeling png --licentie Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanuit de code:**

{{< highlight csharp >}}
var opties = nieuw Aspose.PSD.CLI.Convert.CommandLineOptions.ConversieOpties
{
    InvoerBestanden = nieuw List<string> { "foto_1.jpg", "foto_2.jpg", "foto_3.jpg", "foto_4.jpg", "foto_5.jpg", "foto_6.jpg" },
    UitvoerPad = "resultaat.zip",
    UitvoerFormaat = "png"
};


if (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Toepassen(opties);
{{< /highlight >}}

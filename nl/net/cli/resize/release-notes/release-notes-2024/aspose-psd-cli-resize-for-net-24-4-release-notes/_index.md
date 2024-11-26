---
title: Aspose.PSD CLI Formaat wijzigen voor .NET 24.4 - Release-opmerkingen
type: docs
weight: 90
url: /nl/net/cli/formaat-wijzigen/release-opmerkingen/aspose-psd-cli-formaat-wijzigen-voor-net-24-4-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD CLI Formaat wijzigen voor .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                     | **Categorie** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Initiële uitgave van de Aspose.PSD CLI Formaat wijzigen toepassing |  Verbetering |


## **Gebruik voorbeelden:**

**PSDNET-2026. Initiële uitgave van de Aspose.PSD CLI Formaat wijzigen toepassing**

**Gebruik vanaf de commandoregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanuit code:**

{{< highlight csharp >}}

var opties = nieuwe Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PadNaarInputAfbeelding = "photo1.jpg",
    PadNaarOutputAfbeelding = "resized.png",
    Schaal = 200,
    UitvoerFormaat = "png"
};


als (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Toepassen(opties);

{{< /highlight >}}

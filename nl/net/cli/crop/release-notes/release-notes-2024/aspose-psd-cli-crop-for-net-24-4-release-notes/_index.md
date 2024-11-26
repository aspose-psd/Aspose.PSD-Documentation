---
title: Aspose.PSD CLI Bijwerken voor .NET 24.4 - Versieopmerkingen
type: docs
weight: 90
url: /nl/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat versieopmerkingen voor [Aspose.PSD CLI Bijwerken voor .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                   | **Categorie** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Initiële release van de Aspose.PSD CLI Bijwerktoepassing |  Verbetering |


## **Gebruik voorbeelden:**

**PSDNET-2023. Initiële release van de Aspose.PSD CLI Bijwerktoepassing**

**Gebruik vanaf de opdrachtregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Bijwerken --input foto1.jpg --output bijgewerkte_foto.png --formaat png --links 10 --boven 35 --breedte 250 --hoogte 300 --bijwerktType rechthoek --licentie Aspose.PSD.Product.Familie.lic
{{< /highlight >}}

**Gebruik vanaf de opdrachtcode:**

{{< highlight csharp >}}
var opties = new Aspose.PSD.CLI.CommandLineOptions.BijwerkOpties
{
    InputPad = "foto1.jpg",
    BijwerkType = BijwerkType.Rechthoek,
    Links = 10,
    Boven = 35,
    Breedte = 250,
    Hoogte = 300,
    OutputPad = "bijgewerkte_foto.png",
    OutputFormaat = "png"
};


if (isGelicentieerd)
{
    opties.LicentiePad = "Aspose.PSD.Product.Familie.lic";
}

Aspose.PSD.CLI.Bijwerken.Toepassen(opties);
{{< /highlight >}}

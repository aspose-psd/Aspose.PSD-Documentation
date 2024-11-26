---
title: Aspose.PSD CLI Convert voor .NET 24.6 - Releasedocumenten
type: docs
weight: 90
url: /nl/net/cli/convert/aspose-psd-cli-convert-voor-net-24-6-releasedocumenten/
---

{{% alert color="primary" %}}

Deze pagina bevat de releasedocumenten voor [Aspose.PSD CLI Convert voor .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Sleutel** | **Samenvatting**                                                                              | **Categorie** |
|:------------|:----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Eerste release van Aspose.PSD CLI-apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor | Verbetering   |


## **Gebruikvoorbeelden:**

**PSDNET-2110. Eerste release van Aspose.PSD CLI-apps: Aspose.PSD.CLI.Export en Aspose.PSD.CLI.NLP.Editor**

**Gebruik vanaf de commandoregel:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Gebruik vanuit coderegels:**

{{< highlight csharp >}}
var opties = nieuwe Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputBestanden = nieuwe List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    Uitvoerpad = "result.zip",
    Uitvoerformaat = "png"
};


if (isGelicentieerd)
{
    opties.Licentiepad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Toepassen(opties);
{{< /highlight >}}

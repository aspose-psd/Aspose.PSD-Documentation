---
title: Aspose.PSD CLI Convert pro .NET 24.6 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/convert/aspose-psd-cli-convert-pro-net-24-6-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI Convert pro .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Klíč**    | **Souhrn**                                                                                  | **Kategorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Počáteční vydání Aspose.PSD CLI aplikací: Aspose.PSD.CLI.Export a Aspose.PSD.CLI.NLP.Editor |  Vylepšení   |


## **Příklady použití:**

**PSDNET-2110. Počáteční vydání Aspose.PSD CLI aplikací: Aspose.PSD.CLI.Export and Aspose.PSD.CLI.NLP.Editor**

**Použití z příkazové řádky:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Použití z kódu:**

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

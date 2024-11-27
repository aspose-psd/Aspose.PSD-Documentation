---
title: Vydání poznámek pro Aspose.PSD CLI Convert pro .NET 24.4
type: docs
weight: 90
url: /cs/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Tato stránka obsahuje vydání poznámek pro [Aspose.PSD CLI Convert pro .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                              | **Kategorie** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Počáteční vydání aplikace Aspose.PSD CLI Convert |  Vylepšení |


## **Příklady použití:**

**PSDNET-2023. Počáteční vydání aplikace Aspose.PSD CLI Convert**

**Použití z příkazového řádku:**

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

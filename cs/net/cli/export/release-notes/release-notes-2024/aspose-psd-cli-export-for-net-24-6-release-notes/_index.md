---
title: Aspose.PSD CLI Export pro .NET 24.6 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI Export pro .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                 | **Kategorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Počáteční vydání aplikací Aspose.PSD CLI: Aspose.PSD.CLI.Export a Aspose.PSD.CLI.NLP.Editor |  Vylepšení |


## **Příklady použití:**

**PSDNET-2110. Počáteční vydání aplikace Aspose.PSD CLI Export**

**Použití z příkazové řádky:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Použití z kódu:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    CestaKVstupnímuObrázku = "photo1.jpg",
    CestaKVýstupnímuObrázku = "exported.png",
    FormátVýstupu = "png",
    NázevVrstvy = "Layer1"
};


if (jeLicencováno)
{
    options.CestaKLicenci = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Použít(opce);

{{< /highlight >}}

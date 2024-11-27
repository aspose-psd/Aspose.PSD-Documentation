---
title: Aspose.PSD CLI Změna velikosti pro .NET 24.6 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI Změna velikosti pro .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                   | **Kategorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Počáteční verze aplikací Aspose.PSD CLI: Aspose.PSD.CLI.Export a Aspose.PSD.CLI.NLP.Editor |  Vylepšení    |


## **Příklady použití:**

**PSDNET-2110. Počáteční vydání aplikace Aspose.PSD CLI Změna velikosti**

**Použití z příkazové řádky:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Použití z kódu:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

---
title: Aspose.PSD CLI Změna velikosti pro .NET 24.4 - Poznámky k vydání
type: docs
weight: 90
url: /cs/net/cli/resize/release-notes/aspose-psd-cli-resize-pro-net-24-4-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD CLI Změnu velikosti pro .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                          | **Kategorie** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | První vydání aplikace Aspose.PSD CLI Změna velikosti | Vylepšení |


## **Příklady použití:**

**PSDNET-2026. První vydání aplikace Aspose.PSD CLI Změna velikosti**

**Použití z příkazového řádku:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Použití z kódu:**

{{< highlight csharp >}}

var možnosti = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    CestaKoVstupníObrázek = "photo1.jpg",
    CestaKoVýstupníObrázek = "resized.png",
    Měřítko = 200,
    VýstupníFormát = "png"
};


jestliže (jeLicencován)
{
    možnosti.CestaKeLicenci = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(možnosti);

{{< /highlight >}}

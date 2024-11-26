---
title: Notatki wydania Aspose.PSD CLI Resize dla .NET 24.4
type: docs
weight: 90
url: /pl/net/cli/resize/notatki-o-wydaniu/aspose-psd-cli-resize-for-net-24-4-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD CLI Resize dla .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                          | **Kategoria** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Pierwsze wydanie aplikacji Aspose.PSD CLI Resize |  Ulepszenie |


## **Przykłady użycia:**

**PSDNET-2026. Pierwsze wydanie aplikacji Aspose.PSD CLI Resize**

**Użycie z wiersza poleceń:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input zdjecie1.jpg --output zmniejszone.png --szerokosc 200 --wysokosc 340 --format png --licencja Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu:**

{{< highlight csharp >}}

var opcje = nowe Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    SciezkaDoZdjeciaWejsciowego = "zdjecie1.jpg",
    SciezkaDoZdjeciaWyjsciowego = "zmniejszone.png",
    Skala = 200,
    FormatWyjscia = "png"
};


if (jestZarejestrowany)
{
    opcje.SciezkaDoLicencji = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(opcje);

{{< /highlight >}}

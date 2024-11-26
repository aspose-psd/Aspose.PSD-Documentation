---
title: Aspose.PSD CLI Eksport dla .NET 24.6 - Notatki Wydania
type: docs
weight: 90
url: /pl/net/cli/eksport/aspose-psd-eksport-cli-aplikacja-dla-net-24-6-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD CLI Eksport dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Klucz**   | **Podsumowanie**                                                                               | **Kategoria** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Pierwsze Wydanie Aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor |  Ulepszenie    |


## **Przykłady Użycia:**

**PSDNET-2110. Pierwsze wydanie Aplikacji Aspose.PSD CLI Eksport**

**Użycie z linii komend:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input zdjecie1.jpg --output wyeksportowane.png --format png --nazwaWarstwy Warstwa1 --licencja Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu:**

{{< highlight csharp >}}

var opcje = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    SciezkaDoZdjeciaWejsciowego = "zdjecie1.jpg",
    SciezkaDoZdjeciaWyjsciowego = "wyeksportowane.png",
    FormatWyjsciowy = "png",
    NazwaWarstwy = "Warstwa1"
};


if (posiadaLicencje)
{
    opcje.SciezkaDoLicencji = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(opcje);

{{< /highlight >}}

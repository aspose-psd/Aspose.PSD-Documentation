---
title: Aspose.PSD CLI Zmień rozmiar dla .NET 24.6 - Notatki wydania
type: docs
weight: 90
url: /pl/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD CLI Zmień rozmiar dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Klucz**     | **Podsumowanie**                                                                              | **Kategoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Pierwsze wydanie aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor | Wzbogacenie   |


## **Przykłady użycia:**

**PSDNET-2110. Pierwsze wydanie aplikacji Aspose.PSD CLI Zmień rozmiar**

**Użycie z wiersza poleceń:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu:** 

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

---
title: Aspose.PSD CLI Convert dla .NET 24.6 - Informacje o wydaniu
type: docs
weight: 90
url: /pl/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ta strona zawiera informacje o wydaniu [Aspose.PSD CLI Convert dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                              | **Kategoria** |
|:------------|:-----------------------------------------------------------------------------------------------|:--------------|
| PSDNET-2110 | Pierwsze wydanie aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor | Wzbogacenie   |


## **Przykłady użycia:**

**PSDNET-2110. Pierwsze wydanie aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor**

**Użycie z wiersza poleceń:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu:**

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

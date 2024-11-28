---
title: Aspose.PSD CLI Przycinanie dla .NET 24.6 - Notatki wydania
type: docs
weight: 90
url: /psd/pl/net/cli/przycinanie/aspose-psd-przytnij-cli-dla-net-24-6-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD CLI Przycinanie dla .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                            | **Kategoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Wersja początkowa aplikacji Aspose.PSD CLI: Aspose.PSD.CLI.Export i Aspose.PSD.CLI.NLP.Editor | Usprawnienie |


## **Przykłady użycia:**

**PSDNET-2110. Wersja początkowa aplikacji Aspose.PSD CLI Przycinanie**

**Użycie z wiersza poleceń:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

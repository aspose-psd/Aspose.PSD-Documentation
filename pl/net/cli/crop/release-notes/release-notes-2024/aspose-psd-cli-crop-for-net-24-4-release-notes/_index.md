---
title: Aspose.PSD CLI Przycinanie dla .NET 24.4 - Notatki o wydaniu
type: docs
weight: 90
url: /pl/net/cli/przycinanie/aspose-psd-cli-przycinanie-dla-net-24-4-notatki-o-wydaniu/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki o wydaniu [Aspose.PSD CLI Przycinanie dla .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Klucz**   | **Podsumowanie**                                          | **Kategoria** |
|:-----------|:----------------------------------------------------------|:--------------|
| PSDNET-2025 | Wprowadzenie Aspose.PSD CLI Przycinania do Aplikacji CLI  | Wzmacnianie  |


## **Przykłady użycia:**

**PSDNET-2023. Wprowadzenie Aspose.PSD CLI Przycinania do Aplikacji CLI**

**Użycie z wiersza poleceń:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Użycie z kodu źródłowego:**

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

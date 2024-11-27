---
title: Примітки до випуску Aspose.PSD CLI Crop для .NET 24.6
type: docs
weight: 90
url: /psd/uk/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску для [Aspose.PSD CLI Crop для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                                                   | **Категорія** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Початковий випуск програм Aspose.PSD CLI: Aspose.PSD.CLI.Export та Aspose.PSD.CLI.NLP.Editor | Покращення   |


## **Приклади використання:**

**PSDNET-2110. Початковий випуск додатка Aspose.PSD CLI Crop**

**Використання з командного рядка:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Використання з коду командного рядка:**

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

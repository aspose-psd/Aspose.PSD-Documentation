---
title: Aspose.PSD CLI Обрізка для .NET 24.4 - Примітки до випуску
type: docs
weight: 90
url: /uk/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску для [Aspose.PSD CLI Обрізки для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**     | **Зміст**                                          | **Категорія** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Початковий випуск додатка Aspose.PSD CLI для обрізки  | Покращення |


## **Приклади використання:**

**PSDNET-2023. Початковий випуск додатка Aspose.PSD CLI для обрізки**

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

---
title: Aspose.PSD CLI Обрезка для .NET 24.4 - Примечания к выпуску
type: docs
weight: 90
url: /ru/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску для [Aspose.PSD CLI Обрезки для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**     | **Краткое описание**                                | **Категория** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Первый релиз приложения Aspose.PSD CLI Обрезки |  Улучшение |

## **Примеры использования:**

**PSDNET-2023. Первый релиз приложения Aspose.PSD CLI Обрезки**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование из кода командной строки:**

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

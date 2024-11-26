---
title: Aspose.PSD CLI Обрезать для .NET 24.6 - Примечания к выпуску
type: docs
weight: 90
url: /ru/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к выпуску для [Aspose.PSD CLI Crop для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**    | **Описание**                                                                           | **Категория** |
|:------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Первый выпуск приложений Aspose.PSD CLI: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor | Улучшение |

## **Примеры использования:**

**PSDNET-2110. Первый выпуск приложения Aspose.PSD CLI Crop**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование из кода:**

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

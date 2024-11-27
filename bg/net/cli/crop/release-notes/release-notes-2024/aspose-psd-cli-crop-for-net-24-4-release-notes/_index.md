---
title: Aspose.PSD CLI Отрязва за .NET 24.4 - Бележки към версията
type: docs
weight: 90
url: /bg/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към версията за [Aspose.PSD CLI Отрязва за .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**     | **Резюме**                                        | **Категория** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | Първоначално пускане на Aspose.PSD CLI Отрязва Приложение |  Подобрение |


## **Примери за използване:**

**PSDNET-2023. Първоначално пускане на Aspose.PSD CLI Отрязва Приложение**

**Използване от командния ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване от команден код:**

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

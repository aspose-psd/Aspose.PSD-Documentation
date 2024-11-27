---
title: Aspose.PSD CLI Изрязване за .NET 24.6 - Бележки за версията
type: docs
weight: 90
url: /bg/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD CLI Изрязване за .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Ключ**     | **Обобщение**                                                                                 | **Категория** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Първоначално пускане на Aspose.PSD CLI приложения: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor |  Подобрение |


## **Примери за използване:**

**PSDNET-2110. Първоначално пускане на приложението за изрязване с Aspose.PSD CLI**

**Използване от командният ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване от код на командния ред:**

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

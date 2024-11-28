---
title: Aspose.PSD CLI Convert для .NET 24.4 - Примітки до випуску
type: docs
weight: 90
url: /uk/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску для [Aspose.PSD CLI Convert для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                 | **Категорія** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Початковий випуск додатку Aspose.PSD CLI Convert | Покращення |


## **Приклади використання:**

**PSDNET-2023. Початковий випуск додатку Aspose.PSD CLI Convert**

**Використання з командного рядка:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Використання з коду команд:**

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

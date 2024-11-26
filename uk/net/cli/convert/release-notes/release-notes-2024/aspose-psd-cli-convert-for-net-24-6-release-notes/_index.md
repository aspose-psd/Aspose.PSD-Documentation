---
title: Основний Підш"шдр Aspose.PSD CLI для .NET 24.6 - Інформація про випуск
type: docs
weight: 90
url: /uk/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить замітки про випуск [Aspose.PSD CLI Convert для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                                                   | **Категорія** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Початковий випуск додатків Aspose.PSD CLI: Aspose.PSD.CLI.Export та Aspose.PSD.CLI.NLP.Editor | Поліпшення |

## **Приклади використання:**

**PSDNET-2110. Початковий випуск додатків Aspose.PSD CLI: Aspose.PSD.CLI.Export та Aspose.PSD.CLI.NLP.Editor**

**Використання з командного рядка:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Використання з коду команди:**

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

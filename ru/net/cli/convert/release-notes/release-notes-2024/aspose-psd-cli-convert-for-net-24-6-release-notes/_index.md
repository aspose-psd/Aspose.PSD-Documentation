---
title: Aspose.PSD CLI Convert для .NET 24.6 - Примечания к выпуску
type: docs
weight: 90
url: /ru/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску для [Aspose.PSD CLI Convert для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**     | **Краткое содержание**                                                                             | **Категория** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Первый выпуск приложений Aspose.PSD CLI: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor |  Улучшение |


## **Примеры использования:**

**PSDNET-2110. Первый выпуск приложений Aspose.PSD CLI: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование из кода:**

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

---
title: Заметки о выпуске Aspose.PSD CLI Convert для .NET 24.4
type: docs
weight: 90
url: /ru/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся заметки о выпуске [Aspose.PSD CLI Convert для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                      | **Категория** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Первый выпуск приложения CLI Convert для Aspose.PSD   |  Улучшение |


## **Примеры использования:**

**PSDNET-2023. Первый выпуск приложения CLI Convert для Aspose.PSD**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование из кода команды:**

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

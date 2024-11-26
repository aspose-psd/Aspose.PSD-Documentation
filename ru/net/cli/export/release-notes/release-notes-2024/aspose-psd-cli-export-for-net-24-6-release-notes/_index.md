---
title: Релизные заметки Aspose.PSD CLI Export для .NET 24.6
type: docs
weight: 90
url: /ru/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит релизные заметки для [Aspose.PSD CLI Export для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                                  | **Категория** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Первый релиз приложений Aspose.PSD CLI: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor | Улучшение |


## **Примеры использования:**

**PSDNET-2110. Первый релиз приложения Aspose.PSD CLI Export**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование в коде:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "exported.png",
    OutputFormat = "png",
    LayerName = "Layer1"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(options);

{{< /highlight >}}

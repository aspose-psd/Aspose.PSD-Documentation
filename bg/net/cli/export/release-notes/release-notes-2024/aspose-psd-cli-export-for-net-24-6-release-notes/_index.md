---
title: Aspose.PSD CLI Експорт за .NET 24.6 - Забележки за изданието
type: docs
weight: 90
url: /bg/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки за изданието на [Aspose.PSD CLI Експорт за .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Ключ**     | **Резюме**                                                                                   | **Категория** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Първоначално издание на Aspose.PSD CLI Приложенията: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor |  Подобрение |


## **Примери за използване:**

**PSDNET-2110. Първоначално издание на приложението за експорт на Aspose.PSD CLI**

**Използване от командния ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване от кода:**

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

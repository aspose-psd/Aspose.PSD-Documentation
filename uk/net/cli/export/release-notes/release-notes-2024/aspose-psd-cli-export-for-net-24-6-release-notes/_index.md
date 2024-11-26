---
title: Оголошення про версію Aspose.PSD CLI Export для .NET 24.6
type: docs
weight: 90
url: /uk/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить оголошення про версію [Aspose.PSD CLI Export для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Ключ**    | **Зміст**                                                                                   | **Категорія** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Початковий реліз додатків Aspose.PSD CLI: Aspose.PSD.CLI.Export і Aspose.PSD.CLI.NLP.Editor | Покращення   |


## **Приклади використання:**

**PSDNET-2110. Початковий реліз додатку Aspose.PSD CLI Export**

**Використання з командного рядка:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Використання через код:**

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

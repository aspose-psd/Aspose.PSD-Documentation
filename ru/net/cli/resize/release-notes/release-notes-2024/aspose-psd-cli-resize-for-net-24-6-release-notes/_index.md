---
title: Релизные заметки Aspose.PSD CLI Resize для .NET 24.6
type: docs
weight: 90
url: /ru/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

На данной странице содержатся релизные заметки для [Aspose.PSD CLI Resize для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Ключ**     | **Описание**                                                                                 | **Категория** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Начальный релиз Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor |  Улучшение |


## **Примеры использования:**

**PSDNET-2110. Начальный релиз приложения Aspose.PSD CLI для изменения размера изображения**

**Использование из командной строки:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Использование из кода:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

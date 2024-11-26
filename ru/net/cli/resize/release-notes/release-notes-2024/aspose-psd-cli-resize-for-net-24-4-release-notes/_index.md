---
title: Руководство по выпуску Aspose.PSD CLI Resize для .NET 24.4
type: документация
weight: 90
url: /ru/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит заметки к выпуску [Aspose.PSD CLI Resize для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Ключ**     | **Краткое описание**                                | **Категория** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Первый выпуск приложения Aspose.PSD CLI Resize      |  Улучшение   |


## **Примеры использования:**

**PSDNET-2026. Первый выпуск приложения Aspose.PSD CLI Resize**

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

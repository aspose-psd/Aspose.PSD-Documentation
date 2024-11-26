---
title: Оновлення Aspose.PSD CLI Resize для .NET 24.6
type: docs
weight: 90
url: /uk/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить оновлення для [Aspose.PSD CLI Resize для .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                                                   | **Категорія** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Початкове випуск програм Aspose.PSD CLI: Aspose.PSD.CLI.Export та Aspose.PSD.CLI.NLP.Editor | Покращення |

## **Приклади використання:**

**PSDNET-2110. Початковий реліз Aspose.PSD CLI Resize Application**

**Використання з командного рядка:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Використання з коду:**

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

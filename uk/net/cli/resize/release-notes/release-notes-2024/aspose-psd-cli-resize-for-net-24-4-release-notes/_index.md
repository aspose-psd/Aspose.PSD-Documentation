---
title: Опис випуску Aspose.PSD CLI Resize для .NET 24.4
type: docs
weight: 90
url: /uk/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить опис випуску для [Aspose.PSD CLI Resize для .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                      | **Категорія** |
|:------------|:------------------------------------------------------------|:-------------|
| PSDNET-2026 | Початковий випуск застосунка Aspose.PSD CLI Resize          | Покращення   |


## **Приклади використання:**

**PSDNET-2026. Початковий випуск застосунка Aspose.PSD CLI Resize**

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

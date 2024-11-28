---
title: Aspose.PSD CLI Resize for .NET 24.4 - Бележки за версията
type: docs
weight: 90
url: /bg/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD CLI Resize for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Ключ**     | **Резюме**                                          | **Категория** |
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | Първоначално пускане на приложението Aspose.PSD CLI Resize | Подобрение |


## **Примери за използване:**

**PSDNET-2026. Първоначално пускане на приложението Aspose.PSD CLI Resize**

**Използване от командния ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване от кода:**

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

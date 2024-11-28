---
title: Aspose.PSD CLI Convert за .NET 24.4 - Изтриване на версията
type: docs
weight: 90
url: /bg/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за версията на [Aspose.PSD CLI Convert за .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**    | **Резюме**                                                 | **Категория** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Първоначално издание на Aspose.PSD CLI Convert приложение | Подобрение   |


## **Примери за използване:**

**PSDNET-2023. Първоначално издание на приложението Aspose.PSD CLI Convert** 

**Използване от командния ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване в кода:**

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

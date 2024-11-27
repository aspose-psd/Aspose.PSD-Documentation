---
title: Aspose.PSD CLI Convert за .NET 24.6 - Забележки за изданието
type: docs
weight: 90
url: /bg/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки за изданието на [Aspose.PSD CLI Convert за .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Ключ**    | **Обобщение**                                                                                   | **Категория** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Първоначално пускане на Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export and Aspose.PSD.CLI.NLP.Editor | Подобрение    |


## **Примери за използване:**

**PSDNET-2110. Първоначално пускане на Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export и Aspose.PSD.CLI.NLP.Editor**

**Използване от командния ред:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Използване от кода на командата:**

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

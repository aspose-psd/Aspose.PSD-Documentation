---
title: Notas da Versão do Aspose.PSD CLI Convert para .NET 24.6
type: docs
weight: 90
url: /pt/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas da versão para [Aspose.PSD CLI Convert para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                    | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lançamento Inicial dos Aplicativos Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Aprimoramento |


## **Exemplos de Utilização:**

**PSDNET-2110. Lançamento Inicial dos Aplicativos Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor**

**Utilização a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilização a partir de código de comando:**

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

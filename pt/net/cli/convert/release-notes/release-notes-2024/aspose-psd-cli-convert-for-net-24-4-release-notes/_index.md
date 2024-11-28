---
title: Aspose.PSD CLI Converter for .NET 24.4 - Notas de Lançamento
type: docs
weight: 90
url: /pt/net/cli/conversao/aplicativo-cli-aspose-psd-para-net-24-6-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD CLI Converter for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                     | **Categoria** |
|:------------|:--------------------------------------------------------------|:-------------|
| PSDNET-2023 | Lançamento inicial do Aplicativo de Conversão Aspose.PSD CLI | Aprimoramento |


## **Exemplos de Uso:**

**PSDNET-2023. Lançamento inicial do Aplicativo de Conversão Aspose.PSD CLI**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código da aplicação:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    ArquivosDeEntrada = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    CaminhoDeSaida = "result.zip",
    FormatoDeSaida = "png"
};


if (estaLicenciado)
{
    options.CaminhoDaLicenca = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(options);
{{< /highlight >}}

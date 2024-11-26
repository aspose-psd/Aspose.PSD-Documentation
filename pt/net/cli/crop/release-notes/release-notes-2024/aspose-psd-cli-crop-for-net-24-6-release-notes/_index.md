---
title: Aspose.PSD CLI Crop para .NET 24.6 - Notas da Versão
type: docs
weight: 90
url: /pt/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas da versão para [Aspose.PSD CLI Crop para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                  | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lançamento Inicial dos Aplicativos Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Aprimoramento |

## **Exemplos de Uso:**

**PSDNET-2110. Lançamento Inicial do Aplicativo Aspose.PSD CLI Crop**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input foto1.jpg --output foto_cortada.png --format png --esquerda 10 --topo 35 --largura 250 --altura 300 --tipoCorte retângulo --licença Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código de comando:**

{{< highlight csharp >}}
var opções = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "foto1.jpg",
    CropType = CropType.Rect,
    Esquerda = 10,
    Topo = 35,
    Largura = 250,
    Altura = 300,
    OutputPath = "foto_cortada.png",
    FormatoSaida = "png"
};

if (licenciado)
{
    opções.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(opções);
{{< /highlight >}}

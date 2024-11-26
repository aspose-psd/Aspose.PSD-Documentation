---
title: Notas da Versão - Aspose.PSD CLI Crop para .NET 24.4
type: docs
weight: 90
url: /pt/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contém as notas da versão para [Aspose.PSD CLI Crop para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Chave**   | **Resumo**                                          | **Categoria**  |
|:------------|:----------------------------------------------------|:--------------|
| PSDNET-2025 | Lançamento inicial do Aplicativo de Corte Aspose.PSD CLI | Aprimoramento |


## **Exemplos de Uso:**

**PSDNET-2023. Lançamento inicial do Aplicativo de Corte Aspose.PSD CLI**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input foto1.jpg --output foto_cortada.png --format png --esquerda 10 --topo 35 --largura 250 --altura 300 --tipoCorte retangulo --licenca Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código de comando:**

{{< highlight csharp >}}
var opcoes = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    CaminhoEntrada = "foto1.jpg",
    TipoCorte = CropType.Rect,
    Esquerda = 10,
    Topo = 35,
    Largura = 250,
    Altura = 300,
    CaminhoSaida = "foto_cortada.png",
    FormatoSaida = "png"
};

if (possuiLicenca)
{
    opcoes.CaminhoLicenca = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Aplicar(opcoes);
{{< /highlight >}}

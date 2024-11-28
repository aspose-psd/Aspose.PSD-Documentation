---
title: Aspose.PSD CLI Redimensionar para .NET 24.4 - Notas de Lançamento
type: docs
weight: 90
url: /pt/net/cli/redimensionar/notas-de-lancamento/aspose-psd-cli-redimensionar-para-net-24-4-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém as notas de lançamento para [Aspose.PSD CLI Redimensionar para .NET 24.4] (https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Chave**   | **Resumo**                                            | **Categoria** |
|:------------|:------------------------------------------------------|:-------------|
| PSDNET-2026 | Lançamento inicial do Aplicativo de Redimensionamento Aspose.PSD CLI | Aprimoramento |

## **Exemplos de Uso:**

**PSDNET-2026. Lançamento inicial do Aplicativo de Redimensionamento Aspose.PSD CLI**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input foto1.jpg --output redimensionada.png --largura 200 --altura 340 --formato png --licença Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código:**

{{< highlight csharp >}}

var opções = novo Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    CaminhoParaImagemDeEntrada = "foto1.jpg",
    CaminhoParaImagemDeSaida = "redimensionada.png",
    Escala = 200,
    FormatoDeSaída = "png"
};

Se (comLicença)
{
    opções.CaminhoDeLicença = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Aplicar(opções);

{{< /highlight >}}

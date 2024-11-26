---
title: Notas da Versão Aspose.PSD CLI Resize para .NET 24.6
type: docs
weight: 90
url: /pt/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD CLI Resize para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                 | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lançamento Inicial das Aplicações Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Aperfeiçoamento |


## **Exemplos de Uso:**

**PSDNET-2110. Lançamento Inicial da Aplicação Aspose.PSD CLI Resize**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código:**

{{< highlight csharp >}}

var opções = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    CaminhoParaImagemDeEntrada = "photo1.jpg",
    CaminhoParaImagemDeSaída = "resized.png",
    Escala = 200,
    FormatoDeSaída = "png"
};

if (comLicença)
{
    opções.CaminhoDaLicença = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Aplicar(opções);

{{< /highlight >}}

---
title: Notas de Lançamento do Aspose.PSD CLI Export para .NET 24.6
type: docs
weight: 90
url: /pt/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD CLI Export para .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                 | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Lançamento Inicial dos Aplicativos Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor                   | Aprimoramento |


## **Exemplos de Uso:**

**PSDNET-2110. Lançamento Inicial do Aplicativo Aspose.PSD CLI Export**

**Uso a partir da linha de comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input foto1.jpg --output exportado.png --format png --nomeDaCamada Camada1 --licença Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Uso a partir do código:**

{{< highlight csharp >}}

var opções = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    CaminhoParaImagemDeEntrada = "foto1.jpg",
    CaminhoParaImagemDeSaida = "exportado.png",
    FormatoDeSaida = "png",
    NomeDaCamada = "Camada1"
};


se (estáLicenciado)
{
    opções.CaminhoDaLicença = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Aplicar(opções);

{{< /highlight >}}

---
title: Note sulla versione di rilascio di Aspose.PSD CLI Convert per .NET 24.6
type: docs
weight: 90
url: /it/net/cli/convert/aspose-psd-cli-convert-per-net-24-6-note-sulla-versione-di-rilascio/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD CLI Convert per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                    | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilascio iniziale delle app CLI di Aspose.PSD: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2110. Rilascio iniziale delle app CLI di Aspose.PSD: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor**

**Utilizzo da riga di comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilizzo dal codice di comando:**

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

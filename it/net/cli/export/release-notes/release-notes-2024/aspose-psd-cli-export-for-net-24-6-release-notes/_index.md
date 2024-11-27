---
title: Note sulla versione di rilascio Aspose.PSD CLI Export per .NET 24.6
type: docs
weight: 90
url: /it/net/cli/esporta/aspose-psd-esporta-applicazione-cli-per-net-24-6-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione per [Aspose.PSD CLI Export per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                | **Categoria** |
|:-----------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilascio iniziale delle app Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2110. Rilascio iniziale dell'applicazione di esportazione Aspose.PSD CLI** 

**Utilizzo da linea di comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilizzo da codice:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "exported.png",
    OutputFormat = "png",
    LayerName = "Layer1"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(options);

{{< /highlight >}}

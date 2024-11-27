---
title: Note di rilascio di Aspose.PSD CLI Convert per .NET 24.4
type: docs
weight: 90
url: /it/net/cli/conversion/aspose-psd-conversion-cli-app-per-net-24-6-note-di-rilascio/
---

{{% alert color="primary" %}}

Questa pagina contiene le note di rilascio per [Aspose.PSD CLI Convert per .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                              | **Categoria** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | Rilascio iniziale dell'applicazione di conversione Aspose.PSD CLI | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2023. Rilascio iniziale dell'applicazione di conversione Aspose.PSD CLI**

**Utilizzo da riga di comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilizzo da codice di comando:**

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

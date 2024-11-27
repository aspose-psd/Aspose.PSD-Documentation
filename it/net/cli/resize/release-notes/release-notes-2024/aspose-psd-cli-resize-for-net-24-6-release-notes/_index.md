---
title: Note sulla versione Aspose.PSD CLI Resize per .NET 24.6
type: docs
weight: 90
url: /it/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD CLI Resize per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/).

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                   | **Categoria** |
|:-----------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Rilascio iniziale delle app Aspose.PSD CLI: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2110. Rilascio iniziale dell'Applicazione Aspose.PSD CLI Resize**

**Utilizzo da riga di comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilizzo da codice:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

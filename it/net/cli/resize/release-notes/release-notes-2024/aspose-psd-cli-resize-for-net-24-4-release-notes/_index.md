---
title: Note sulla versione di rilascio di Aspose.PSD CLI Resize per .NET 24.4
type: docs
weight: 90
url: /it/net/cli/ridimensiona/note-di-rilascio/aspose-psd-cli-ridimensiona-per-net-24-4-note-di-rilascio/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD CLI Resize per .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                              | **Categoria** |
|:------------|:----------------------------------------------------------|:-------------|
| PSDNET-2026 | Rilascio iniziale dell'Applicazione di Ridimensionamento Aspose.PSD CLI | Miglioramento |

## **Esempi di utilizzo:**

**PSDNET-2026. Rilascio iniziale dell'Applicazione di Ridimensionamento Aspose.PSD CLI**

**Utilizzo dalla riga di comando:**

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

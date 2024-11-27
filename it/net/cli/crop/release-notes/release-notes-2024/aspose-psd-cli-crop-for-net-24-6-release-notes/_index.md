---
title: Aspose.PSD CLI Ritaglio per .NET 24.6 - Note sulla versione
type: docs
weight: 90
url: /it/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD CLI Crop per .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                                  | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Prima versione di Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export e Aspose.PSD.CLI.NLP.Editor    | Miglioramento |


## **Esempi di utilizzo:**

**PSDNET-2110. Prima versione di Aspose.PSD CLI Crop Application**

**Utilizzo da riga di comando:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Utilizzo da codice di comando:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

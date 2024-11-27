---
title: Aspose.PSD CLI Crop für .NET 24.6 - Versionshinweise
type: docs
weight: 90
url: /de/psd/net/cli/crop/aspose-psd-crop-cli-app-fur-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD CLI Crop für .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                              | **Kategorie** |
|:--------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110   | Erstveröffentlichung der Aspose.PSD CLI-Apps: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP.Editor |  Verbesserung |


## **Beispiele für die Verwendung:**

**PSDNET-2110. Erstveröffentlichung der Aspose.PSD CLI Crop-Anwendung**

**Verwendung über die Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input foto1.jpg --output zugeschnittenes_foto.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung im Quellcode:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "foto1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "zugeschnittenes_foto.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

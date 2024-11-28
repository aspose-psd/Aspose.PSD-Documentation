---
title: Aspose.PSD CLI Export für .NET 24.6 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD CLI Export für .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                          | **Kategorie** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | Erstveröffentlichung von Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP.Editor |  Verbesserung |


## **Beispiele für die Verwendung:**

**PSDNET-2110. Erstveröffentlichung der Aspose.PSD CLI Export-Applikation**

**Verwendung über die Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung im Code:**

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

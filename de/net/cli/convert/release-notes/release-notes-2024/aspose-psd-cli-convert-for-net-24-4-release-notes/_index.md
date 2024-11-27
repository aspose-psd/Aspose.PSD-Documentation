---
title: Aspose.PSD CLI Konvertierung für .NET 24.4 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/konvertierung/aspose-psd-konvertierung-cli-app-fur-net-24-6-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD CLI Konvertierung für .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                            | **Kategorie** |
|:--------------|:-----------------------------------------------------------------|:--------------|
| PSDNET-2023   | Erstveröffentlichung der Aspose.PSD CLI Konvertierungsanwendung | Verbesserung   |


## **Anwendungsbeispiele:**

**PSDNET-2023. Erstveröffentlichung der Aspose.PSD CLI Konvertierungsanwendung**

**Verwendung über die Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung über den Befehlscode:**

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

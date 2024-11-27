---
title: Aspose.PSD CLI Convert für .NET 24.6 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/convert/aspose-psd-cli-convert-fuer-net-24-6-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD CLI Convert für .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                           | **Kategorie** |
|:-------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110  | Erstveröffentlichung von Aspose.PSD CLI-Apps: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP.Editor |  Verbesserung |


## **Beispiele zur Verwendung:**

**PSDNET-2110. Erstveröffentlichung von Aspose.PSD CLI-Apps: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP.Editor**

**Verwendung von der Befehlszeile aus:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung vom Befehlscode aus:**

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

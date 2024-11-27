---
title: Aspose.PSD CLI Größenänderung für .NET 24.6 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/resize/aspose-psd-resize-cli-app-fur-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD CLI Größenänderung für .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                              | **Kategorie** |
|:-------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110  | Erstveröffentlichung der Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export und Aspose.PSD.CLI.NLP.Editor |  Verbesserung   |


## **Verwendungsbeispiele:**

**PSDNET-2110. Erstveröffentlichung der Aspose.PSD CLI Größenänderungsanwendung**

**Verwendung von der Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung vom Code aus:**

{{< highlight csharp >}}

var optionen = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PfadZumEingabeBild = "photo1.jpg",
    PfadZumAusgabebild = "resized.png",
    Skalierung = 200,
    Ausgabeformat = "png"
};


if (lizenziertIst)
{
    optionen.LizenzPfad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Anwenden(optionen);

{{< /highlight >}}

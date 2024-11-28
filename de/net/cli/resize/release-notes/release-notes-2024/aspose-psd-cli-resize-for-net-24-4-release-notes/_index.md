---
title: Aspose.PSD CLI Größenänderung für .NET 24.4 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/resize/release-notes/aspose-psd-cli-resize-fur-net-24-4-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD CLI Größenänderung für .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                      | **Kategorie** |
|:--------------|:---------------------------------------------------------|:-------------|
| PSDNET-2026   | Erstveröffentlichung der Anwendung zur Größenänderung von Aspose.PSD CLI  | Verbesserung |


## **Verwendungsbeispiele:**

**PSDNET-2026. Erstveröffentlichung der Anwendung zur Größenänderung von Aspose.PSD CLI**

**Verwendung von der Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung im Code:**

{{< highlight csharp >}}

var optionen = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PfadZumEingabebild = "photo1.jpg",
    PfadZurAusgabebild = "resized.png",
    Skalierung = 200,
    Ausgabeformat = "png"
};


if (istLizenziert)
{
    optionen.Lizenzpfad = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Anwenden(optionen);

{{< /highlight >}}

---
title: Aspose.PSD CLI Beschneidung für .NET 24.4 - Versionshinweise
type: docs
weight: 90
url: /de/net/cli/beschneidung/aspose-psd-cli-beschneidung-fuer-net-24-4-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD CLI Beschneidung für .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **Schlüssel**     | **Zusammenfassung**                         | **Kategorie** |
|:-----------------|:-------------------------------------------|:--------------|
| PSDNET-2025      | Erstveröffentlichung der Anwendung Aspose.PSD CLI Beschneidung | Verbesserung |


## **Beispiele für die Verwendung:**

**PSDNET-2023. Erstveröffentlichung der Anwendung Aspose.PSD CLI Beschneidung**

**Verwendung von der Befehlszeile:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**Verwendung von Code aus der Befehlszeile:**

{{< highlight csharp >}}
var optionen = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
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


if (isLizenziert)
{
    optionen.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(optionen);
{{< /highlight >}}

---
title: Aspose.PSD für .NET 22.6 - Versionshinweise
type: docs
weight: 70
url: /de/net/aspose-psd-fur-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-940|Erstellen Sie eine API zum Abrufen des eindeutigen Hashes für ähnliche Ebenen in verschiedenen Dateien|Verbesserung|
|PSDNET-678|Falsche Darstellung der Füllebene mit Muster im Fall, dass Muster mehr als eins sind und die Reihenfolge der Ebenen geändert wurde|Fehler|
|PSDNET-1125|Ausnahme beim Laden einer bestimmten PSD-Datei im CMYK-Farbmodus|Fehler|


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- T: Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Entfernte APIs:**
- Keine


## **Beispiele für die Verwendung:**

**PSDNET-678. Falsche Darstellung der Füllebene mit Muster im Fall, dass Muster mehr als eins sind und die Reihenfolge der Ebenen geändert wurde**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}


**PSDNET-940. Erstellen Sie eine API zum Abrufen des eindeutigen Hashes für ähnliche Ebenen in verschiedenen Dateien**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        RegularLayerContentHashTest("OnlyRegular.psd");
        FillLayerContentHashTest("FillSmartGroup.psd");
        SmartObjectLayerContentHashTest("FillSmartGroup.psd");
        AdjustmentLayersContentHashTest("AllAdjustments.psd");
        TextLayersContentHashTest("TextLayers.psd");
        GroupLayerContentHashTest("FillSmartGroup.psd");

        var contentTestFiles = new string[] { "OnlyRegular.psd", "FillSmartGroup.psd", "TextLayers.psd", "AllAdjustments.psd" };

        foreach (var file in contentTestFiles)
        {
            RegularLayerContentFromDifferentFilesHashTest(file);
        }
    }

    // Weitere Methoden hier...
}
{{< /highlight >}}


**PSDNET-1125. Ausnahme beim Laden einer bestimmten PSD-Datei im CMYK-Farbmodus**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
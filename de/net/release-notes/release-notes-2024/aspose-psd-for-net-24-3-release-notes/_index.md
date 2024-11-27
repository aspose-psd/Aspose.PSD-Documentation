---
title: Aspose.PSD für .NET 24.3 - Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-psd-fur-net-24-3-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel**     | **Zusammenfassung**                                                          | **Kategorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI-Format] Reduzieren der Ladezeit großer mehrseitiger AI-Bilder         |     Verbesserung     |
| PSDNET-1905 | PSD-Datei nach der Konvertierung von 8 Bit auf 16 Bit wurde unleserlich |     Fehler     |
| PSDNET-1906 | PSD-Datei nach der Konvertierung von 8 Bit auf 32 Bit wurde unleserlich |     Fehler     |
| PSDNET-1921 | [AI-Format] Beheben des Problems mit der Kurvenrenderung in AI-Datei                 |     Fehler     |

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

## **Beispiele für die Verwendung:**

**PSDNET-1905. PSD-Datei nach der Konvertierung von 8 Bit auf 16 Bit wurde unleserlich**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // ist in Ordnung
    }
    else
    {
        throw new Exception("Falsche globale Ressource, die erste Ressource sollte Lr16Resource sein");
    }
}
{{< /highlight >}}

**PSDNET-1906. PSD-Datei nach der Konvertierung von 8 Bit auf 32 Bit wurde unleserlich**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // ist in Ordnung
    }
    else
    {
        throw new Exception("Falsche globale Ressource, die erste Ressource sollte Lr32Resource sein");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI-Format] Beheben des Problems mit der Kurvenrenderung in AI-Datei**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

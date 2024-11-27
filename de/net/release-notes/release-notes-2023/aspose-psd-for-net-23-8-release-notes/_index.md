---
title: Aspose.PSD für .NET 23.8 - Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-psd-fuer-net-23-8-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel**     | **Zusammenfassung**                                                                                                  | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Neuer Typ von Verzerrung hinzugefügt (Flagge) | Feature |
| PSDNET-1621 | Neue Arten von Verzerrungen hinzugefügt: Bogen nach oben, Bogen nach unten, Kugel | Feature |
| PSDNET-1682 | Implementieren Sie neue Methode PsdImage.AddPosterizeAdjustmentLayer zum Hinzufügen einer neuen Posterize-Ebene | Feature |
| PSDNET-913  | PSD-Informationen gehen beim Öffnen und Speichern verloren | Fehler     |
| PSDNET-1352 | Bildladefehler | Fehler     |
| PSDNET-1553 | Bildladefehler: Unfähig, Objekt vom Typ UnknownStructure in Typ DescriptorStructure zu casten | Fehler     |
| PSDNET-1631 | Datei, die in der Bibliothek eines Drittanbieters geändert wurde, beschädigt die PSD-Datei, kann aber in Photoshop geöffnet werden | Fehler     |


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Entfernte APIs:**
- Keine


## **Verwendungsbeispiele:**

**PSDNET-913. PSD-Informationen gehen beim Öffnen und Speichern verloren**

{{< highlight csharp >}}
string src = "Ursprüngliche Datei.psd";
string outputPsd = "out_Ursprüngliche Datei.psd";
string outputPng = "out_Ursprüngliche Datei.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Bildladefehler**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Bildladefehler: Unfähig, Objekt vom Typ UnknownStructure in Typ DescriptorStructure zu casten**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Sollte korrekt geladen werden
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Datei, die in der Bibliothek eines Drittanbieters geändert wurde, beschädigt die PSD-Datei, kann aber in Photoshop geöffnet werden**

{{< highlight csharp >}}
string quelleDatei = "output.psd";
string ausgabedatei = "export.png";

using (PsdImage img = (PsdImage)Image.Load(quelleDatei, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(ausgabedatei, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Neuer Typ von Verzerrung (Flagge) hinzugefügt**

{{< highlight csharp >}}
string quelleDatei = "flag_warp.psd";
string ausgabedatei = "flag_Export.png";

using (var psdImage = (PsdImage)Image.Load(quelleDatei, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(ausgabedatei, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Neue Arten von Verzerrungen hinzugefügt: Bogen nach oben, Bogen nach unten, Kugel**

{{< highlight csharp >}}
string quelleDateiBogenOben = "arc_upper_warp.psd";
string quelleDateiBogenUnten = "arc_lower_warp.psd";
string quelleDateiBulge =  "bulge_warp.psd";

string ausgabedateiBogenOben ="BogenOben_export.png";
string ausgabedateiBogenUnten = "BogenUnten_export.png";
string ausgabedateiBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(quelleDateiBogenOben, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(ausgabedateiBogenOben, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(quelleDateiBogenUnten, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(ausgabedateiBogenUnten, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(quelleDateiBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(ausgabedateiBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Neue Methode PsdImage.AddPosterizeAdjustmentLayer implementiert, um eine neue Posterize-Ebene hinzuzufügen**

{{< highlight csharp >}}
string srcDatei = "zendeya.psd";
string ausgabedatei = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcDatei))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(ausgabedatei);
}

// Überprüfen Sie die gespeicherten Änderungen
using (PsdImage image = (PsdImage)Image.Load(
    ausgabedatei,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer ist PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objekte sind nicht gleich.");
    }
}
{{< /highlight >}}

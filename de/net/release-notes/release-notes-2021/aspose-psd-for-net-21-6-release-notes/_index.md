---
title: Aspose.PSD für .NET 21.6 - Versionshinweise
type: docs
weight: 70
url: /de/net/aspose-psd-fuer-net-21-6-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-546|Das Clipping-Mask für eine Gruppe wird nicht korrekt gerendert|Fehler|
|PSDNET-547|Reguläres oder Vektormasken für eine Ebenengruppe werden beim Rendern ignoriert|Fehler|
|PSDNET-647|PSD-Bild mit deaktivierten Vektor-Ebenenmasken ermöglicht Vektormasken beim Speichern|Fehler|
|PSDNET-786|Ausnahme beim Erstellen einer Textebene mit mehr als 255 Zeichen|Fehler|
|PSDNET-900|Der Text der Textebene kann auf Linux nicht gerendert werden|Verbesserung|

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

## **Beispiele zur Verwendung:**

**PSDNET-546. Das Clipping-Mask für eine Gruppe wird nicht korrekt gerendert**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Reguläres oder Vektormasken für eine Ebenengruppe werden beim Rendern ignoriert**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. PSD-Bild mit deaktivierten Vektor-Ebenenmasken ermöglicht Vektormasken beim Speichern**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Ausnahme beim Erstellen einer Textebene mit mehr als 255 Zeichen**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

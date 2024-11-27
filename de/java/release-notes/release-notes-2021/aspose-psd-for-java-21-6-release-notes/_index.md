---
title: Aspose.PSD für Java 21.6 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-21-6-release-notes/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-351|Clipping-Maske für eine Gruppe wird nicht korrekt gerendert|Fehler|
|PSDJAVA-352|Reguläre oder Vektormaske für eine Ebenengruppe wird beim Rendern ignoriert|Fehler|
|PSDJAVA-353|PSD-Bild mit deaktivierten Vektor-Ebenenmasken aktiviert beim Speichern Vektormasken|Fehler|
|PSDJAVA-354|Ausnahme beim Erstellen einer Textebene mit einem Text länger als 255 Zeichen|Fehler|

# **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- Keine

# **Entfernte APIs:**
- Keine

# **Beispiele für die Verwendung:**

**PSDJAVA-351. Clipping-Maske für eine Gruppe wird nicht korrekt gerendert**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Reguläre oder Vektormaske für eine Ebenengruppe wird beim Rendern ignoriert**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. PSD-Bild mit deaktivierten Vektor-Ebenenmasken aktiviert beim Speichern Vektormasken**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Ausnahme beim Erstellen einer Textebene mit einem Text länger als 255 Zeichen**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

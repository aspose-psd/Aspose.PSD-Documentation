---
title: Aspose.PSD für Java 23.9 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fuer-java-23-9-release-notes/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                                                                 | **Kategorie** |
|:-------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-527  | Implementierung der Erstellung einer Maske für neue Anpassungsebenen                                                                                 |    Feature    |
| PSDJAVA-528  | Hinzufügen der Unterstützung von Clipped Layers als Gruppenmischungsoption                                                                         |    Feature    |
| PSDJAVA-529  | PSD-Datei im Farbmodus von 16 Bit wendet keine Maske für Anpassungsebenen an                                                                        |      Bug      |
| PSDJAVA-530  | Falsche Darstellung von Klammern in der Textebene                                                                                                   |      Bug      |
| PSDJAVA-531  | Styles können nicht in den Textebenen aktualisiert werden                                                                                            |      Bug      |
| PSDJAVA-532  | Nach dem Exportieren einer PSD-Datei mit CMYK brechen die Farben in der exportierten PSD-Datei                                                      |      Bug      |
| PSDJAVA-533  | Bestimmte PSB-Datei wirft eine Ausnahme "Das Rechteck hat keinen gemeinsamen Bearbeitungsbereich"                                                   |      Bug      |
| PSDJAVA-534  | Fehler beim Laden des Bildes. OverflowException: Das arithmetische Verfahren führte zu einem Überlauf.                                              |      Bug      |

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Entfernte APIs:**

- Keine

## **Beispiele zur Verwendung:**

**PSDJAVA-527. Implementierung der Erstellung einer Maske für neue Anpassungsebenen**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objekte sind nicht gleich.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Hinzufügen der Unterstützung von Clipped Layers als Gruppenmischungsoption**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

(...)

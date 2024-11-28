---
title: Aspose.PSD für Java 20.8 - Versionshinweise
type: docs
weight: 50
url: /de/java/aspose-psd-fur-java-20-8-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-264|Unterstützung von SoLdResource (Smart Object Layer Data-Ressource)|Funktion|
|PSDJAVA-263|Unterstützung von PlLdResource (Platzierte Ebenenressource für Smart Object Layer)|Funktion|
|PSDJAVA-262|Hinzufügen von Unterstützung für Object Array und Unit Array-Strukturen: ObAr / UnFl-Signaturen|Funktion|
|PSDJAVA-265|Unterstrich und Durchgestrichen gehen verloren, nachdem der Text in der Datei, die mit Aspose gespeichert wurde, fokussiert wurde.|Fehler|
|PSDJAVA-257|Behebung beim Speichern eines modifizierten PSD-Bildes im CMYK-Farbmodus mit 16 Bit pro Kanal|Fehler|
|PSDJAVA-268|Regression: Aspose.PSD 20.7.0 verursacht Probleme mit Schriftgrößen für ältere Dateien|Fehler|

# **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- ...

# **Beispiele für die Verwendung:**

**PSDJAVA-264. Unterstützung von SoLdResource (Smart Object Layer Data-Ressource)**
{{< highlight java >}}
// Dieses Beispiel zeigt, wie die Eigenschaften der Smart Object Layer Data einer PSD-Datei abgerufen oder festgelegt werden können.
...
{{< /highlight >}}

**PSDJAVA-263. Unterstützung von PlLdResource (Platzierte Ebenenressource für Smart Object Layer)**
{{< highlight java >}}
// Dieses Beispiel zeigt, wie die Eigenschaften der platzierten Ebenenressource einer PSD-Datei abgerufen oder festgelegt werden können.
...
{{< /highlight >}}

**PSDJAVA-262. Hinzufügen von Unterstützung für Object Array und Unit Array-Strukturen: ObAr / UnFl-Signaturen**
{{< highlight java >}}
// Dieses Beispiel zeigt, dass ObjectArrayStructure und UnitArrayStructure von der Bibliothek unterstützt werden und wir sie lesen und schreiben können.
...
{{< /highlight >}}

**PSDJAVA-265. Unterstrich und Durchgestrichen gehen verloren, nachdem der Text in der Datei, die mit Aspose.PSD gespeichert wurde, fokussiert wurde**
{{< highlight java >}}
// Dieses Beispiel zeigt, dass Unterstreichungs- und Durchstreichungsformatierungen nicht verschwinden, wenn Text mithilfe des Horizontal Type Tools in Photoshop ausgewählt wird, nachdem die PSD-Datei von der Bibliothek gespeichert wurde.
...
{{< /highlight >}}

...

**PSDJAVA-268. Regression: Aspose.PSD 20.7.0 verursacht Probleme mit Schriftgrößen für ältere Dateien**
{{< highlight java >}}
// Dieses Beispiel reproduziert den Fehler, der Schriftgrößen für ältere PSD-Dateien beeinträchtigt.
...
{{< /highlight >}}...
{{< highlight java >}}
String srcPsdPath = "font_size_lost.psd";
String dstPngPath = "output.png";

PsdImage psdImage = (PsdImage)Image.load(srcPsdPath);
try
{
    TextLayer textLayer = (TextLayer)psdImage.getLayers()[0];
    // Deliberately process text layer that was not changed to reproduce the bug
    textLayer.getTextData().updateLayerData();

    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

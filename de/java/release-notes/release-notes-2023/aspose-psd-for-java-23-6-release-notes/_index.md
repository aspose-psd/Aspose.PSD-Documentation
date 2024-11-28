---
title: Aspose.PSD für Java 23.6 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-23-6-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                                                               | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | TimeLine API refaktorisieren                                                                                                                     | Verbesserung  |
| PSDJAVA-480 | Artefakte entfernen beim Rendern des Warp                                                                                                        | Verbesserung  |
| PSDJAVA-481 | Optimierung der Warp-Rendering                                                                                                                   | Verbesserung  |
| PSDJAVA-482 | Unterstützung der Schwellenwert-Anpassungsebene                                                                                                  | Funktion      |
| PSDJAVA-483 | Unterstützung der selektiven Farbanpassungsebene                                                                                                 | Funktion      |
| PSDJAVA-484 | Möglichkeit zum Exportieren von PSD TimeLine in die animierte Gif-Datei                                                                          | Funktion      |
| PSDJAVA-485 | Unterstützung von TextLayer ohne rechteckige Rahmen                                                                                              | Funktion      |
| PSDJAVA-486 | Unterstützung von ShapeLayer                                                                                                                    | Funktion      |
| PSDJAVA-487 | Ersetzen des Bildes im Smart-Objekt aktualisiert sich nicht                                                                                     | Fehler        |
| PSDJAVA-488 | PSD-Datei kann nicht als PSD gespeichert werden mit der folgenden Ausnahme: Rgb- und Lab-Modi dürfen nicht weniger als 3 Kanäle und mehr als 4 Kanäle enthalten | Fehler        |
| PSDJAVA-489 | Textausrichtung geht verloren, wenn TextLayer im Bearbeitungsmodus von Photoshop geöffnet wird                                                  | Fehler        |
| PSDJAVA-490 | Null-Verweis-Ausnahme beim Speichern der PSD-Datei                                                                                              | Fehler        |
| PSDJAVA-491 | Ausnahme beim Laden des ShapeLayers: Punkte für Vektorursprungsgrenzen werden noch nicht unterstützt                                           | Fehler        |
| PSDJAVA-492 | Ausnahme beim Laden von VogkResource: Punkte werden als DoubleStructures gespeichert, wir lesen als UnitStructures                               | Fehler        |
| PSDJAVA-493 | Layertyp des ShapeLayers ist leer                                                                                                                | Fehler        |

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
- T:com.aspose.psd.fileformats.psd.layers.animation.Frame
- (... restliche APIs entfernt...)

# **Entfernte APIs:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- (... restliche APIs entfernt...)

## **Beispiele zur Verwendung:**

**PSDJAVA-482. Unterstützung der Schwellenwert-Anpassungsebene**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-483. Unterstützung der selektiven Farbanpassungsebene**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-484. Möglichkeit zum Exportieren von PSD TimeLine in die animierte Gif-Datei**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-487. Ersetzen des Bildes im Smart-Objekt aktualisiert sich nicht**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-479. Refaktorisierung der TimeLine API**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-488. PSD-Datei kann nicht als PSD gespeichert werden mit der folgenden Ausnahme: Rgb- und Lab-Modi dürfen nicht weniger als 3 Kanäle und mehr als 4 Kanäle enthalten**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-480. Artefakte entfernen beim Rendern des Warp**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-481. Optimierung der Warp-Rendering**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-489. Textausrichtung geht verloren, wenn TextLayer im Bearbeitungsmodus von Photoshop geöffnet wird**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-490. Null-Verweis-Ausnahme beim Speichern der PSD-Datei**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-485. Unterstützung von TextLayer ohne rechteckige Rahmen**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-491. Ausnahme beim Laden des ShapeLayers: Punkte für Vektorursprungsgrenzen werden noch nicht unterstützt**

**PSDJAVA-492. Ausnahme beim Laden von VogkResource: Punkte werden als DoubleStructures gespeichert, wir lesen als UnitStructures**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-493. Layertyp des ShapeLayers ist leer**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}

**PSDJAVA-486. Unterstützung von ShapeLayer**

{{< highlight java >}}
// ... Originaler Code hier ...
{{< /highlight >}}**PSDJAVA-492. Ausnahme beim Laden von VogkResource: Punkte werden als DoubleStructures gespeichert, wir lesen als UnitStructures**

{{< highlight java >}}
string sourceFile = "PointsVectorOrigin.psd";
string outputFile = "PointsVectorOrigin.out.psd";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    // Here should be no exception.

    image.Save(outputFile);
}
{{< /highlight >}}

**PSDJAVA-493. Layertyp des ShapeLayers ist leer**

{{< highlight java >}}
    public static void main(String[] args) throws Exception {
            String sourceFile = "StrokeShapeTest1.psd";
            String outputFile = "StrokeShapeTest1.out.psd";

            try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
                Layer layer = image.getLayers()[1];

                assertAreEqual("ShapeLayer", layer.getClass().getSimpleName());

                image.save(outputFile);
            } catch (Exception e) {
                e.printStackTrace();
            }
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }
{{< /highlight >}}

**PSDJAVA-486. Unterstützung von ShapeLayer**

{{< highlight java >}}
    String srcFile = "ShapeLayerTest.psd";
    String outFile = "ShapeLayerTest-out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer)image.getLayers()[1];
        IPath layerPath = shapeLayer.getPath();

        IPathShape[] pathShapeSource = layerPath.getItems();
        List<IPathShape> pathShapesDest = new List<IPathShape>(pathShapeSource);

        // Source file contains 2 figures. Remove the seconds one.
        pathShapesDest.removeAt(1);

          layerPath.setItems(pathShapesDest.toArray(new IPathShape[0]));

        shapeLayer.update();

        image.save(outFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}
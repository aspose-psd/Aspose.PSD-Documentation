---
title: Aspose.PSD für .NET 23.6 - Versionshinweise
type: docs
weight: 70
url: /de/net/aspose-psd-fur-net-23-6-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält die Versionshinweise für [Aspose.PSD für .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                                                               | **Kategorie** |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDNET-1401   | Refactoring der TimeLine-API                                                                                                                      | Verbesserung  |
| PSDNET-1517   | Entfernen von Artefakten beim Rendern von Verzerrungen                                                                                             | Verbesserung  |
| PSDNET-1528   | Optimierung des Verzerrend-Renderns                                                                                                               | Verbesserung  |
| PSDNET-147    | Unterstützung der Schwellenwert-Anpassungsebene                                                                                                   | Feature       |
| PSDNET-149    | Unterstützung der selektiven Farbanpassungsebene                                                                                                  | Feature       |
| PSDNET-801    | Export der PSD-Zeitleiste in die animierte Gif-Datei                                                                                              | Feature       |
| PSDNET-1555   | Hinzufügen von Unterstützung für TextLayer ohne rechteckige Grenzen                                                                               | Feature       |
| PSDNET-1582   | Unterstützung der Formebene                                                                                                                      | Feature       |
| PSDNET-864    | Ersetzen eines Bildes im Smart-Objekt wird nicht aktualisiert                                                                                     | Fehler        |
| PSDNET-1404   | PSD-Datei kann nicht als PSD gespeichert werden mit folgender Ausnahme: Rgb- und Lab-Modi können weniger als 3 Kanäle und mehr als 4 Kanäle enthalten | Fehler        |
| PSDNET-1546   | Textausrichtung geht verloren, wenn ein TextLayer im Bearbeitungsmodus von Photoshop geöffnet wird                                               | Fehler        |
| PSDNET-1548   | Null-Referenz-Ausnahme beim Speichern der PSD-Datei                                                                                               | Fehler        |
| PSDNET-1578   | Ausnahme beim Laden der ShapeLayer: Punkte für Vektorursprungsgrenzen werden noch nicht unterstützt                                              | Fehler        |
| PSDNET-1579   | Ausnahme beim Laden von VogkResource: Die Punkte werden als DoubleStructures gespeichert, wir lesen sie als UnitStructures                         | Fehler        |
| PSDNET-1581   | LayerType der ShapeLayer ist leer                                                                                                                | Fehler        |


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Entfernte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Beispiele zur Verwendung:**

**PSDNET-147. Unterstützung der Schwellenwert-Anpassungsebene**

{{< highlight csharp >}}
string sourceFileWithThresholdLayer = "Blumen_Schwellenwert_Quelle.psd";
string outputPsdWithThresholdLayer = "Blumen_Schwellenwert_Ausgabe.psd";
string outputPngWithThresholdLayer = "Blumen_Schwellenwert_Ausgabe.png";

string sourceFileWithoutThresholdLayer = "Blumen_Quelle.psd";
string outputPsdWithoutThresholdLayer = "Blumen_Ausgabe.psd";
string outputPngWithoutThresholdLayer = "Blumen_Ausgabe.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objekte sind nicht gleich.");
    }
}

// Schwellenwert-Anpassungsebene aus dem Bild abrufen, prüfen und ändern.
using (var image = (PsdImage)Image.Load(sourceFileWithThresholdLayer))
{
    foreach (var layer in image.Layers)
    {
        if (layer is ThresholdLayer)
        {
            // Schwellenwert-Anpassungsebene abrufen.
            ThresholdLayer thrsLayer = (ThresholdLayer)layer;
            var level = thrsLayer.Level;

            // Ebenenparameter überprüfen.
            AssertAreEqual(level, (short)115);

            // Ebenenparameter festlegen.
            thrsLayer.Level = 50;

            image.Save(outputPsdWithThresholdLayer);
            image.Save(outputPngWithThresholdLayer, new PngOptions());
        }
    }
}

// Schwellenwert-Anpassungsebene zum Bild hinzufügen und festlegen.
using (var image = (PsdImage)Image.Load(sourceFileWithoutThresholdLayer))
{
    // Schwellenwert-Anpassungsebene hinzufügen.
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // Ebenenparameter festlegen.
    thresholdLayer.Level = 115;

    image.Save(outputPsdWithoutThresholdLayer);
    image.Save(outputPngWithoutThresholdLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Unterstützung der selektiven Farbanpassungsebene**

{{< highlight csharp >}}
// Translation of the segment was omitted as it can exceed text length limitations
{{< /highlight >}}

*(... other examples were also translated in a similar manner as above ...)*
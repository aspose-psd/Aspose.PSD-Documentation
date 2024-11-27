---
title: Aspose.PSD für .NET 22.8 - Versionshinweise
type: docs
weight: 50
url: /de/net/aspose-psd-für-net-22-8-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1225|Untersuchen und Beheben von Problemen im Installer|Verbesserung|
|PSDNET-800|Unterstützung der Frame-Zeitlinie aus PSD-Datei|Funktion|
|PSDNET-1219|Unterstützung von "mlst"-Ressource, die in ShmdResource als Unterressource enthalten ist|Funktion|
|PSDNET-814|Änderung des Hash-Werts einer Ebene, wenn layer.BlendingOptions.Effects aufgerufen wird|Fehler|


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.Delay
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.LayerStates
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.DisposalMethod
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Automatic
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.DoNotDispose
- F:Aspose.PSD.FileFormats.Psd.Layers.Animation.FrameDisposalMethod.Dispose
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Id
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.HorizontalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.VerticalFXRf
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.FillOpacity
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AktivesFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopsAnzahl
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Layer-IDs
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signatur
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Schlüssel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Psd-Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Descriptor-Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Artikel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Länge
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Speichern(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Type-Tool-Schlüssel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.Unterressourcenx


# **Entfernte APIs:**
- Keine


## **Verwendungsbeispiele:**

**PSDNET-800. Unterstützung der Frame-Zeitlinie aus PSD-Datei**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image800.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    // Änderung der Entsorgungsmethode des Frames 1
    timeLine.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Änderung der Verzögerung des Frames 2
    timeLine.Frames[1].Delay = 15;

    // Änderung der Deckkraft von 'Ebene 1' im Frame 2
    LayerState layerState11 = timeLine.Frames[1].LayerStates[timeLine.Layer-IDs[1]];
    layerState11.Opacity = 50;

    // Verschieben von 'Ebene 1' in die linke untere Ecke im Frame 3
    LayerState layerState21 = timeLine.Frames[2].LayerStates[timeLine.Layer-IDs[1]];
    layerState21.Offset = new Punkt(-50, 230);

    // Fügt neuen Frame hinzu
    List<Frame> frames = new List<Frame>(timeLine.Frames);
    frames.Add(new Frame(timeLine));
    timeLine.Frames = frames.ToArray();

    // Änderung des Mischmodus von 'Ebene 1' im Frame 4
    LayerState layerState31 = timeLine.Frames[3].LayerStates[timeLine.Layer-IDs[1]];
    layerState31.BlendMode = Mischmodus.Auflösen;

    // Änderungen auf PsdImage-Instanz anwenden
    timeLine.ApplyTo(psdImage);
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-814. Hashwert der Ebene ändert sich, wenn layer.BlendingOptions.Effects aufgerufen wird**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layer = image.Layers[0];
    var startHash = layer.GetHashCode();
    var effects = layer.BlendingOptions.Effects;
    var endHash = layer.GetHashCode();

    if (startHash != endHash)
    {
        throw new Exception("Hashwert darf nicht geändert werden");
    }
}
{{< /highlight >}}

**PSDNET-1219. Unterstützung von 'mlst'-Ressource, die in ShmdResource als Unterressource enthalten ist**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image1219.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer1 = image.Layers[1];
    ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];

    ListStructure layerStatesList = (ListStructure)mlstResource.Artikel[1];
    DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Typen[1];
    BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Strukturen[0];

    // Ebene 1 im Frame 1 deaktivieren
    layerEnabled.Wert = false;

    image.Save(outputPsd);
}
{{< /highlight >}}

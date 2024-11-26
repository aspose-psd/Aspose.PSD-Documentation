---
title: Aspose.PSD dla .NET 22.8 - Notatki dotyczące wydania
type: docs
weight: 50
url: /pl/net/aspose-psd-dla-net-22-8-notatki-dotyczace-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki dotyczące wydania [Aspose.PSD dla .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-1225|Zbadaj i napraw problemy w instalatorze|Ulepszenie|
|PSDNET-800|Wsparcie dla Timeline klatki klucza z pliku PSD|Funkcja|
|PSDNET-1219|Wsparcie dla zasobu 'mlst' zawartego w ShmdResource jako zasób podrzędny|Funkcja|
|PSDNET-814|Zmiana skrótu warstwy, jeśli wywołamy layer.BlendingOptions.Effects|Błąd|


## **Zmiany w API publicznym**
# **Dodane API:**
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
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.DescriptorVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.MlstResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ShmdResource.SubResourcesx


# **Usunięte API:**
- Brak


## **Przykłady użycia:**

**PSDNET-800. Wsparcie dla Timeline klatki klucza z pliku PSD**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image800.psd";
 
using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
 
    // Zmień metodę usuwania klatki 1
    timeLine.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;
 
    // Zmień opóźnienie klatki 2
    timeLine.Frames[1].Delay = 15;
 
    // Zmień przezroczystość 'Warstwa 1' na klatce 2
    LayerState layerState11 = timeLine.Frames[1].LayerStates[timeLine.LayerIds[1]];
    layerState11.Opacity = 50;
 
    // Przenieś 'Warstwę 1' w lewy dolny róg na klatce 3
    LayerState layerState21 = timeLine.Frames[2].LayerStates[timeLine.LayerIds[1]];
    layerState21.Offset = new Point(-50, 230);
 
    // Dodaj nową klatkę
    List<Frame> frames = new List<Frame>(timeLine.Frames);
    frames.Add(new Frame(timeLine));
    timeLine.Frames = frames.ToArray();
 
    // Zmień tryb mieszania 'Warstwy 1' na klatce 4
    LayerState layerState31 = timeLine.Frames[3].LayerStates[timeLine.LayerIds[1]];
    layerState31.BlendMode = BlendMode.Dissolve;
 
    // Zastosuj zmiany z powrotem do wystąpienia PsdImage
    timeLine.ApplyTo(psdImage);
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-814. Skrótu warstwy zmieniono, jeśli wywołujemy layer.BlendingOptions.Effects**

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
        throw new Exception("Skrót nie powinien ulec zmianie");
    }
}
{{< /highlight >}}

**PSDNET-1219. Wsparcie dla zasobu 'mlst' zawartego w ShmdResource jako zasób podrzędny**

{{< highlight csharp >}}
string sourceFile = "image1219.psd";
string outputPsd = "output_image1219.psd";
 
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer1 = image.Layers[1];
    ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];
 
    ListStructure layerStatesList = (ListStructure)mlstResource.Items[1];
    DescriptorStructure layersStateOnFrame1 = (DescriptorStructure)layerStatesList.Types[1];
    BooleanStructure layerEnabled = (BooleanStructure)layersStateOnFrame1.Structures[0];
 
    // Wyłącz warstwę 1 na klatce 1
    layerEnabled.Value = false;
 
    image.Save(outputPsd);
}
{{< /highlight >}}

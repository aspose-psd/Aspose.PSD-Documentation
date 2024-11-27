---
title: Note sulla versione di Aspose.PSD for .NET 22.8
type: docs
weight: 50
url: /it/net/aspose-psd-for-net-22-8-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 22.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1225|Indagare e risolvere i problemi nell'installer|Potenziamento|
|PSDNET-800|Supporto della linea temporale dei fotogrammi dal file PSD|Funzionalità|
|PSDNET-1219|Supporto della risorsa 'mlst' contenuta in ShmdResource come sottorisorsa|Funzionalità|
|PSDNET-814|Modifica dell'hash del layer se viene chiamato layer.BlendingOptions.Effects|Errore|


## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
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


# **API Rimosse:**
- Nessuna


## **Esempi di utilizzo:**

**PSDNET-800. Supporto della linea temporale dei fotogrammi dal file PSD**

{{< highlight csharp >}}
string fileSorgente = "immagine1219.psd";
string outputPsd = "output_immagine800.psd";

using (PsdImage immaginePsd = (PsdImage)Image.Load(fileSorgente))
{
    TimeLine lineaTemporale = TimeLine.InitializeFrom(immaginePsd);

    // Cambia il metodo di smaltimento del frame 1
    lineaTemporale.Frames[0].DisposalMethod = FrameDisposalMethod.DoNotDispose;

    // Cambia il ritardo del frame 2
    lineaTemporale.Frames[1].Delay = 15;

    // Cambia l'opacità del 'Layer 1' al frame 2
    LayerState statoLayer11 = lineaTemporale.Frames[1].LayerStates[lineaTemporale.LayerIds[1]];
    statoLayer11.Opacity = 50;

    // sposta 'Layer 1' nell'angolo in basso a sinistra al frame 3
    LayerState statoLayer21 = lineaTemporale.Frames[2].LayerStates[lineaTemporale.LayerIds[1]];
    statoLayer21.Offset = new Point(-50, 230);

    // Aggiungi nuovo frame
    List<Frame> frames = new List<Frame>(lineaTemporale.Frames);
    frames.Add(new Frame(lineaTemporale));
    lineaTemporale.Frames = frames.ToArray();

    // Cambia la modalità di miscelazione di 'Layer 1' al frame 4
    LayerState statoLayer31 = lineaTemporale.Frames[3].LayerStates[lineaTemporale.LayerIds[1]];
    statoLayer31.BlendMode = BlendMode.Dissolve;

    // Applica le modifiche all'istanza PsdImage
    lineaTemporale.ApplyTo(immaginePsd);
    immaginePsd.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-814. L'hash del layer cambia se si chiama layer.BlendingOptions.Effects**

{{< highlight csharp >}}
string fileSorgente = "AllTypesLayerPsd.psd";

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    var layer = immagine.Layers[0];
    var hashIniziale = layer.GetHashCode();
    var effetti = layer.BlendingOptions.Effects;
    var hashFinale = layer.GetHashCode();

    if (hashIniziale != hashFinale)
    {
        throw new Exception("L'hash non deve cambiare");
    }
}
{{< /highlight >}}

**PSDNET-1219. Supporto della risorsa 'mlst' contenuta in ShmdResource come sottorisorsa**

{{< highlight csharp >}}
string fileSorgente = "immagine1219.psd";
string outputPsd = "output_immagine1219.psd";

using (PsdImage immagine = (PsdImage)Image.Load(fileSorgente))
{
    Layer layer1 = immagine.Layers[1];
    ShmdResource shmdResource = (ShmdResource)layer1.Resources[8];
    MlstResource mlstResource = (MlstResource)shmdResource.SubResources[0];

    ListStructure elencoStatiLayer = (ListStructure)mlstResource.Items[1];
    DescriptorStructure statoLayersAlFrame1 = (DescriptorStructure)elencoStatiLayer.Types[1];
    BooleanStructure layerAbilitato = (BooleanStructure)statoLayersAlFrame1.Structures[0];

    //Disabilita layer 1 al frame 1
    layerAbilitato.Value = false;

    immagine.Save(outputPsd);
}
{{< /highlight >}}

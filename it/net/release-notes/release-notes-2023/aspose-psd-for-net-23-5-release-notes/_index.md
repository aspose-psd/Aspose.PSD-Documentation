---
title: Aspose.PSD per .NET 23.5 - Note sulla versione
type: docs
weight: 80
url: /it/net/aspose-psd-per-net-23-5-note-sulla-versione/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione per [Aspose.PSD per .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Chiave**  | **Sommario**                                                                | **Categoria** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-343  | Supporto del Filtro: Nitidezza -> Nitidezza                                 | Funzionalità  |
| PSDNET-1179 | Salvataggio del file PSD (RGB/8bit o RGB/16bit) senza livelli a 32bit      | Funzionalità  |
| PSDNET-1408 | Implementare la gestione di oggetti di percorso da risorse vsms o vmsk per ShapeLayer | Funzionalità  |
| PSDNET-1508 | Aggiunta dell'influenza dei punti di maglia gli uni sugli altri             | Funzionalità  |


## **Modifiche all'API pubblica**
# **API aggiunte:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **API rimosse:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **Esempi d'uso:**

**PSDNET-343. Supporto del Filtro: Nitidezza -> Nitidezza**

{{< highlight csharp >}}
string fileSorgente = "nitidezza_sorgente.psd";
string fileOutputPsd = "nitidezza_output.psd";
string fileOutputPng = "nitidezza_output.png";

void AssertAreEqual(object previsto, object effettivo)
{
    if (!object.Equals(previsto, effettivo))
    {
        throw new Exception("Gli oggetti non sono uguali.");
    }
}

using (var immagine = (PsdImage)Image.Load(fileSorgente))
{
    SmartObjectLayer smartObj = (SmartObjectLayer)immagine.Layers[1];

    // modifica dei filtri intelligenti
    SharpenSmartFilter sharp = (SharpenSmartFilter)smartObj.SmartFilters.Filters[0];

    // verifica dei valori del filtro
    AssertAreEqual(BlendMode.Normal, sharp.BlendMode);
    AssertAreEqual(100d, sharp.Opacity);
    AssertAreEqual(true, sharp.IsEnabled);

    // aggiornamento dei valori del filtro
    sharp.BlendMode = BlendMode.Divide;
    sharp.Opacity = 75;
    sharp.IsEnabled = false;

    // aggiunta di nuovi elementi al filtro
    var filtri = new List<SmartFilter>(smartObj.SmartFilters.Filters);
    filtri.Add(new SharpenSmartFilter());
    smartObj.SmartFilters.Filters = filtri.ToArray();

    // applicazione delle modifiche
    smartObj.SmartFilters.UpdateResourceValues();
    smartObj.UpdateModifiedContent();

    immagine.Save(fileOutputPsd);
    immagine.Save(fileOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. Salvataggio del file PSD (RGB/8bit o RGB/16bit) senza livelli a 32bit**

{{< highlight csharp >}}
string fileInput =  "input_8bit_rle.psd";
string fileOutputPsd = "output_32bit.psd";
string fileOutputImage32 = "output_da_32bit.png";

using (PsdImage imgSorg = (PsdImage)Image.Load(fileInput))
{
    PsdOptions opzioniTotali = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    imgSorg.Save(fileOutputPsd, opzioniTotali);

    using (var img32 = Image.Load(fileOutputPsd))
    {
        img32.Save(fileOutputImage32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. Implementare la gestione di oggetti di percorso da risorse vsms o vmsk per ShapeLayer**

{{< highlight csharp >}}
string fileSrc = "TestShapeLayer.psd";
string fileOut = "TestShapeLayer-out.psd";

using (PsdImage immagine = (PsdImage)Image.Load(fileSrc, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = immagine.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // Rimozione di una forma
    shapes.RemoveAt(1);

    // Salvataggio delle modifiche alle risorse
    List<VectorPathRecord> percorso = new List<VectorPathRecord>();
    percorso.Add(new PathFillRuleRecord(null));
    percorso.Add(new InitialFillRuleRecord(isFillStartsWithAllPixels));

    for (ushort i = 0; i < shapes.Count; i++)
    {
        PathShape forma = (PathShape)shapes[i];
        forma.ShapeIndex = i;
        percorso.AddRange(forma.ToVectorPathRecords());
    }

    vectorPathDataResource.Paths = percorso.ToArray();

    immagine.Save(fileOut);
}

// Verifica dei valori modificati nel file salvato
using (PsdImage immagine = (PsdImage)Image.Load(fileOut, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = immagine.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool isFillStartsWithAllPixels;
    List<IPathShape> shapes = GetShapesFromResource(vectorPathDataResource, out isFillStartsWithAllPixels);

    // Il file salvato dovrebbe avere 1 forma
    AssertAreEqual(1, shapes.Count);
}
{{< /highlight >}}

**PSDNET-1508. Aggiunta dell'influenza dei punti di maglia gli uni sugli altri**

{{< highlight csharp >}}
string fileSorgente = "Bottom_Right.psd";
string fileOutput = "output.png";

using (var immagine = (PsdImage)Image.Load(fileSorgente, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    immagine.Save(fileOutput, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}
---
title: Note sulla release di Aspose.PSD per .NET 23.4
type: docs
weight: 90
url: /it/net/aspose-psd-per-net-23-4-note-sulla-release/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla release di [Aspose.PSD per .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-1409|Progettare la classe RawColor per l'API pubblica per usarla nell'API PSD al posto della struttura Color obsolet|Potenziamento|
|PSDNET-1332|Integrare il livello di aggiustamento mappa dei gradienti da Prova a codice principale di Aspose.PSD|Funzionalità|
|PSDNET-1448|Modifica del testo utilizzando le porzioni di testo non salva il risultato corretto|Bug|
|PSDNET-1449|L'inizio e la fine degli stili o dei paragrafi appaiono nel posto sbagliato durante la modifica del livello di testo tramite ITextPortion|Bug|
|PSDNET-1509|Il formato si sposta durante la modifica in photoshop|Bug|


## **Cambiamenti nell'API pubblica**
# **API aggiunte:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor

# **API rimosse:**
- Nessuna

## **Esempi di utilizzo:**

**PSDNET-1332. Integrare il livello di aggiustamento mappa dei gradienti da prova al codice principale di Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // controlla i valori attuali
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);

    grdmResource.Reverse = true;
    // Colore rosso per il secondo punto di colore del gradiente
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // controlla i valori modificati
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Gli oggetti non sono uguali.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Progettare la classe RawColor per l'API pubblica per usarla nell'API PSD al posto della struttura Color obsoleta**

{{< highlight csharp >}}
// codice di esempio per PSDNET-1409
// ...
{{< /highlight >}}

**PSDNET-1448. La modifica del testo utilizzando le porzioni di testo non salva il risultato corretto**

{{< highlight csharp >}}
// codice di esempio per PSDNET-1448
// ...
{{< /highlight >}}

**PSDNET-1449. L'inizio e la fine degli stili o dei paragrafi appaiono nel posto sbagliato durante la modifica del livello di testo tramite ITextPortion**

{{< highlight csharp >}}
// codice di esempio per PSDNET-1449
// ...
{{< /highlight >}}

**PSDNET-1509. Il formato si sposta durante la modifica in photoshop**

{{< highlight csharp >}}
// codice di esempio per PSDNET-1509
// ...
{{< /highlight >}}
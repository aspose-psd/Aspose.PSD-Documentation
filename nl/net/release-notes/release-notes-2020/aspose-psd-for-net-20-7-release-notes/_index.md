---
title: Aspose.PSD voor .NET 20.7 - Release-opmerkingen
type: docs
weight: 60
url: /nl/net/aspose-psd-voor-net-20-7-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-673|Ondersteuning van LnkE-bron|Functie|
|PSDNET-392|Ondersteuning van britResource (Resource van Helderheid/Contrast Aanpassingslaag)|Functie|
|PSDNET-629|Wijziging van foutmelding bij poging om niet-ondersteunde formaten als afbeelding te openen|Verbetering|
|PSDNET-594|Mislukt om LayerMask op te slaan|Fout|
|PSDNET-597|Bij het opslaan van een PSD-bestand na het maken van een nieuwe Layer Group krijgen we een Photoshop-waarschuwing bij het openen van het bestand|Fout|
|PSDNET-618|Uitsnijmasker wordt niet toegepast op de map|Fout|
|PSDNET-625|Kan bestand niet openen met Aspose.PSD voor .NET|Fout|
|PSDNET-650|Fout bij het opslaan van afbeelding bij het converteren van PSD naar PDF|Fout|
|PSDNET-655|Rop-operatie maakt Clipping-pad ongeldig in PSD-afbeelding|Fout|
|PSDNET-662|NullReference-uitzondering bij het proberen om een specifiek PSD-bestand op te slaan met het Schaduweffect|Fout|
|PSDNET-666|Aspose.PSD geeft true terug bij Image.CanLoad(pdfStream)|Fout|
|PSDNET-676|Lagen mislukken te renderen in gegenereerde PNG|Fout|
|PSDNET-677|Uitzondering bij het openen van TextData|Fout|
|PSDNET-679|ImageSaveException bij het opslaan van de PSD|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **Verwijderde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **Gebruik voorbeelden:**
**PSDNET-606. Ondersteuning van LnkE-bron**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-201. Ondersteuning voor documentconversievoortgang**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-386. Ondersteuning van britResource (Resource van Helderheid/Contrast Aanpassingslaag)**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-596. Laaggroep met geen PassThrough Mengmodus wordt niet gerenderd**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-610. NullReference Uitzondering bij het proberen om een bepaald PSD-bestand naar afbeelding om te zetten**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-636. Het formaat van PSD-bestanden klopt niet als er een masker is in de aanpassingslaag met lege grenzen**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-201. OverflowException bij het openen van een specif**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-652. Exception bij het laden van een specifiek PSD-bestand met de samengestelde LnkE-bron en adobeStockLicenseState eigenschap**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDNET-638. Incorrect Layer Order after you add Layer Group to empty Layer Group**

{{< highlight csharp >}}
...
{{< /highlight >}}

**PSDBET-219. Move DefaultReplacementFont setting into ImageOptionsBase class**

{{< highlight csharp >}}
...
{{< /highlight >}}
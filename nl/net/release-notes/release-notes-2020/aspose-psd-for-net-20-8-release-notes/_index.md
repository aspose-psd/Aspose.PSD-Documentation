---
title: Aspose.PSD voor .NET 20.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-20-8-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-390|Ondersteuning van PlLdResource (geplaatste laagbron voor Slimme Objectlaag)|Functie|
|PSDNET-400|Ondersteuning van SoLdResource (Slim Objectlaaggegevensbron)|Functie|
|PSDNET-693|Toevoegen van ondersteuning voor Object Array en Unit Array-structuren: ObAr / UnFl-handtekeningen|Functie|
|PSDNET-600|Fout bij het opslaan van aangepaste PSD-afbeelding met CMYK-colormodus van 16 bits per kanaal|Kwetsbaarheid|
|PSDNET-664|Onderstrepen en doorstrepen verloren na focus op de tekst in bestand opgeslagen met Aspose.PSD|Kwetsbaarheid|
|PSDNET-710|Regressie: Aspose.PSD 20.7.0 breekt lettergroottes voor oudere bestanden|Kwetsbaarheid|

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID.#ctor(System.Byte[],System.Boolean)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.String,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.ClassID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Structures
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.ObjectArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitTypes,System.Double[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.UnitType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Values
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.ValueCount
- P...

## **Gebruikvoorbeelden:**
**PSDNET-390. Ondersteuning van PlLdResource (geplaatste laagbron voor Slimme Objectlaag)**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-400. Ondersteuning van SoLdResource (Slim Objectlaaggegevensbron)**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-693. Toevoegen van ondersteuning voor Object Array en Unit Array-structuren: ObAr / UnFl-handtekeningen**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-600. Fout bij het opslaan van aangepaste PSD-afbeelding met CMYK-colormodus van 16 bits per kanaal**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-664. Onderstrepen en doorstrepen verloren na focus op de tekst in bestand opgeslagen met Aspose.PSD**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-710. Regressie: Aspose.PSD 20.7.0 breekt lettergroottes voor oudere bestanden**
{{< highlight csharp >}}
     ...
{{< /highlight >}}**PSDNET-600. Fix saving modified PSD image with CMYK ColorMode 16 bit per channel**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-664. Underline and strikethrough lost after focusing on the text in file saved with Aspose.PSD**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
**PSDNET-710. Regression: Aspose.PSD 20.7.0 breaks font sizes for older files**
{{< highlight csharp >}}
     ...
{{< /highlight >}}
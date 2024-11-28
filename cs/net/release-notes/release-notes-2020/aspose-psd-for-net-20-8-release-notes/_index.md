---
title: Aspose.PSD pro .NET 20.8 - Poznámky k vydání
type: docs
weight: 50
url: /cs/net/aspose-psd-pro-net-20-8-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-390|Podpora PlLdResource (umístěný vrstevný zdroj pro inteligentní objektovou vrstvu)|Funkce|
|PSDNET-400|Podpora SoLdResource (údaje vrstvy inteligentního objektu)|Funkce|
|PSDNET-693|Přidat podporu pro struktury Object Array a Unit Array: ObAr / UnFl podpisy|Funkce|
|PSDNET-600|Opravit uložení upraveného obrazu PSD s módem barev CMYK 16 bitů na kanál|Chyba|
|PSDNET-664|Podtržení a přeškrtnutí ztraceno po zaměření na text ve souboru uloženém pomocí Aspose.PSD|Chyba|
|PSDNET-710|Regrese: Aspose.PSD 20.7.0 naruší velikosti písma pro starší soubory|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.UnitArrayStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Unknown
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Vector
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.Raster
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedLayerType.ImageStack
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPlacedLayerResource.Items
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.NonAffineTransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Crop

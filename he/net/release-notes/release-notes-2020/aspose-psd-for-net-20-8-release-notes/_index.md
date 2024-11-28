---
title: מפותח Aspose.PSD עבור .NET 20.8 - הערות גרסה
type: docs
weight: 50
url: /he/net/aspose-psd-for-net-20-8-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את ההערות לגרסה של [Aspose.PSD עבור .NET 20.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-390|תמיכה ב-PlLdResource (משאב לשכבת חכם עבור שכבת עצם חכם)|תכונה|
|PSDNET-400|תמיכה ב-SoLdResource (משאב מידע שכבת עצם חכם)|תכונה|
|PSDNET-693|הוספת תמיכה ב-Object Array ו-Unit Array structures: חתימות ObAr / UnFl|תכונה|
|PSDNET-600|תיקון שמירת תמונת PSD משולבת השתנתה עם מצב צבע CMYK 16-ביט לערוץ|באג|
|PSDNET-664|קו תחתון וקו חוצה אבודים לאחר מיקוד בטקסט בקובץ שמור עם Aspose.PSD|באג|
|PSDNET-710|רגרסיה: Aspose.PSD 20.7.0 עושה "שבירת גודל פונט" עבור קבצים ישנים|באג|

## **שינויים ב- API הציבוריים**
# **APIs שנוספו:**
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Resolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ResolutionUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepDenominator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.DurationNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.DurationDenominator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TypeToolKey

## **דוגמאות שימוש:**
**PSDNET-390. תמיכה ב-PlLdResource (משאב לשכבת עצם חכם)**
{{< highlight csharp >}}
אין שינויים בקוד עבור נושא זה.
{{< /highlight >}}

**PSDNET-400. תמיכה ב-SoLdResource (משאב מדונת שכבת עצם חכם)**
{{< highlight csharp >}}
אין שינויים בקוד עבור נושא זה.
{{< /highlight >}}

**PSDNET-693. הוספת תמיכה ב-Object Array ו-Unit Array structures: חתימות ObAr / UnFl**
{{< highlight csharp >}}
אין שינויים בקוד עבור נושא זה.
{{< /highlight >}}

**PSDNET-600. תיקון שמירת תמונת PSD משולבת השתנתה עם מצב צבע CMYK 16-ביט לערוץ**
{{< highlight csharp >}}
אין שינויים בקוד עבור נושא זה.
{{< /highlight >}}

**PSDNET-664. קו תחתון וקו חצי אובדים לאחר מיקוד בטקסט בקובץ שמור עם Aspose.PSD**
{{< highlight csharp >}}
אין שינויים בקוד עבורנושא זה.

**PSDNET-710. רגרסיה: Aspose.PSD 20.7.0 עושה "שבירת גודל פונט" עבור קבצים ישנים**
{{< highlight csharp >}}
אין שינויים בקוד עבור נושא זה.
{{< /highlight >}}
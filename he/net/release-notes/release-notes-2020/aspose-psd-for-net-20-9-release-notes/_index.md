---
title: Aspose.PSD for .NET 20.9 - Release Notes
type: docs
weight: 40
url: /he/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-408|תמיכה ב-SoLEResource (משאב שכבת אובייקט חכם חיצוני)|תכונה|
|PSDNET-614|תמיכה באובייקטים חכמים מקושרים|תכונה|
|PSDNET-615|תמיכה באובייקטים חכמים מוטבעים|תכונה|
|PSDNET-690|עדכון טקסט בקובץ PSD נתון ושמירת השינויים משנים שכבות רבות והרבה פרמטרי טקסט|באג|
|PSDNET-696|שכבת מילוי לא מעודכנת אחרי היצירה ואינה יכולה להיות מוצגת כראוי|באג|
|PSDNET-712|חזרה: Aspose.PSD 20.8.0 לא יכולה לפתוח קובץ|באג|
|PSDNET-714|בקובץ PSD ספציפי, שינוי גודל שכבת טקסט מעבד את ערכי המיקום|באג|

## **שינויים ציבוריים ב- API**
# **APIs חדשים:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.IsCustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HorizontalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VerticalMeshPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HorizontalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VerticalMeshPointUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PerspectiveOther
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Items
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PageNumber
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TotalPages
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.AntiAliasPolicy
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PlacedLayerType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.NonAffineTransformMatrix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Crop
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.FrameCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Resolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.ResolutionUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.FrameStepNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.FrameStepDenominator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DurationNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DurationDenominator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GeneratePlacedResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GenerateSmartEmbeddedResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartResourceCreator.GenerateSmartExternalResource
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ContentsBounds
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ContentsSource
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.Contents
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ContentType
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartObjectProvider
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ExportContents(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.LoadContents(Aspose.PSD.LoadOptions)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(Aspose.PSD.Image)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ReplaceContents(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.EmbedLinked
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.ConvertToLinked(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.RelinkToFile(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.UpdateModifiedContent
- T:Aspose.PSD.FileFormats.Psd.SmartObjectProvider
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.EmbedAllLinked
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.UpdateAllModifiedContent
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.Embedded
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.AvailableLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.UnavailableLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectType.LibraryLink
- P:Aspose.PSD.FileFormats.Psd.PsdImage.SmartObjectProvider

# **APIs שנמחקו:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.VOrder
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspective
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PerspectiveOther
- P:Asspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Crop
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Resolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.ResolutionUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.FrameStepDenominator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.DurationNumerator
- P:Aspose.PSD.File
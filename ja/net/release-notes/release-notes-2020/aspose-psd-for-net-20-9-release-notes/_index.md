---
title: Aspose.PSD for .NET 20.9 - リリースノート
type: docs
weight: 40
url: /ja/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}} 

このページには、[Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/) のリリースノートが含まれています。

{{% /alert %}} 

|**キー**|**概要**|**カテゴリ**|
| :- | :- | :- |
|PSDNET-408|SoLEResource（スマートオブジェクトレイヤーの外部リソース）のサポート|機能|
|PSDNET-614|リンクされたスマートオブジェクトのサポート|機能|
|PSDNET-615|埋め込まれたスマートオブジェクトのサポート|機能|
|PSDNET-690|指定されたPSDファイル内のテキストを更新して保存すると、特定のレイヤーと多くのテキストパラメータが変更される|不具合|
|PSDNET-696|FillLayer が作成後に更新されず、正しくレンダリングされない|不具合|
|PSDNET-712|リグレッション: Aspose.PSD 20.8.0 がファイルを開けない|不具合|
|PSDNET-714|特定のPSDファイルで、TextLayer のリサイズが位置値を壊す|不具合|

## **パブリックAPIの変更**
# **追加されたAPI:**
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

（この内容は続きます...）- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
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
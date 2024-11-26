---
title: Aspose.PSD for .NET 20.9 - 发行说明
type: docs
weight: 40
url: /zh/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}} 

本页面包含 [Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-408|支持 SoLEResource（智能对象层外部资源）|功能|
|PSDNET-614|支持链接的智能对象|功能|
|PSDNET-615|支持嵌入的智能对象|功能|
|PSDNET-690|更新给定 PSD 文件中的文本并保存将更改一些图层和许多文本参数|错误|
|PSDNET-696|创建后未更新 FillLayer，并且无法正确呈现|错误|
|PSDNET-712|回归：Aspose.PSD 20.8.0 无法打开文件|错误|
|PSDNET-714|在特定 PSD 文件中，调整 TextLayer 的大小会破坏位置值|错误|

## **公共 API 更改**
# **已添加的 API:**
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
... (此处省略部分内容)

## **使用示例:**
**PSDNET-408. 支持 SoLEResource（智能对象层外部资源）**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-614. 支持链接的智能对象**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-615. 支持嵌入的智能对象**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-690. 在给定 PSD 文件中更新文本并保存，将更改一些图层和许多文本参数**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-696. 创建后未更新 FillLayer，并且无法正确呈现**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-712. 回归：Aspose.PSD 20.8.0 无法打开文件**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-714. 在特定 PSD 文件中，调整 TextLayer 的大小会破坏位置值**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}**PSDNET-690. 在给定 PSD 文件中更新文本并保存，将更改一些图层和许多文本参数**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-696. 创建后未更新 FillLayer，并且无法正确呈现**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-712. 回归：Aspose.PSD 20.8.0 无法打开文件**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
**PSDNET-714. 在特定 PSD 文件中，调整 TextLayer 的大小会破坏位置值**
{{< highlight csharp >}}
(部分代码已省略)
{{< /highlight >}}
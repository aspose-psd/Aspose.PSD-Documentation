---
title: Примітки до версії Aspose.PSD для .NET 19.2
type: docs
weight: 110
url: /uk/net/aspose-psd-for-net-19-2-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до версії Aspose.PSD для .NET 19.2

{{% /alert %}} 

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-97|Додана підтримка шарів заливки: заливка кольором|Функціонал|
|PSDNET-98|Додана підтримка шарів заливки: градієнтна заливка|Функціонал|
|PSDNET-105|Підтримка GdFlResource|Функціонал|
|PSDNET-106|Підтримка VmskResource|Функціонал|
|PSDNET-109|Перенесення фактичних джерел Aspose.Imaging в Aspose.PSD|Покращення|
|PSDNET-92|Додано підтримку часткового завантаження для деяких методів|Покращення|
|PSDNET-110|Падіння продуктивності PSD кілька разів|Помилка|

## **Зміни в публічному API**
# **Додані API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillType
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientName
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Gradient
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType.Pattern
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IColorFillSettings.Color
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.TransparencyPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint.MedianPointLocation
- M:Aspose.PSD.Extensions.RectangleExtensions.UnionWith(Aspose.PSD.RectangleF,Aspose.PSD.RectangleF)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Points
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.#ctor(System.Byte[])
- P:Aspose.P```java
.public PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.IsOpen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathFillRuleRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecord.Type
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.ProducePathRecord(System.Byte[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClosedSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathLengthRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotLinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.OpenSubpathBezierKnotUnlinked
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.PathFillRuleRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.ClipboardRecord
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathType.InitialFillRuleRecord
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillLayerResource.Signature
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientInterval
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.AlignWithLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Tr...
```
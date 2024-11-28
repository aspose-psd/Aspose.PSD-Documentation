---
title: Notas de la versión Aspose.PSD para .NET 19.2
type: docs
weight: 110
url: /es/net/aspose-psd-para-net-19-2-notas-de-version/
---

{{% alert color="primary" %}} 

Esta página contiene notas de la versión para Aspose.PSD para .NET 19.2

{{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-97|Agregar soporte de capas de relleno: Relleno de color|Funcionalidad|
|PSDNET-98|Agregar soporte de capas de relleno: Relleno de degradado|Funcionalidad|
|PSDNET-105|Soporte de GdFlResource|Funcionalidad|
|PSDNET-106|Soporte de VmskResource|Funcionalidad|
|PSDNET-109|Portar las fuentes reales de Aspose.Imaging a Aspose.PSD|Mejora|
|PSDNET-92|Agregar soporte de carga parcial para algunos métodos|Mejora|
|PSDNET-110|El rendimiento de PSD bajó varias veces|Error|

## **Cambios en la API pública**
# **APIs agregadas:**
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
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.ClipboardRecord.Type
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
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.TransparencyPoints
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddColorPoint
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AddTransparencyPoint
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Linear
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Radial
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Angle
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Reflected
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.Diamond
- F:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientType.ShapeBurst
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GenerateLfx2ResourceNodes
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Color
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FontSettings.UpdateFonts
- T:Aspose.PSD.ImageOptions.CmxRasterizationOptions
- M:Aspose.PSD.ImageOptions.CmxRasterizationOptions.#ctor
- P:Aspose.PSD.ImageOptions.CmxRasterizationOptions.Positioning
- T:Aspose.PSD.ImageOptions.PositioningTypes
- F:Aspose.PSD.ImageOptions.PositioningTypes.DefinedByDocument
- F:Aspose.PSD.ImageOptions.PositioningTypes.DefinedByOptions
- F:Aspose.PSD.ImageOptions.PositioningTypes.Relative
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.SmoothingMode
- T:Aspose.PSD.Interfaces.IObjectWithSizeF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.SizeF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.WidthF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.HeightF
- T:Aspose.PSD.VectorImage
- M:Aspose.PSD.VectorImage.#ctor
- P:Aspose.PSD.VectorImage.SizeF
- P:Aspose.PSD.VectorImage.WidthF
- P:Aspose.PSD.VectorImage.HeightF
- P:Aspose.PSD.VectorImage.Width
- P:Aspose.PSD.VectorImage.Height
# **APIs eliminadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType 
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

## **Ejemplos de uso:**
**PSDNET-97. Agregar soporte de capas de relleno: Relleno de color**

{{< highlight java >}}

 // Agregar soporte de capas de relleno: Relleno de color

string nombreArchivo = "CapaRellenoDeColor.psd";

string rutaExportada = "CapaRellenoDeColor_salida.psd";

string rutaExportadaPng = "CapaRellenoDeColor_salida.png";

var imagenPSD = (PsdImage) Image.Load(nombreArchivo);

    using(imagenPSD) {

     foreach(var capa in imagenPSD.Layers) {

      if (capa is FillLayer) {

       var capaRelleno = (FillLayer) capa;

       if (capaRelleno.FillSettings.FillType != FillType.Color) {

        throw new Exception("Capa de relleno incorrecta");

       }

       var ajustes = (IColorFillSettings) capaRelleno.FillSettings;

       ajustes.Color = Color.Red;

       capaRelleno.Update(); 

       imagenPSD.Save(rutaExportada);  

       break;

      }

     }

    }


{{< /highlight >}}

**PSDNET-98. Agregar soporte de capas de relleno: Relleno de degradado**

{{< highlight java >}}

 // Soporte de Capa de Relleno de Degradado

string nombreArchivo = "CapaRellenoDegradadoComplejo.psd";

string archivoSalida = "CapaRellenoDegradadoComplejo_salida.psd";

var imagenPSD = (PsdImage) Image.Load(nombreArchivo);

    using(imagenPSD) {

     foreach(var capa in imagenPSD.Layers) {

      if (capa is FillLayer) {

       var capaRelleno = (FillLayer) capa;

       if (capaRelleno.FillSettings.FillType != FillType.Gradient) {

        throw new Exception("Capa de relleno incorrecta");

       }

       var ajustes = (IGradientFillSettings) capaRelleno.FillSettings;

       if (
          Math.Abs(ajustes.Angle - 45) > 0.25 ||
          ajustes.Dither != true ||
          ajustes.AlignWithLayer != false ||
          ajustes.Reverse != false ||
          Math.Abs(ajustes.HorizontalOffset - (-39)) > 0.25 ||
          Math.Abs(ajustes.VerticalOffset - (-5)) > 0.25 ||
          ajustes.TransparencyPoints.Length != 3 ||
          ajustes.ColorPoints.Length != 2 ||
          Math.Abs(100.0 - ajustes.TransparencyPoints[0].Opacity) > 0.25 ||
          ajustes.TransparencyPoints[0].Location != 0 ||
          ajustes.TransparencyPoints[0].MedianPointLocation != 50 ||
          ajustes.ColorPoints[0].Color != Color.FromArgb(203, 64, 140) ||
          ajustes.ColorPoints[0].Location != 0 ||
          ajustes.ColorPoints[0].MedianPointLocation != 50
         ) {

        throw new Exception("El relleno de degradado no se leyó correctamente");

       }

       ajustes.Angle = 0.0;
       ajustes.Dither = false;
       ajustes.AlignWithLayer = true;
       ajustes.Reverse = true;
       ajustes.HorizontalOffset = 25;
       ajustes.VerticalOffset = -15;

      var colorPoints = new List < IGradientColorPoint > (ajustes.ColorPoints);
      var transparencyPoints = new List < IGradientTransparencyPoint > (ajustes.TransparencyPoints);

      colorPoints.Add(new GradientColorPoint() {
        Color = Color.Violet,
        Location = 4096,
        MedianPointLocation = 75
      });

      colorPoints[1].Location = 3000;

      transparencyPoints.Add(new GradientTransparencyPoint() {
        Opacity = 80.0,
        Location = 4096,
        MedianPointLocation = 25
      });

      transparencyPoints[2].Location = 3000;

      ajustes.ColorPoints = colorPoints.ToArray();
      ajustes.TransparencyPoints = transparencyPoints.ToArray();

      capaRelleno.Update();

      imagenPSD.Save(archivoSalida, new PsdOptions(imagenPSD));
      break;
     }
    }
  }

{{< /highlight >}}
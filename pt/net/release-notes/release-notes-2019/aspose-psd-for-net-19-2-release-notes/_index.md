---
title: Notas de Lançamento Aspose.PSD para .NET 19.2
type: docs
weight: 110
url: /pt/net/aspose-psd-for-net-19-2-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém as notas de lançamento do Aspose.PSD para .NET 19.2

{{% /alert %}} 

| **Chave** | **Resumo** | **Categoria** |
| :- | :- | :- |
| PSDNET-97 | Adicionar suporte para camadas de Preenchimento: Preenchimento de Cor | Recurso |
| PSDNET-98 | Adicionar suporte para camadas de Preenchimento: Preenchimento de Gradiente | Recurso |
| PSDNET-105 | Suporte do recurso GdFlResource | Recurso |
| PSDNET-106 | Suporte do recurso VmskResource | Recurso |
| PSDNET-109 | Portando as fontes reais do Aspose.Imaging para o Aspose.PSD | Aprimoramento |
| PSDNET-92 | Adicionado suporte para carregamento parcial para alguns métodos | Aprimoramento |
| PSDNET-110 | O desempenho do PSD caiu várias vezes | Correção de erro |

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.FillType
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.Atualizar
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradienteFillSettings.GradientName
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
- M:Aspose.PSD.Extensions.RectangleExtensions.UnirCom(Aspose.PSD.RectangleF,Aspose.PSD.RectangleF)
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
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorPathRecordFactory.GerarRegistroDoCaminho(System.Byte[])
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
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Salvar(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.TipoFerramentaKey
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
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Salvar(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.TipoFerramentaKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.VerticalOffset
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.Salvar(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoCoResource.TipoFerramentaKey
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
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.TransparencyPoints
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AdicionarPontoDeCor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.AdicionarPontoDeTransparência
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
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoverPontoDeTransparência(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.RemoverPontoDeCor(Aspose.PSD.FileFormats.Psd.Layers.IGradientColorPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientTransparencyPoint.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.GerarNósDeRecursoLfx2
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Cor
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.SubstituirQuadro(Sistema.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FontSettings.AtualizarFontes
- T:Aspose.PSD.ImageOptions.CmxRasterizationOptions
- M:Aspose.PSD.ImageOptions.CmxRasterizationOptions.#ctor
- P:Aspose.PSD.ImageOptions.CmxRasterizationOptions.Posicionamento
- T:Aspose.PSD.ImageOptions.TipoPosicionamento
- F:Aspose.PSD.ImageOptions.TipoPosicionamento.DefinidoPeloDocumento
- F:Aspose.PSD.ImageOptions.TipoPosicionamento.DefinidoPelasOpções
- F:Aspose.PSD.ImageOptions.TipoPosicionamento.Relativo
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.ModoSuavização
- T:Aspose.PSD.Interfaces.IObjectWithSizeF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.SizeF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.LarguraF
- P:Aspose.PSD.Interfaces.IObjectWithSizeF.AlturaF
- T:Aspose.PSD.VectorImage
- M:Aspose.PSD.VectorImage.#ctor
- P:Aspose.PSD.VectorImage.SizeF
- P:Aspose.PSD.VectorImage.LarguraF
- P:Aspose.PSD.VectorImage.AlturaF
- P:Aspose.PSD.VectorImage.Largura
- P:Aspose.PSD.VectorImage.Altura
# **APIs Removidas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation
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
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AdicionarPontoDeCor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AdicionarPontoDeTransparência
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoverPontoDeTransparência(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoverPontoDeCor(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)
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
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.Linear
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.Radial
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.Angle
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.Refletido
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.Diamante
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.TipoGradiente.ExplosãoDeForma
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GerarNósDeRecursoLfx2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Cor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GerarNósDeRecursoLfx2(Sistema.String,Aspose.PSD.Color,Sistema.String,Sistema.String,Sistema.Duplo,Sistema.Boolean,Aspose.PSD.PointF)

## **Exemplos de Uso:**
**PSDNET-97. Adicionar suporte para camadas de Preenchimento: Preenchimento de Cor**

{{< highlight java >}}

 // Adicionar suporte para camadas de Preenchimento: Preenchimento de Cor

string nomeArquivoFonte = "CamadaPreenchimentoCor.psd";

string caminhoExportacao = "resultadoCamadaPreenchimentoCor.psd";

string caminhoExportacaoPng = "resultadoCamadaPreenchimentoCor.png";

var im = (PsdImage) Image.Load(nomeArquivoFonte);

using(im) {

 foreach(var camada in im.Layers) {

  if (camada is FillLayer) {

   var camadaPreenchimento = (FillLayer) camada;

   if (camadaPreenchimento.FillSettings.FillType != FillType.Color) {

    throw new Exception("Tipo de Preenchimento Errado");

   }

   var configurações = (IColorFillSettings) camadaPreenchimento.FillSettings;

   configurações.Color = Color.Red;

   camadaPreenchimento.Atualizar(); 

   im.Save(caminhoExportacao);

   break;

  }

 }

}


{{< /highlight >}}

**PSDNET-98. Adicionar suporte para camadas de Preenchimento: Preenchimento de Gradiente**

{{< highlight java >}}

 // Suporte para Camada de Preenchimento Gradiente

string nomeArquivoFonte = "CamadaPreenchimentoGradienteComplexo.psd";

string arquivoSaida = "CamadaPreenchimentoGradienteComplexo_saida.psd";

var im = (PsdImage) Image.Load(nomeArquivoFonte);

using(im) {

 foreach(var camada in im.Layers) {

  if (camada is FillLayer) {

   var camadaPreenchimento = (FillLayer) camada;

   if (camadaPreenchimento.FillSettings.FillType != FillType.Gradient) {

    throw new Exception("Tipo de Preenchimento Errado");

   }

   var configurações = (IGradientFillSettings) camadaPreenchimento.FillSettings;

   if (

    Math.Abs(configurações.Angle - 45) > 0.25 ||

    configurações.Dither != true ||

    configurações.AlignWithLayer != false ||

    configurações.Reverse != false ||

    Math.Abs(configurações.HorizontalOffset - (-39)) > 0.25 ||

    Math.Abs(configurações.VerticalOffset - (-5)) > 0.25 ||

    configurações.TransparencyPoints.Length != 3 ||

    configurações.ColorPoints.Length != 2 ||

    Math.Abs(100.0 - configurações.TransparencyPoints[0].Opacity) > 0.25 ||

    configurações.TransparencyPoints[0].Location != 0 ||

    configurações.TransparencyPoints[0].MedianPointLocation != 50 ||

    configurações.ColorPoints[0].Color != Color.FromArgb(203, 64, 140) ||

    configurações.ColorPoints[0].Location != 0 ||

    configurações.ColorPoints[0].MedianPointLocation != 50) {

    throw new Exception("Preenchimento Gradiente foi lido incorretamente");

   }

   configurações.Angle = 0.0;

   configurações.Dither = false;

   configurações.AlignWithLayer = true;

   configurações.Reverse = true;

   configurações.HorizontalOffset = 25;

   configurações.VerticalOffset = -15;

   var pontosDeCor = new List < IGradientColorPoint > (configurações.ColorPoints);

   var pontosDeTransparência = new List < IGradientTransparencyPoint > (configurações.TransparencyPoints);

   pontosDeCor.Add(new GradientColorPoint() {

    Color = Color.Violet,

     Location = 4096,

     MedianPointLocation = 75

   });

   pontosDeCor[1].Location = 3000;

   pontosDeTransparência.Add(new GradientTransparencyPoint() {

    Opacity = 80.0,

     Location = 4096,

     MedianPointLocation = 25

   });

   pontosDeTransparência[2].Location = 3000;

   configurações.ColorPoints = pontosDeCor.ToArray();

   configurações.TransparencyPoints = pontosDeTransparência.ToArray();

   camadaPreenchimento.Atualizar();

   im.Save(arquivoSaida, new PsdOptions(im));

   break;

  }

 }

}

{{< /highlight >}}

**PSDNET-105. Suporte do recurso GdFlResource**

{{< highlight java >}}

 // Suporte do recurso GdFlResource

string nomeArquivoFonte = "CamadaPreenchimentoGradienteComplexo.psd";

string caminhoExportacao = "CamadaPreenchimentoGradienteComplexo_após.psd";

var im = (PsdImage) Image.Load(nomeArquivoFonte);

using(im) {

 foreach(var camada in im.Layers) {

  if (camada is FillLayer) {

   var camadaPreenchimento = (FillLayer) camada;

   var recursos = camadaPreenchimento.Resources;

   foreach(var res in recursos) {

    if (res is GdFlResource) {

     // Leitura

     var recurso = (GdFlResource) res;

     if (recurso.AlignWithLayer != false ||

      (Math.Abs(recurso.Angle - 45.0) > 0.001) ||

      recurso.Dither != true ||

      recurso.Reverse != false ||

      recurso.Color != Color.Empty ||

      Math.Abs(recurso.HorizontalOffset - (-39)) > 0.001 ||

      Math.Abs(recurso.VerticalOffset - (-5)) > 0.001 ||

      recurso.TransparencyPoints.Length != 3 ||

      recurso.ColorPoints.Length != 2) {

      throw new Exception("Parâmetros do Recurso foram lidos incorretamente");

     }

     var pontosDeTransparência = recurso.TransparencyPoints;

     if (Math.Abs(100.0 - pontosDeTransparência[0].Opacity) > 0.25 ||

      pontosDeTransparência[0].Location != 0 ||

      pontosDeTransparência[0].MedianPointLocation != 50 ||

      Math.Abs(50.0 - pontosDeTransparência[1].Opacity) > 0.25 ||

      pontosDeTransparência[1].Location != 2048 ||

      pontosDeTransparência[1].MedianPointLocation != 50 ||

      Math.Abs(100.0 - pontosDeTransparência[2].Opacity) > 0.25 ||

      pontosDeTransparência[2].Location != 4096 ||

      pontosDeTransparência[2].MedianPointLocation != 50) {

      throw new Exception("Pontos de Transparência de Gradiente foram lidos incorretamente");

     }

     var pontosDeCor = recurso.ColorPoints;

     if (pontosDeCor[0].Color != Color.FromArgb(203, 64, 140) ||

      pontosDeCor[0].Location != 0 ||

      pontosDeCor[0].MedianPointLocation != 50 ||

      pontosDeCor[1].Color != Color.FromArgb(203, 0, 0) ||

      pontosDeCor[1].Location != 4096 ||

      pontosDeCor[1].MedianPointLocation != 50) {

      throw new Exception("Pontos de Cor de Gradiente foram lidos incorretamente");

     }

     // Edição

     recurso.Angle = 30.0;

     recurso.Dither = false;

     recurso.AlignWithLayer = true;

     recurso.Reverse = true;

     recurso.HorizontalOffset = 25;

     recurso.VerticalOffset = -15;

     var novosPontosDeCor = new List < IGradientColorPoint > (recurso.ColorPoints);

     var

      novosPontosDeTransparência = new

     List < IGradientTransparencyPoint > (recurso.TransparencyPoints);

     novosPontosDeCor.Add(new GradientColorPoint() {

      Color = Color.Violet,

       Location = 4096,

       MedianPointLocation = 75

     });

     pontosDeCor[1].Location = 3000;

     novosPontosDeTransparência.Add(new GradientTransparencyPoint() {

      Opacity = 80.0,

       Location = 4096,

       MedianPointLocation = 25

     });

     pontosDeTransparência[2].Location = 3000;

     recurso.ColorPoints = novosPontosDeCor.ToArray();

     recurso.TransparencyPoints = novosPontosDeTransparência.ToArray();

     im.Save(caminhoExportacao);

    }

    break;

   }

   break;

  }

 }

}   

{{< /highlight >}}

**PSDNET-110. O desempenho do PSD caiu várias vezes**

{{< highlight java >}}

  // O desempenho do PSD caiu várias vezes

string nomeArquivoFonte = "1.psd";

string nomeArquivoPng = "imagem3203.png";

string nomeArquivoPsd = "imagem3203.psd";

var cronômetro = new Stopwatch();

using(PsdImage imagem = Image.Load(nomeArquivoFonte) as PsdImage) {

 cronômetro.Start();

 imagem.Save(nomeArquivoPng, new PngOptions() {

  TipoCor = PngColorType.TruecolorWithAlpha

 });

 imagem.Save(nomeArquivoPsd, new PsdOptions());

 cronômetro.Stop();

}

Console.WriteLine("DECORRIDO: ", cronômetro.Elapsed);

{{< /highlight >}}
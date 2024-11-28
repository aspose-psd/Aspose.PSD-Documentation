---
title: Aspose.PSD for .NET 18.12 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-net-18-12-release-notes/
---

|**키**|**개요**|**카테고리**|
| :- | :- | :- |
|PSDNET-76|스트로크 레이어 지원|기능|
|PSDNET-83|그라데이션 효과 지원|기능|
|PSDNET-84|패턴 효과 지원|기능|
|PSDNET-89|PsdImage에 새로 생성된 레귤러 레이어를 추가할 수 있는 기능|기능|
|PSDNET-93|텍스트 레이어의 내용을 \(백슬래시\) 문자로 업데이트한 후 Photoshop에서 결과 파일을 열 수 없음|버그|
|PSDNET-39|CMYK 색상 모드에서 이미지 데이터가 오버사이즈로 일어난 이미지 내보내기 후 깨지는 이미지|버그|
|PSDNET-52|가능: PSD에서 회전이 작동하지 않음|버그|
|PSDNET-88|가능: Aspose.Psd의 크롭 메서드가 작동하지 않음|버그|
|PSDNET-91|Aspose.Imaging의 변경사항을 Aspose.PSD에 적용|개선|

## **공개 API 변경**
메소드    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

클래스    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

메소드    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

메소드    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

클래스    Aspose.PSD.FileFormats.Psd```java
.Layers.LayerResources.Lfx2Resources.GradientType

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

필드/열거    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

메소드    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

클래스    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

속성    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity
```
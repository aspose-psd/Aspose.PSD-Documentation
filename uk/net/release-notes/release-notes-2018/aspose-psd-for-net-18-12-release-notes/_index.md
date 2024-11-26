---
title: Примітки до версії Aspose.PSD for .NET 18.12
type: docs
weight: 10
url: /uk/net/aspose-psd-for-net-18-12-release-notes/
---

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-76|Підтримка шару обводки|Функціонал|
|PSDNET-83|Підтримка ефекту градієнту|Функціонал|
|PSDNET-84|Підтримка ефекту візерунку|Функціонал|
|PSDNET-89|Додано можливість додавати в PsdImage нове згенероване звичайне зображення|Функціонал|
|PSDNET-93|Після оновлення вмісту текстового шару символом \ (зворотний слеш) створений файл не може бути відкритий у Photoshop|Помилка|
|PSDNET-39|Пошкоджені зображення після експорту з надмірними даними зображення у режимі кольорів CMYK|Помилка|
|PSDNET-52|Можливість: Поворот у PSD не працює|Помилка|
|PSDNET-88|Можливість: Методи обрізки в Aspose.Psd не працюють|Помилка|
|PSDNET-91|Застосувати зміни Aspose.Imaging до Aspose.PSD|Покращення|

## **Зміни у загальнодоступному API**
Метод    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Клас    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Метод    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Метод    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Поле/Перерахування    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Клас    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Властивість    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity
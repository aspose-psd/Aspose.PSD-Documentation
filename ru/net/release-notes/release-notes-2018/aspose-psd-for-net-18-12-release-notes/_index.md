---
title: Выпуск Aspose.PSD для .NET 18.12 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-for-net-18-12-release-notes/
---

|**Ключ**|**Сводка**|**Категория**|
| :- | :- | :- |
|PSDNET-76|Поддержка слоя обводки|Функция|
|PSDNET-83|Поддержка градиентного эффекта|Функция|
|PSDNET-84|Поддержка эффекта узора|Функция|
|PSDNET-89|Возможность добавления вновь созданного обычного слоя в PsdImage|Функция|
|PSDNET-93|После обновления содержимого текстового слоя с символом \ (обратная косая черта), файл не удается открыть в Photoshop|Ошибка|
|PSDNET-39|Испорченные изображения после экспорта с избыточными данными изображения в CMYK Color Mode|Ошибка|
|PSDNET-52|Возможно: Вращение в PSD не работает|Ошибка|
|PSDNET-88|Возможно: Методы обрезки в Aspose.Psd не работают|Ошибка|
|PSDNET-91|Применить изменения Aspose.Imaging к Aspose.PSD|Улучшение|

## **Изменения в публичном API**
Метод    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Класс    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Метод    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Метод    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Поле/Перечисление    Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Метод    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Класс    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Свойство    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Примеры использования:**
**PSDNET-76. Поддержка слоя обводки**

**1) Тип заполнения - Узор**

{{< highlight java >}}

     // Эффект обводки. Тип заполнения - Узор. Пример

     // Код на Java

{{< /highlight >}}

**Тип заполнения - Градиент**

{{< highlight java >}}

     // Эффект обводки. Тип заполнения - Градиент. Пример

     // Код на Java

{{< /highlight >}}

**Тип заполнения - Цвет**

{{< highlight java >}}

     // Эффект обводки. Тип заполнения - Цвет. Пример

     // Код на Java

{{< /highlight >}}

**PSDNET-83. Поддержка градиентного эффекта**

{{< highlight java >}}

     // Эффект градиентного наложения. Пример

     // Код на Java

{{< /highlight >}}

**PSDNET-84. Поддержка эффекта узора**

{{< highlight java >}}

     // Эффект наложения узора. Пример

     // Код на Java

{{< /highlight >}}

**PSDNET-89. Возможность добавления в PsdImage вновь созданного обычного слоя**

{{< highlight java >}}

  // Возможность добавлять в PsdImage вновь созданный обычный слой
  
     // Java код
     
{{< /highlight >}}

**PSDNET-93. После обновления содержимого текстового слоя с символом \ (обратная косая черта), файл не удается открыть в Photoshop**

{{< highlight java >}}

  // Java код
  
{{< /highlight >}}

**PSDNET-39. Испорченные изображения после экспорта с избыточными данными изображения в CMYK Color Mode**

{{< highlight java >}}

     // Испорченные изображения после экспорта с избыточными данными изображения в CMYK Color Mode. Пример

     // Код на Java

{{< /highlight >}}

**~ PSDNET-52. Возможно: Вращение в PSD не работает**

{{< highlight java >}}

  // Вращение в PSD. Пример

     // Код на Java
     
{{< /highlight >}}

**PSDNET-88. Возможно: Методы обрезки в Aspose.Psd не работают**

{{< highlight java >}}

   // Возможно: Методы обрезки в Aspose.Psd не работают

    // Код на Java

{{< /highlight >}}
**Usage examples (continued):**

**PSDNET-91. Apply changes of Aspose.Imaging to Aspose.PSD**

{{< highlight java >}}

  // Java code

{{< /highlight >}}

**Public API Changes (continued):**

Class    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayerMethod

Class    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Method    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Field/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Method    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Class    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Property    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity
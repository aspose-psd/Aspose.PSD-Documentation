---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 18.12
type: docs
weight: 10
url: /fa/net/aspose-psd-for-net-18-12-release-notes/
---

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-76|پشتیبانی از لایه Stroke|ویژگی|
|PSDNET-83|پشتیبانی از افکت Gradient|ویژگی|
|PSDNET-84|پشتیبانی از افکت Pattern|ویژگی|
|PSDNET-89|قابلیت اضافه کردن لایه معمولی تازه تولید شده به PsdImage|ویژگی|
|PSDNET-93|پس از به‌روزرسانی محتوای لایه متن با کاراکتر \ (بک‌اسلش)، فایل نهایی نمی‌تواند در فتوشاپ باز شود|اشکال|
|PSDNET-39|تصاویر خراب شده پس از صادرات با داده تصویر بزرگ در حالت رنگ CMYK|اشکال|
|PSDNET-52|احتمالی: چرخش در PSD کار نمی‌کند|اشکال|
|PSDNET-88|احتمالی: متدهای بریدن در Aspose.Psd کار نمی‌کند|اشکال|
|PSDNET-91|اعمال تغییرات Aspose.Imaging به Aspose.PSD|بهبود|

## **تغییرات API عمومی**
متد    Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

کلاس    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

متد    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

متد    Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

متد    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

فیلد/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

فیلد/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

فیلد/Enum    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

...

...
کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

متد    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

متد    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

متد    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

متد    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

کلاس    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

خاصیت    Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

...

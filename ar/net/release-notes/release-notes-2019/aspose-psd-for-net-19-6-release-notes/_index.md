---
title: ملاحظات الإصدار Aspose.PSD for .NET 19.6
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-19-6-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

** 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-127|القدرة على تحويل ملف PSD إلى PSB والعكس|ميزة|
|PSDNET-154|نقل مصادر Aspose.Imaging 19.5 إلى Aspose.PSD|تعزيز|
|PSDNET-155|تنظيف واجهة برمجة التطبيقات العامة ذات الصلة بـ Aspose.PSD|تعزيز|
|PSDNET-159|إزالة خاصية IsLicensed|تعزيز|
|PSDNET-102|تعلق تحويل PSB إلى JPG|خلل|
|PSDNET-150|تحديث موضع طبقة النص المضافة حديثًا ينقلب أثناء التحرير في Photoshop|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة APIs:**
- T: Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F: Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F: Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P: Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F: Aspose.PSD.FileFormat.Cdr
- F: Aspose.PSD.FileFormat.Cmx
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P: Aspose.PSD.Image.BufferSizeHint
- P: Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P: Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M: Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P: Aspose.PSD.LoadOptions.BufferSizeHint
- T: Aspose.PSD.MemoryManagement.Configuration
- P: Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T: Aspose.PSD.ResolutionUnit
- F: Aspose.PSD.ResolutionUnit.None
- F: Aspose.PSD.ResolutionUnit.Inch
- F: Aspose.PSD.ResolutionUnit.Cm
# **تمت إزالة APIs:**
- M: Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M: Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M: Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M: Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T: Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M: Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P: Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P: Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- ...

## **أم
---
title: Aspose.PSD لـ .NET 20.7 - ملاحظات الإصدار
type: docs
weight: 60
url: /ar/net/aspose-psd-for-net-20-7-release-notes/
---

{{% alert color="primary" %}} 

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 20.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-673|دعم مورد LnkE|ميزة|
|PSDNET-392|دعم britResource (مورد للتوهّج/تناسب طبقة التعديل)|ميزة|
|PSDNET-629|تغيير رسالة الاستثناء عند محاولة فتح تنسيقات غير مدعومة كصورة|تحسين|
|PSDNET-594|فشل في حفظ LayerMask|خلل|
|PSDNET-597|إذا قمنا بحفظ ملف PSD بعد إنشاء مجموعة طبقة جديدة نحصل على تحذير من Photoshop عند فتح الملف|خلل|
|PSDNET-618|قناع القص لا يُطبق على المجلد|خلل|
|PSDNET-625|تعذّر فتح الملف بـ Aspose.PSD لـ .NET|خلل|
|PSDNET-650|استثناء فشل في حفظ الصورة عند تحويل PSD إلى PDF|خلل|
|PSDNET-655|عملية rop تجعل مسار Clipping غير صالح في صورة PSD|خلل|
|PSDNET-662|استثناء الإشارة المباشرة عند محاولة حفظ ملف PSD محدد بمعين مع تأثير الظل|خلل|
|PSDNET-666|تعيد Aspose.PSD القيمة true عند Image.CanLoad(pdfStream)|خلل|
|PSDNET-676|الطبقات تفشل في التقديم في PNG الذي تم إنشاؤه|خلل|
|PSDNET-677|استثناء عند الوصول إلى TextData|خلل|
|PSDNET-679|استثناء إدخال الصورة عند حفظ PSD|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المُضافة:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Overprint
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Position
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Size
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Inside
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Center
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokePosition.Outside
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk3Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource
- M:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.Version
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Resources.WorkingPathResource.IsInverted
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.IVectorPathData.IsInverted

# **APIs المُلغاة:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddExposureLayer(System.Single,System.Single,System.Single)

## **أمثلة الاستخدام:**
**PSDNET-606. دعم مورد LnkE**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual)
 {
     if (!object.Equals(actual, expected))
     {
         throw new FormatException(string.Format("قيمة الواقعية {0} لا تساوي المتوقعة {1}.", actual, expected));
     }
 .... النص طويل ....
{{< /highlight >}}
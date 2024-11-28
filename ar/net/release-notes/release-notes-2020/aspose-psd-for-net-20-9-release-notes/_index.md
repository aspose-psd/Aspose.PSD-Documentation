---
title: ملاحظات الإصدار لـ Aspose.PSD for .NET 20.9
type: docs
weight: 40
url: /ar/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-408|دعم لـ SoLEResource (مورد الطبقة الذكية الخارجية)|ميزة|
|PSDNET-614|دعم للكائنات الذكية المرتبطة|ميزة|
|PSDNET-615|دعم للكائنات الذكية المضمنة|ميزة|
|PSDNET-690|تحديث النص في ملف PSD معين وحفظ التغييرات تؤدي إلى تغيير بعض الطبقات والعديد من معلمات النص|خلل|
|PSDNET-696|طبقة FillLayer لا تُحدَّث بعد الإنشاء ولا يمكن عرضها بشكل صحيح|خلل|
|PSDNET-712|انحدار: يتعذر على Aspose.PSD 20.8.0 فتح الملف|خلل|
|PSDNET-714|في ملف PSD محدد، تكسير قيمة موقع طبقة النص أثناء تغيير الحجم|خلل|

## **تغييرات الواجهة البرمجية العامة**
# **تمت إضافة واجهات برمجة تطبيقات جديدة:**
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
- ... (القائمة مستمرة)

## **أمثلة الاستخدام:**

**PSDNET-408. دعم SoLEResource (مورد الطبقة الذكية الخارجية)**
{{< highlight csharp >}}
            // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-614. دعم الكائنات الذكية المرتبطة**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-615. دعم الكائنات الذكية المضمنة**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-690. تحديث النص في ملف PSD معين وحفظ التغييرات تؤدي إلى تغيير بعض الطبقات والعديد من معلمات النص**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-696. طبقة FillLayer لا تُحدَّث بعد الإنشاء ولا يمكن عرضها بشكل صحيح**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-712. انحدار: Aspose.PSD 20.8.0 يتعذر فتح الملف**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}

**PSDNET-714. في ملف PSD محدد، تكسير قيمة موقع طبقة النص أثناء تغيير الحجم**
{{< highlight csharp >}}
        // يتم كتابة مثال الاستخدام لهنا
{{< /highlight >}}
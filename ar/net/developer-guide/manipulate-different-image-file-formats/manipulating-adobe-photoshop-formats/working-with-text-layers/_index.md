---
title: العمل مع طبقات النص
type: docs
weight: 170
url: /ar/net/working-with-text-layers/
---

## **إضافة طبقة نص**
يتيح لك Aspose.PSD لـ .NET إضافة طبقة نص في ملف PSD. تكوين خطوات إضافة طبقة نص في ملف PSD بسيط كما يلي:

- قم بتحميل ملف PSD كصورة باستخدام الطريقة الثابتة [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) التي يتم الكشف عنها بواسطة فئة [Image class](https://reference.aspose.com/psd/net/aspose.psd/image)
- اتصل بالأسلوب [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) الذي يقبل نصًا ومثيلًا من فئة [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- احفظ النتائج

يوضح مقطع الكود التالي كيفية إضافة طبقة نص في ملف PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **تعيين موقع الطبقة النصية**
يتيح لك Aspose.PSD لـ .NET تحديد موقع طبقة نص في ملف PSD. تكوين خطوات تحديد موقع طبقة النص في ملف PSD بسيط كما يلي:

- قم بتحميل ملف PSD كصورة باستخدام الطريقة الثابتة Load التي تم الكشف عنها بواسطة فئة Image
- اتصل بالأسلوب AddTextLayer مع تحديد مواقع اليسار والأعلى لطبقة النص
- احفظ النتائج

يوضح مقطع الكود التالي كيفية تعيين موقع طبقة النص في ملف PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}

## **الحصول على خصائص النص من طبقة نص**
مع استخدام Aspose.PSD لـ .NET ، يمكنك الحصول على وتحديث خصائص النصوص المختلفة المتاحة في طبقة نص PSD. يوضح هذا المقال كيفية الحصول على فقرات وأنماط النص وخصائص النص من الطبقة النصية وتحديثها.

يوضح مقطع الكود أدناه كيفية تحقيق هذه المتطلبات.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}

اليك مثالًا آخر يوضح كيف يمكن للمطور الحصول على تنسيق النصوص المختلفة من [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) باستخدام [Aspose.PSD لـ .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}

## **تحديث طبقة النص في ملف PSD**
تتيح لك Aspose.PSD لـ .NET تلاعب النص في طبقة النص في ملف PSD. يرجى استخدام فئة Aspose.PSD.FileFormats.Psd.Layers.TextLayer لتحديث النص في طبقة PSD. يحمل مقطع الكود التالي ملف PSD ، يصل إلى طبقة النص ، يحدث النص ويحفظ ملف PSD باسم جديد باستخدام الأسلوب [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **دعم طبقات النص على مدار الوقت التشغيلي**
يوضح هذا المقال كيفية إضافة طبقات نص على الطير لصور PSD. تم توفير مقطع الكود أدناه.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
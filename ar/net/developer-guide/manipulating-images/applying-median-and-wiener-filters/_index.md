---
title: تطبيق فلاتر الميديان وواينر
type: docs
weight: 10
url: /ar/net/applying-median-and-wiener-filters/
---

## **تطبيق فلاتر الميديان وواينر**
فلتر الميديان هو تقنية تصفية رقمية غير خطية، تُستخدم في كثير من الأحيان لإزالة الضوضاء. يُعتبر تقليل الضوضاء مثل هذا خطوة معالجة مسبقة نموذجية لتحسين نتائج المعالجة اللاحقة. فلتر واينر هو فلتر خطي ثابت يعتبر الأمثل بالنسبة لخطأ المربعات المتوسطة عندما تخضع الصور للتشويش الإضافي والتشويش بالضباب. باستخدام Aspose.PSD لمطوري واجهة برمجة التطبيقات لـ .NET يمكن تطبيق فلتر الميديان لتقليل الضوضاء على الصورة ويمكن تطبيق فلتر جوس واينر على الصور. يوضح هذا المقال كيف يمكن تطبيق فلتر الميديان وفلتر جوس واينر على الصور.

### **تطبيق فلتر الميديان**
توفر Aspose.PSD [فئة MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) لتطبيق فلتر على [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). يوضح قطعة الكود أدناه كيفية تطبيق فلتر الميديان على صورة نقطية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **تطبيق فلتر جاوس واينر**
توفر Aspose.PSD [فئة GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) لتطبيق فلتر على [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). يوضح قطعة الكود أدناه كيفية تطبيق فلتر جاوس واينر على صورة نقطية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **تطبيق فلتر جاوس واينر على صورة ملونة**
توفر Aspose.PSD [فئة GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) للصور الملونة أيضًا. يوضح قطعة الكود أدناه كيفية تطبيق فلتر جاوس واينر على صورة ملونة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **تطبيق فلتر واينر الحركي**
توفر Aspose.PSD [فئة MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) لتطبيق فلتر على [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). يوضح قطعة الكود أدناه كيفية تطبيق فلتر واينر الحركي على صورة نقطية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **تطبيق فلتر التصحيح على صورة**
يوضح هذا المقال استخدام Aspose.PSD لـ .NET لتنفيذ فلاتر التصحيح على صورة. فئات واجهة برمجة التطبيقات لـ Aspose.PSD قد عرضت طرقاً فعالة وسهلة للاستخدام لتحقيق هذا الهدف. لقد عرض Aspose.PSD لـ .NET [فئة BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) و [فئة SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) للتصفية. تتطلب فئة BilateralSmoothingFilterOptions عددًا صحيحًا كحجم. الخطوات لتنفيذ تغيير الحجم بسيطة كما يلي:

1. تحميل صورة باستخدام الطريقة الأساسية Load المعرضة من قبل فئة Image.
1. تحويل الصورة إلى RasterImage.
1. إنشاء مثيلات لفئة BilateralSmoothingFilterOptions و SharpenFilterOptions.
1. استدعاء طريقة [Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) من RasterImage مع تحديد المستطيل كحدود صورة ومثيل فئة BilateralSmoothingFilterOptions.
1. استدعاء طريقة [Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) من RasterImage مع تحديد المستطيل كحدود صورة ومثيل فئة SharpenFilterOptions.
1. ضبط التباين
1. تعيين سطوع
1. حفظ النتائج.


## **استخدام خوارزمية Bradley threshold**
يُستخدم تقنين الصورة في تطبيقات الرسومات. هدف تقنين الصورة هو تصنيف البكسلات إما كـ"مظلمة" أو "فاتحة". تسمح واجهة برمجة التطبيقات لـ Aspose.PSD باستخدام تقنية خوارزمية Bradley threshold أثناء تحويل الصور. تُظهر مقطع الكود التالي لك كيفية تحديد قيمة عتبة ثم استدعاء خوارزمية عتبة Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
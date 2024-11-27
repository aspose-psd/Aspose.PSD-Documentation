---
title: تطبيق فلتر المتوسط وفلتر وينر
type: docs
weight: 10
url: /ar/java/applying-median-and-wiener-filters/
---

## **تطبيق فلتر المتوسط وفلتر وينر**
يعد فلتر المتوسط تقنية تصفية رقمية غير خطية، وعادة ما يُستخدم لإزالة الضوضاء. إن تقليل هذه الضوضاء هو خطوة مسبقة نموذجية لتحسين نتائج المعالجة لاحقًا. فلتر وينر هو أمثلية خطية ثابتة للأخطاء بالمتوسط ​​للصور المتدهورة بواسطة الضوضاء الإضافية والتشويش. يمكن لمطوري واجهة برمجة التطبيقات لـ Java من Aspose.PSD تطبيق فلتر المتوسط ​​لإزالة الضوضاء من الصورة ويمكنهم تطبيق فلتر وينر جاوسي على الصور. يوضح هذا المقال كيف يمكن تطبيق فلتر المتوسط ​​وفلتر وينر جاوسي على الصور.

### **تطبيق فلتر المتوسط**
توفر Aspose.PSD فئة MedianFilterOptions لتطبيق الفلتر على RasterImage. الكود البرمجي الوارد أدناه يوضح كيفية تطبيق فلتر المتوسط ​​على صورة نقطية.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **تطبيق فلتر وينر جاوسي**
توفر Aspose.PSD فئة GaussWienerFilterOptions لتطبيق الفلتر على RasterImage. الكود البرمجي الوارد أدناه يوضح كيفية تطبيق فلتر وينر جاوسي على صورة نقطية.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **تطبيق فلتر وينر جاوسي على صورة ملونة**
توفر Aspose.PSD فئة GaussWienerFilterOptions للصور الملونة أيضًا. الكود البرمجي الوارد أدناه يوضح كيفية تطبيق فلتر وينر جاوسي على صورة ملونة.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **تطبيق فلتر وينر جاوسي لحركة الصورة**
توفر Aspose.PSD فئة MotionWienerFilterOptions لتطبيق الفلتر على RasterImage. الكود البرمجي الوارد أدناه يوضح كيفية تطبيق فلتر وينر لحركة الصورة على صورة نقطية.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **تطبيق فلتر التصحيح على صورة**
يوضح هذا المقال استخدام Aspose.PSD لـ Java لتنفيذ فلاتر التصحيح على الصورة. API لـ Aspose.PSD قد قدمت أساليب فعالة وسهلة الاستخدام لتحقيق هذا الهدف. لـ Aspose.PSD لـ Java، تمت تعريض فئتي BilateralSmoothingFilterOptions و SharpenFilterOptions للتصفية. تحتاج فئة BilateralSmoothingFilterOptions إلى عدد صحيح كحجم. تكون خطوات تنفيذ تغيير الحجم بسيطة كما يلي:

١. تحميل صورة باستخدام الطريقة الفعالة التي قدمتها فئة Image.
١. تحويل الصورة إلى RasterImage.
١. إنشاء مثيلات لفئتي BilateralSmoothingFilterOptions و SharpenFilterOptions.
١. استدعاء طريقة Filter من RasterImage مع تحديد المستطيل كحدود صورة ومثيل فئة BilateralSmoothingFilterOptions.
١. استدعاء طريقة Filter من RasterImage مع تحديد المستطيل كحدود صورة ومثيل فئة SharpenFilterOptions.
١. ضبط التباين.
١. تعيين السطوع.
١. حفظ النتائج.

الكود البرمجي التالي يوضح لك كيفية تطبيق فلتر التصحيح.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **استخدام خوارزمية Bradley threshold**
يُستخدم تحديد العتبة في تطبيقات الرسومات. الهدف من تحديد عتبة الصورة هو تصنيف البكسلات إما كـ "داكنة" أو "فاتحة". تسمح واجهة برمجة التطبيقات لـ Aspose.PSD بك استخدام تحديد عتبة Bradley أثناء تحويل الصور. يوضح الكود البرمجي الوارد أدناه كيفية تعريف قيمة العتبة ومن ثم استدعاء خوارزمية العتبة Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
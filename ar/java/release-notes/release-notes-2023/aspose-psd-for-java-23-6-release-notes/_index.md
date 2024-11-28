---
title: ملاحظات الإصدار Aspose.PSD للجافا 23.6
type: docs
weight: 40
url: /ar/java/aspose-psd-for-java-23-6-release-notes/
---

{{% alert color="primary" %}} هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD للجافا 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **المفتاح** | **الملخص** | **الفئة** |
|:------------|:------------|:------------|
| PSDJAVA-479 | إعادة هيكلة واجهة برمجة التطبيقات (API) للوقت المحدد | تحسين |
| PSDJAVA-480 | إزالة الفنون عند تقديم التشويه | تحسين |
| PSDJAVA-481 | تحسين أداء تقديم التشويه | تحسين |
| PSDJAVA-482 | دعم طبقة ضبط العتبة | ميزة |
| PSDJAVA-483 | دعم طبقة ضبط الألوان الانتقائية | ميزة |
| PSDJAVA-484 | القدرة على تصدير وقت القص من PSD إلى ملف GIF متحرك | ميزة |
| PSDJAVA-485 | إضافة دعم لطبقة النص بدون حدود مستطيلية | ميزة |
| PSDJAVA-486 | دعم طبقة الشكل | ميزة |
| PSDJAVA-487 | لا يتم تحديث استبدال الصورة في الكائن الذكي | خلل |
| PSDJAVA-488 | لا يمكن حفظ ملف PSD كـ PSD بالاستثناء التالي: لا يمكن أن تحتوي وسائط Rgb و Lab على أقل من 3 قنوات وأكثر من 4 قنوات | خلل |
| PSDJAVA-489 | يتم فقدان التبرير النصي عند فتح طبقة النص بوضع التحرير في فوتوشوب | خلل |
| PSDJAVA-490 | استثناء مرجعية فارغة عند حفظ ملف PSD | خلل |
| PSDJAVA-491 | استثناء عند تحميل طبقة الشكل: نقاط حدود الأصل للفيكتور غير مدعومة بعد | خلل |
| PSDJAVA-492 | استثناء عند تحميل مصدر Vogk: تم حفظ النقاط كهياكل Double ، ونحن نقرأ بوصفها هياكل Unit | خلل |
| PSDJAVA-493 | نوع الطبقة لطبقة الشكل فارغ | خلل |

## **تغييرات الواجهة البرمجية العمومية**
# **الواجهات الجديدة:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
...

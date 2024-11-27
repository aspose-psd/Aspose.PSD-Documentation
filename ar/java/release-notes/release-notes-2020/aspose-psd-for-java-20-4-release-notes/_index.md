```md
---
title: Aspose.PSD لـ Java 20.4 - ملاحظات الإصدار
type: docs
weight: 30
url: /ar/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDJAVA-156|دعم لـ مورد 'بيانات الأصل الناشئ' للفيكتور|ميزة|
|PSDJAVA-171|دعم lclrResource (ضبط لون الورقة)|ميزة|
|PSDJAVA-157|دعم الخصائص من بيانات LengthRecord. (عمليات المسار (عمليات منطقية), فهرس الشكل في الطبقة, عدد سجلات العقد بيزير)|ميزة|
|PSDJAVA-158|دعم لـ مورد قسم الصورة #1010 للخلفية|ميزة|
|PSDJAVA-161|إضافة تعميمات للأطبقة أثناء التشغيل|ميزة|
|PSDJAVA-168|دعم مورد قسم الصورة #1009 لمعلومات الحدود.|ميزة|
|PSDJAVA-169|دعم الطبقات في ملفات تنسيق AI|ميزة|
|PSDJAVA-163|دعم قراءة وتحرير تأثير طبقة تحصيل التدرج|ميزة|
|PSDJAVA-164|تقديم تأثير طبقة تحصيل التدرج|ميزة|
|PSDJAVA-149| Aspose.PSD for java خطأ عند الحصول على خاصية textData.items للطبقة النصية|خلل|
|PSDJAVA-166|إصلاح حفظ صورة PSD بنمط ألوان اللون Grayscale و 16 بت لكل قناة إلى تنسيق PSD Grayscale|خلل|
|PSDJAVA-167|إصلاح حفظ صورة PSD بنمط ألوان اللون Grayscale و 16 بت لكل قناة إلى تنسيق PNG|خلل|
|PSDJAVA-159|لا تُعرض تغييرات خاصية GradientOverlayEffect.BlendMode في Photoshop|خلل|

# **تغييرات الواجهة البرمجية العامة**
## **الواجهات الجديدة:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose
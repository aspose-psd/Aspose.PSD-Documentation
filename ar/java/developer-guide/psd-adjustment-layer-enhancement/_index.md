---
title: استخدام طبقة التعديل لتحسين PSD
weight: 100
type: docs
description: أمثلة على استخدام طبقة التعديل عبر Aspose.PSD للجافا
keywords: [طبقة التعديل, تحسين الصورة, تعديل المنحنيات, تحسين المستويات, عكس, تصفية الصور,  واجهة برمجة التطبيقات لملفات PSD, جافا, عينة الشيفرة]
url: /ar/java/adjustment-layer-enhancement/
---

## **نظرة عامة**

يستكشف هذا المقال تحرير طبقات التعديل في Aspose.PSD للجافا. تعتبر طبقات التعديل ميزة قوية في تحرير الصور تسمح لك بإجراء تغييرات غير مدمرة على صورتك. يوفر Aspose.PSD مجموعة شاملة من فصائل طبقات التعديل يمكنك استخدامها لتعديل جوانب مختلفة من صورك.

لتوضيح تحرير طبقات التعديل، سنقدم مقتطف شفرة مثال في نهاية الصفحة يحمل صورة PSD ويطبق تعديلات مختلفة على طبقاتها.

في مقتطف الشفرة التالي، نبدأ بتحميل صورة PSD باستخدام طريقة PsdImage.load(). ثم نعد الخيارات لحفظ ملفات الإخراج بتنسيق PNG. تسمح فئة PngOptions لنا بتحديد نوع اللون لصورة الإخراج.

بعد ذلك، نكرر من خلال كل طبقة في صورة PSD ونتحقق من نوعها باستخدام الطريقة isAssignable(). إذا كانت الطبقة من نوع معين، نحولها إلى ذلك النوع باستخدام الطريقة cast() ونطبق التعديل المطلوب. على سبيل المثال، نضبط سطوع وتباين BrightnessContrastLayer، نعدّل المستويات LevelsLayer، نضيف نقطة منحنى لطبقة CurvesLayer، وهكذا.

يمكنك إضافة شيفرات إضافية لتطبيق تعديلات أخرى على طبقاتها الخاصة. يوفر Aspose.PSD مجموعة واسعة من فئات طبقات التعديل، مثل [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) والمزيد.

أخيرًا، نحفظ الصورة المعدّلة باستخدام طريقة save() لفئة PsdImage.

توفر هذه النظرة العامة أساسيات كيفية تحرير طبقات التعديل في Aspose.PSD للغة الجافا. يمكنك تخصيص التعديلات وفقا لاحتياجاتك واستكشاف الخيارات المختلفة المتاحة في وثائق واجهة برمجة التطبيقات.

يرجى التحقق من المثال الكامل أدناه.

## **مثال**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
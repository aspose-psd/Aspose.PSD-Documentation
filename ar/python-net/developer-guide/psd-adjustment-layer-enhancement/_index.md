---
title: 'استخدام طبقة التعديل لتحسين PSD'
weight: 100
type: docs
description: 'أمثلة على استخدام طبقة التعديل عبر Aspose.PSD لـ Python'
keywords: [طبقة التعديل, تعزيز الصورة, تعديل المنحنيات, تحسين المستويات, عكس, مرشح الصورة, واجهة برمجة التطبيقات لملفات PSD, Python, عينة الكود]
url: ar/python-net/adjustment-layer-enhancement/
---

## **نظرة عامة**

في هذا المقال، سنستكشف تعديل طبقات التعديل في Aspose.PSD لـ Python. تعد طبقات التعديل ميزة قوية في تحرير الصور تسمح لك بإجراء تغييرات غير تدميرية على صورك. يوفر Aspose.PSD مجموعة شاملة من فصول طبقات التعديل التي يمكنك استخدامها لتعديل جوانب مختلفة من صورك.

لعرض تحرير طبقات التعديل، سنستخدم مقطعًا من الكود عينة في نهاية الصفحة الذي يقوم بتحميل صورة PSD وتطبيق تعديلات مختلفة على طبقاتها.

في مقطع الكود أدناه، نبدأ بتحميل صورة PSD باستخدام طريقة PsdImage.load(). ثم نقوم بإعداد الخيارات لحفظ ملفات PNG الناتجة. تسمح فئة PngOptions لنا بتحديد نوع الألوان للصورة الناتجة.

بعد ذلك، نكرر كل طبقة في صورة PSD ونتحقق من نوعها باستخدام طريقة is_assignable(). إذا كانت الطبقة من نوع معين، نقوم بتحويلها إلى تلك الفئة باستخدام طريقة cast() وتطبيق التعديل المطلوب. على سبيل المثال، نعدل سطوع وتباين BrightnessContrastLayer، نعدل المستويات LevelsLayer، نضيف نقطة منحنى إلى CurvesLayer، وهكذا.

يمكنك إضافة كود إضافي لتطبيق تعديلات أخرى على طبقاتها المعنية. يوفر Aspose.PSD مجموعة واسعة من فصول طبقات التعديل، مثل [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer)، وغيرها.

وأخيرًا، نحفظ الصورة المعدلة باستخدام طريقة save() في فئة PsdImage.

يوفر هذا الكود نظرة عامة أساسية عن كيفية تحرير طبقات التعديل في Aspose.PSD لـ Python. يمكنك تخصيص التعديلات وفقًا لاحتياجاتك واستكشاف الخيارات المتنوعة المتاحة في وثائق الواجهة البرمجية.

يرجى التحقق من المثال الكامل.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
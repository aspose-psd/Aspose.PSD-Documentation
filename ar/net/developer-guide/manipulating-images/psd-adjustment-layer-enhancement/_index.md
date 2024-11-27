---
title: استخدام طبقة التعديل لتعزيز PSD
weight: 100
type: docs
description: أمثلة على استخدام طبقات التعديل عبر Aspose.PSD لـ C#
keywords: [طبقة التعديل، تعزيز الصورة، تعديل منحنيات، تعزيز المستويات، عكس، تصفية الصورة، واجهة برمجة تطبيقات PSD، C#، csharp، عينة الكود]
url: ar/net/تعزيز-طبقة-التعديل/
---

## نظرة عامة

في هذا المقال، سنستكشف تحرير طبقات التعديل في Aspose.PSD لـ C#. طبقات التعديل هي ميزة قوية في تحرير الصور تسمح لك بإجراء تغييرات غير تدميرية على صورك. يوفر Aspose.PSD مجموعة شاملة من فصول طبقات التعديل التي يمكنك استخدامها لتعديل جوانب مختلفة من صورك.

لتوضيح تحرير طبقات التعديل، سنستخدم مقتطفًا من الكود الذي يحمل صورة PSD ويطبق تعديلات مختلفة على طبقاتها.

في مقتطف الكود أدناه، نبدأ بتحميل الصورة PSD باستخدام طريقة `PsdImage.Load()`. ثم نقوم بإعداد الخيارات لحفظ ملفات PNG الناتجة. تسمح فئة `PngOptions` لنا بتحديد نوع اللون للصورة الناتجة.

بعد ذلك، نكرر عبر كل طبقة في صورة PSD ونتحقق من نوعها باستخدام الطريقة `IsAssignable()`. إذا كانت الطبقة من نوع معين، فإننا نقوم بتحويلها إلى هذا النوع باستخدام الطريقة `Cast()` وتطبيق التعديل المطلوب. على سبيل المثال، نعدل سطوع وتباين `BrightnessContrastLayer`، نعدل مستويات `LevelsLayer`، نضيف نقطة منحنى إلى `CurvesLayer`، وهكذا.

يمكنك إضافة كود إضافي لتطبيق تعديلات أخرى على طبقاتها الخاصة. يوفر Aspose.PSD مجموعة واسعة من فئات طبقات التعديل، مثل [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)، [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer)، [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer)، [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer)، [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer)، [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer)، [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer)، [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer)، [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer)، [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer)، وغيرها.

أخيرًا، نقوم بحفظ الصورة المعدلة باستخدام الطريقة `Save()` من فئة `PsdImage`.

يقدم هذا الكود نظرة عامة أساسية حول كيفية تحرير طبقات التعديل في Aspose.PSD لـ C#. يمكنك تخصيص التعديلات وفقًا لاحتياجاتك و استكشاف الخيارات المتاحة في وثائق الواجهة البرمجية التطبيقية.

## مثال

إليك عينة من الكود توضح كيفية استخدام طبقات التعديل باستخدام Aspose.PSD لـ C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

لمزيد من المعلومات المفصلة والأمثلة، يرجى زيارة [توثيق Aspose.PSD لـ C#](https://docs.aspose.com/psd/net/).
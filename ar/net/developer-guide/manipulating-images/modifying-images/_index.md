---
title: تعديل الصور
type: docs
weight: 50
url: /ar/net/modifying-images/
---

## **تخفيت الصور النقطية**
التخفيت هو تقنية لخلق وهم من الألوان والظلال الجديدة من خلال تغيير نمط النقاط التي تخلق بالفعل صورة. إنها أكثر الوسائل شيوعًا لتقليل نطاق الألوان للصور إلى 256 لون (أو أقل). توفر Aspose.PSD دعم التخفيت لفئة [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) عن طريق إدخال طريقة الخفيت التي تقبل المعلمتين. الأولى من نوع DitheringMethod المراد تطبيقه مع خيارين ممكنين هما FloydSteinbergDithering و ThresholdDithering. المعامل الثاني لطريقة [Dither(https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) هو عدد البتات بالجدول الصحيح. يحدد BitCount حجم العينة لنتيجة الخفيت. القيمة الافتراضية هي 1 التي تمثل الأسود والأبيض، حيث القيم المسموح بها هي 1، 4، 8 توليد لوحات ألوان مع 2، 4 و 256 لونًا على التوالي.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}


## **تعديل السطوع والتباين والجاما**
التعديلات اللونية في الصور الرقمية هي أحد الميزات الأساسية التي تقدمها معظم مكتبات معالجة الصور. يمكن تصنيف التعديلات اللونية في ما يلي.

1. السطوع يشير إلى فاتح أو غامق من لون. زيادة سطوع الصورة يضيء جميع الألوان بينما يقلل السطوع يظلم جميع الألوان.
1. التباين يشير إلى جعل الكائنات أو التفاصيل في الصورة أكثر وضوحًا. زيادة التباين في الصورة يقوي الفارق بين المناطق الفاتحة والمظلمة بحيث تصبح المناطق الفاتحة أفتح والمناطق الداكنة تصبح أغمق. تقليل التباين سيجعل المناطق الفاتحة والداكنة تظل تقريبًا نفسها ولكن الصورة بشكل عام تصبح أكثر تجانسًا.
1. الجاما يحسن التباين والسطوع للإضاءة غير المباشرة التي تضيء كائنًا في الصورة.
### **ضبط السطوع**
يوفر Aspose.PSD API لـ .NET الطريقة [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) لفئة [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) التي يمكن استخدامها لضبط سطوع الصورة عن طريق تمرير قيمة صحيحة كمعلمة. أعلى قيمة معلمة تشير إلى صورة أكثر إشراقًا. هنا هي الصورة الأصلية والصورة الناتجة للمقارنة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **ضبط التباين**
تشتمل الطريقة [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) التي تعرضها فئة [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) على ضبط تباين الصورة عن طريق تمرير قيمة عائمة كمعلمة.

القيمة العائمة الأعلى تشير إلى تباين أعلى في الصورة المعطاة. هنا هي الصورة الأصلية والصورة الناتجة للمقارنة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}


### **ضبط الجاما**
تعرض الطريقة [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) التي تعرضها فئة [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) نسختين. إحدى الإصدارات تقبل قيمة عائمة وتنفذ تصحيح جاما لمعاملات قناة الأحمر والأزرق والأخضر. في حين أن الإصدار الآخر يقبل ثلاثة معلمات عائمة تمثل كل معامل لون على حدة. يوضح الكود التالي كيفية ضبط جاما على صورة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}


## **تحديش سطح الصورة**
توضح هذه المقالة استخدام Aspose.PSD for .NET لأداء تأثير تحديش على صورة. لقد عرضت واجهات برمجة التطبيقات Aspose.PSD لـ .NET طرقًا فعالة وسهلة الاستخدام لتحقيق هذا الهدف. لقد عرضت Aspose.PSD for .NET طبقة [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) لإنشاء تأثير تحديش على الطاير. تحتاج فئة [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) إلى قيم نصف قطر وسيجما لإنشاء تأثير تحديش على صورة. الخطوات لأداء تغيير الحجم بسيطة كما يلي:

1. قم بتحميل صورة باستخدام طريقة Load المعرضة من قبل فئة الصورة.
1. قم بتحويل الصورة إلى [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. قم بإنشاء مثيل من فئة [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) بناء على البيانات أو قدم قيم نصف قطر وسيجما في البناء.
1. استدعاء طريقة [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter مع تحديد المستطيل كحدود صورة ومثيل فئة [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. احفظ النتائج.

الكود التالي يوضح كيفية إنشاء تأثير تحديش على صورة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}


## **التحقق من شفافيّة الصورة**
توضح هذه المقالة استخدام Aspose.PSD for .NET للتحقق من شفافية الصورة. الخطوات للتحقق من شفافية الصورة بسيطة كما يلي:

1. تحميل الصورة باستخدام الطريقة المعرضة [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) من قبل فئة [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. التحقق من شفافية الصورة إذا كانت شفافية الصورة صفرًا فإن الصورة شفافة.
1. الكود التالي يوضح كيفية التحقق من شفافية الصورة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}


## **تطبيق ضاغط Lossy GIF**
يمكن للمطورين باستخدام Aspose.PSD لـ .NET تحديد فارق البكسل. تستند ضغطات GIF على "قاموس" يتضمن سلاسل من نقاط البكسل المرئية. يبحث المرشح العادي في القاموس عن أطول سلسلة من النقاط القابلة للمطابقة بالضبط للنقاط في الصورة. يختار المرشح القاسي أطول سلسلة من النقاط القابلة للمطابقة "بما فيه الكفاية" للنقاط في الصورة. أدناه توضيح الكود لهذه الوظيفة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}


## **تنفيذ إعادة تحجيم Bicubic**
التحجيم يعني أنك تغيّر أبعاد البكسل لصورة. عند الإنقاص، أنت تقوم بحذف البكسل وبالتالي تحذف المعلومات والتفاصيل من الصورة. عند الزيادة، أنت تضيف البكسل. يضيف Photoshop هذه البكسل عبر تحسين التداخل. توضح هذه المقالة كيف يمكنك القيام بتنفيذ إعادة تحجيم Bicubic باستخدام Aspose.PSD for .NET.

أدناه توضيح الكود لهذه الوظيفة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}


## **طبقة تعديل توازن الألوان**
توضح هذه المقالة استخدام Aspose.PSD لـ .NET لتنفيذ **طبقة تعديل توازن الألوان** على صورة. تتيح طبقة تعديل توازن الألوان القدرة على إجراء تعديلات على تلوين الصور. تقدم الطبقة ثلاث قنوات ألوان وألوانها المكملة ويمكنك ضبط توازن هذه الأزواج لتغيير مظهر الصورة.

أدناه توضيح الكود لهذه الوظيفة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}


## **طبقة تعديل العكس**
توضح هذه المقالة كيف يمكنك تنفيذ **طبقة تعديل العكس** باستخدام Aspose.PSD لـ .NET. طبقة التعديل هي نوع خاص من الطبقات يستخدم بشكل رئيسي لتصحيح الألوان. بدلاً من وجود محتوى خاص بهم، يقومون بضبط المعلومات على الطبقات تحتهم. تعمل طبقة التعديل على تحويل تأثير تأثير صورة سلبيًا بعكس ألوان الصورة.

أدناه توضيح الكود لهذه الوظيفة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
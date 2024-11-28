---
title: تعديل الصور
type: docs
weight: 50
url: /ar/java/modifying-images/
---

## **تقطيع الصور النقطية**
التقطيع هو تقنية لإنشاء وهم ألوان وظلال جديدة عن طريق تغيير النمط من النقاط التي تخلق الصورة فعليًا. وهو الوسيلة الأكثر شيوعًا لتقليل نطاق الألوان للصور إلى 256 (أو أقل) لون. توفر Aspose.PSD دعم التقطيع لفئة RasterImage من خلال إدخال طريقة Dither التي تقبل معلمتين. الأولى من نوع DitheringMethod التي ستُطبق مع اثنتين من الخيارات الممكنة FloydSteinbergDithering وThresholdDithering. المعلمة الثانية لطريقة Dither هي BitCount بصيغة عدد صحيح. يحدد BitCount حجم العينة لنتيجة التقطيع. القيمة الافتراضية هي 1 التي تُمثل الأسود والأبيض، في حين أن القيم المسموح بها هي 1، 4، 8 لتوليد لوحات ذات 2، 4 و 256 لونًا على التوالي.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **ضبط السطوع، التباين والجاما**
تعتبر التعديلات اللونية في الصور الرقمية واحدة من الميزات الأساسية التي تقدمها معظم مكتبات معالجة الصور. يمكن تصنيف التعديلات اللونية في الأقسام التالية.

1. السطوع يشير إلى ضوء أو ظلام اللون. زيادة سطوع الصورة تومئ إلى إضاءة جميع الألوان بينما تقليل السطوع يظلم جميع الألوان.
1. التباين يشير إلى جعل الكائنات أو التفاصيل داخل الصورة أكثر وضوحًا. زيادة التباين في الصورة يزيد الفارق بين المناطق الخفيفة والداكنة بحيث تصبح المناطق الخفيفة أكثر إضاءة والمناطق الداكنة تصبح أكثر ظلمة. بينما يجعل تقليل التباين المناطق الخفيفة والداكنة تظل تقريبًا نفسها ولكن الصورة العامة تصبح أكثر تجانسًا.
1. الجاما يحسن العقد والسطوع للإضاءة الغير مباشرة التي تنير كائنًا في الصورة.

### **ضبط السطوع**
توفر واجهة برمجة تطبيقات Aspose.PSD للغة Java الطريق AdjustBrightness لفئة RasterImage التي يمكن استخدامها لضبط سطوع الصورة من خلال تمرير قيمة صحيحة كمعلمة. تعبر قيمة المعلمة الأعلى عن صورة أكثر إشراقًا. فيما يلي الصورة الأصلية والصورة الناتجة للمقارنة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **ضبط التباين**
يمكن استخدام طريقة AdjustContrast التي تكشف عنها فئة RasterImage لضبط التباين في الصورة عن طريق تمرير قيمة عشرية كمعلمة.

تعبر القيمة الأعلى عن تباين أعلى في الصورة المعطاة. فيما يلي الصورة الأصلية والصورة الناتجة للمقارنة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **ضبط الجاما**
تكشف طريقة AdjustGamma التي تكشف عنها فئة RasterImage عن نسختين. إحدى النسخ تقبل قيمة عشرية وتُنفذ تصحيح جاما لمعاملات قناة الأحمر والأزرق والأخضر. في حين تقبل النسخة الأخرى ثلاثة قيم بصيغة عشرية تمثل كل معامل لون على حدة. يوضح الكود التالي كيفية ضبط الجاما على صورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **تشويش الصورة**
توضح هذه المقالة استخدام Aspose.PSD للغة Java لتنفيذ تأثير التشويش على الصورة. لقد كشف APIs Aspose.PSD عن طرق فعالة وسهلة الاستخدام لتحقيق هذا الهدف. قد كشف Aspose.PSD للغة Java عن فئة GaussianBlurFilterOptions لإنشاء تأثير تشويش على الطاير. تحتاج فئة GaussianBlurFilterOptions إلى قيم شعاع وسيجما لإنشاء تأثير تشويش على الصورة. الخطوات لتنفيذ Resize بسيطة كما يلي:

1. تحميل صورة باستخدام طريقة الكائن المصنع معرضة من قبل فئة Image.
1. تحويل الصورة إلى RasterImage.
1. إنشاء نسخة من فئة GaussianBlurFilterOptions باستخدام البناء الافتراضي أو توفير قيم شعاع وسيجما في البناء.
1. استدعاء طريقة RasterImage.Filter مع تحديد مستطيل كحدود للصورة ونسخة فئة GaussianBlurFilterOptions.
1. حفظ النتائج.

يوضح الكود التالي كيفية تطبيق تأثير تشويش على الصورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **التحقق من شفافية الصورة**
توضح هذه المقالة استخدام Aspose.PSD للغة Java للتحقق من شفافية الصورة. الخطوات للتحقق من شفافية الصورة بسيطة كما يلي:

1. تحميل صورة باستخدام طريقة الكائن المصنع معرضة من قبل فئة Image.
1. التحقق من الضبابية في الصورة إذا كانت الضبابية تساوي الصفر فإن الصورة شفافة.
1. يوضح الكود التالي كيفية التحقق من شفافية الصورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **تنفيذ ضاغط GIF اللاإرجاعي**
مع Aspose.PSD للغة Java، يمكن للمطورين تعيين فرق البكسل. تعتمد ضغط GIF على "قاموس" من سلاسل البكسل المرئية. يقوم المشفر العادي بالبحث في القاموس عن أطول سلسلة من البكسل التي تطابق تمامًا بكسل الصورة. يختار المشفر ذو الضمان أطول سلسلة من البكسل التي "تكون مشابهة بما فيه الكفاية" للبكسل في الصورة. يعرض الكود أدناه لتوضيح الوظيفة المذكورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **تنفيذ إعادة عينات Bicubic**
يعني إعادة عينات أنك تقوم بتغيير أبعاد البكسل للصورة. عندما تقوم بإجراء عينات دونية، فأنت تقوم بالتخلص من البكسل وبالتالي حذف المعلومات والتفاصيل من الصورة الخاصة بك. عندما تقوم بإجراء عينات علوية، أنت تضيف بكسلًا. يضيف Photoshop هذه البكسل باستخدام التكبير الرقمي. توضح هذه المقالة كيف يمكنك تنفيذ إعادة العينات Bicubic باستخدام Aspose.PSD للغة Java.

يعرض الكود أدناه لتوضيح الوظيفة المذكورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **تنفيذ طبقة الضبط المعكوس**
توضح هذه المقالة كيف يمكنك تنفيذ **الطبقة ضبط المعكوس** باستخدام Aspose.PSD للغة Java. الطبقة الضبطية هي نوع خاص من الطبقات تستخدم في معظم الأحيان لتصحيح الألوان. بدلاً من وجود المحتوى الخاص بهم، فإنها تعدل المعلومات على الطبقات تحتها. تمنح طبقة التعديل المعكوس تأثير صورة سلبية من خلال عكس الألوان للصورة.

يعرض الكود أدناه لتوضيح الوظيفة المذكورة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}
---
title: تحديث طبقة ملء PSD باستخدام Python
weight: 100
type: docs
description: أمثلة على استخدام جميع أنواع الطبقات التعديلية بما في ذلك طبقة الملء اللونية وطبقة الملء التدرجية وطبقة الملء نمطية
keywords: [طبقة الملء, طبقة الملء اللونية, طبقة الملء التدرجية, طبقة الملء نمطية, واجهة برمجة تطبيقات PSD, Python, عينة الكود]
url: ar/python-net/تحرير-طبقة-ملء-psd/
---

## **نظرة عامة**

لإنشاء طبقة عادية، يمكنك استخدام وظيفة create_regular_layer المقدمة في الكود. تأخذ هذه الوظيفة المعلمات left, top, width, و height لتعريف موضع وحجم الطبقة. يتم إنشاء طبقة جديدة، وتعيين حدودها، وملؤها بلون محدد.

لإنشاء طبقة ملء لونية، يمكنك استخدام طريقة create_instance من الفئة FillLayer بمعلمة FillType.COLOR. بعد إنشاء طبقة الملء، يمكنك الوصول إلى إعدادات الملء الخاصة بها باستخدام خاصية fill_settings وتحديد اللون باستخدام خاصية color من فئة ColorFillSettings. في الكود المقدم، يتم تعيين اللون إلى Color.coral. يتم تعيين خاصية clipping من طبقة الملء إلى 1، مما يجعل الطبقة تعمل كقناع قص.

لإنشاء طبقة ملء تدرجية، يمكنك استخدام طريقة create_instance من الفئة FillLayer بمعلمة FillType.GRADIENT. بشكل مماثل لطبقة الملء اللونية، يمكنك الوصول إلى إعدادات الملء باستخدام خاصية fill_settings وتحديد نقاط لون التدرج ونقاط الشفافية. في الكود المقدم، تم تحديد نقاط لون التدرج باستخدام فئة GradientColorPoint، وتم تعريف نقاط الشفافية باستخدام فئة GradientTransparencyPoint. كما تم تعيين خاصية clipping من طبقة الملء إلى 1.

لإنشاء طبقة ملء نمطية، يمكنك استخدام طريقة create_instance من الفئة FillLayer بمعلمة FillType.PATTERN. مرة أخرى، يمكنك الوصول إلى إعدادات الملء باستخدام خاصية fill_settings وتحديد بيانات النمط وخصائص أخرى. في الكود المقدم، تم تعريف بيانات النمط باستخدام فئة PatternFillSettings، وتم تعيين خاصية clipping إلى 1.

بعد إنشاء طبقات الملء، يمكنك إضافتها إلى صورة PSD باستخدام طريقة add_layer. يمكنك أيضًا تحديد اسم العرض وخصائص أخرى لكل طبقة ملء.

وأخيرًا، يمكنك حفظ صورة PSD وصورة PNG المقابلة باستخدام الكود المقدم. تم تعيين خيارات PNG لاستخدام الألوان الحقيقية مع تعتيم ألفا للشفافية.

يرجى التحقق من المثال الكامل.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "التوثيق-Python-Aspose-psd-fill-layer-editing.py" >}}
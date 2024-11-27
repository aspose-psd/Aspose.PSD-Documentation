---
title: إضافة علامة مائية لصورة
type: docs
weight: 30
url: /ar/net/adding-a-watermark-to-an-image/
---

## **إضافة علامة مائية لصورة**
هذا المستند يشرح كيفية إضافة علامة مائية إلى صورة باستخدام Aspose.PSD. إضافة علامة مائية إلى صورة هو متطلب شائع في تطبيقات معالجة الصور. يستخدم هذا المثال فئة الرسومات لرسم سلسلة على سطح الصورة.
### **إضافة علامة مائية**
لتوضيح العملية، سنقوم بتحميل صورة BMP من القرص ورسم سلسلة كعلامة مائية على سطح الصورة باستخدام طريقة DrawString في فئة الرسومات. سنقوم بحفظ الصورة بتنسيق PNG باستخدام فئة PngOptions. فيما يلي مثال على الشيفرة التي توضح كيفية إضافة علامة مائية لصورة. تم تقسيم شيفرة المصدر الخاصة بالمثال إلى أجزاء لجعل متابعتها سهلة. خطوة بخطوة، توضح الأمثلة كيفية:

1. [تحميل](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) صورة.
1. أنشاء وتهيئة [كائن الرسومات Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. إنشاء وتهيئة فئة Font و [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. رسم سلسلة كعلامة مائية باستخدام طريقة [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) في فئة الرسومات.
1. حفظ الصورة بتنسيق PNG.

الشيفرة التالية تظهر لك كيفية إضافة علامة مائية على الصورة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **إضافة علامة مائية قطرية**
إضافة علامة مائية قطرية إلى صورة مماثلة لإضافة علامة مائية أفقية كما تم مناقشتها أعلاه، مع بعض الاختلافات. لتوضيح العملية، سنقوم بتحميل صورة JPG من القرص، إضافة تحويلات باستخدام كائن من [فئة الMatrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) ورسم سلسلة كعلامة مائية على سطح الصورة باستخدام طريقة DrawString في فئة الرسومات. فيما يلي مثال على الشيفرة التي توضح كيفية إضافة علامة مائية قطرية إلى صورة. تم تقسيم شيفرة المصدر الخاصة بالمثال إلى أجزاء لجعل متابعتها سهلة. خطوة بخطوة، توضح الأمثلة كيفية:

1. تحميل صورة.
1. إنشاء وتهيئة كائن رسومات.
1. إنشاء وتهيئة [فئة الFont](https://reference.aspose.com/psd/net/aspose.psd/font) وكائن SolidBrush.
1. الحصول على حجم الصورة في [كائن SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. إنشاء نسخة من فئة الMatrix وتنفيذ تحويل مركب.
1. تعيين التحويل إلى كائن الرسومات.
1. إنشاء وتهيئة [فئة StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. رسم سلسلة كعلامة مائية باستخدام طريقة DrawString في فئة الرسومات.
1. حفظ الصورة الناتجة.

الشيفرة التالية تظهر لك كيفية إضافة علامة مائية قطرية.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
---
title: إنشاء، فتح، وحفظ الصور
type: docs
weight: 30
url: /ar/net/creating-opening-and-saving-images/
---

## **إنشاء ملفات الصور**
يسمح Aspose.PSD for .NET للمطورين بإنشاء صورهم الخاصة. استخدم الطريقة الثابتة Create المكشوفة بواسطة فئة الصورة لإنشاء صور جديدة. كل ما عليك فعله هو توفير كائن مناسب من إحدى فئات فضاء ImageOptions لتنسيق الصورة المطلوبة. لإنشاء ملف صورة، ابدأ أولاً بإنشاء مثيل من إحدى فئات فضاء ImageOptions. تحدد هذه الفئات تنسيق الصورة الناتجة. فيما يلي بعض الفئات من فضاء ImageOptions (لاحظ أن عائلة تنسيق ملفات PSD هي الوحيدة المدعومة حاليًا للإنشاء):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) تحدد الخيارات لإنشاء ملف PSD. يمكن إنشاء ملفات الصور عن طريق تعيين مسار إخراج أو عن طريق تعيين تيار.
### **الإنشاء عن طريق تعيين المسار**
أنشئ PsdOptions من [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) فضاء ImageOptions وقم بتعيين الخصائص المختلفة. أهم خاصية لتعيينها هي الخاصية Source. تحدد هذه الخاصية أين تتواجد بيانات الصورة (في ملف أو تيار). في المثال أدناه، المصدر هو ملف. بعد تعيين الخصائص، قم بتمرير الكائن إلى إحدى الطرق الثابتة [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) جنبًا إلى جنب مع معلمات العرض والارتفاع. يُعرف العرض والارتفاع بالبكسل.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **الإنشاء باستخدام تيار**
العملية لإنشاء صورة باستخدام تيار مماثلة لاستخدام المسار. الفرق الوحيد هو أنه يجب عليك إنشاء مثيل من [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) عن طريق تمرير كائن Stream إلى بناؤه وتعيينه لخاصية Source.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}

## **فتح ملفات الصور**
يمكن للمطورين استخدام Aspose.PSD for .NET API لفتح ملفات الصور PSD الحالية لأغراض مختلفة، مثل إضافة تأثيرات على الصورة أو تحويل ملف موجود إلى تنسيق آخر. بغض النظر عن الغرض، يوفر Aspose.PSD طريقتين قياسيتين لفتح الملفات الحالية: من ملف أو من تيار.
### **الفتح من القرص**
افتح ملف صورة عن طريق تمرير المسار واسم الملف كمعلمة إلى الطريقة الثابتة Load المكشوفة بواسطة فئة الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **الفتح باستخدام تيار**
أحيانًا، الصورة التي نحتاج إلى فتحها مخزنة كتيار. في مثل هذه الحالات، استخدم الإصدار المكدس من الطريقة Load. يقبل هذا الإصدار كائن Stream كوسيط لفتح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **تحميل الصورة كطبقة**
توضح هذه المقالة استخدام Aspose.PSD لتحميل صورة كطبقة. لقد قامت APIs للتلاعب بالصور Aspose.PSD بتوفير طرق فعالة وسهلة الاستخدام لتحقيق هذا الهدف. قد قامت Aspose.PSD بتعريض طريقة AddLayer في فئة PsdImage لإضافة صورة إلى ملف PSD كطبقة.

خطوات تحميل صورة إلى PSD كطبقة بسيطة كما يلي:

- أنشئ مثيل صورة باستخدام فئة PsdImage بعرض وارتفاع محدد.
- قم بتحميل ملف PSD كصورة باستخدام الطريقة الثابتة Load التي تعرضها فئة Image.
- أنشئ مثيلًا من الفئة Layer وقم بتعيين طبقة صورة PSD إليها.
- أضف الطبقة التي تم إنشاؤها باستخدام طريقة AddLayer التي تكشف عنها فئة PsdImage.
- احفظ النتائج.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **تحميل الصورة كطبقة من تيار**
توضح هذه المقالة استخدام Aspose.PSD لتحميل صورة كطبقة من تيار. لتحميل صورة من تيار، مرر ببساطة كائن تيار يحتوي على الصورة إلى بناء الفئة Layer. أضف الطبقة التي تم إنشاؤها باستخدام طريقة AddLayer التي تعرضها فئة PsdImage واحفظ النتائج.

وفيما يلي الشفرة المصدرية العينية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **حفظ ملفات الصور**
Aspose.PSD تتيح لك إنشاء ملفات الصور من البداية. كما توفر وسائل لتحرير ملفات الصور الموجودة. بمجرد إنشاء الصورة أو تعديلها، يتم عادة حفظ الملف على القرص. Aspose.PSD توفر لك طرقًا لحفظ الصور على القرص عن طريق تحديد مسار أو باستخدام كائن تيار.
### **الحفظ على القرص**
تمثل فئة Image كائن صورة، لذا توفر هذه الفئة جميع الأدوات اللازمة لإنشاء وتحميل وحفظ ملف صورة. استخدم طريقة الحفظ Save لفئة Image لحفظ الصور. إحدى الإصدارات المكدسة لطريقة الحفظ تقبل موقع الملف كسلسلة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **الحفظ على تيار**
يقبل إصدار آخر مكدس من طريقة الحفظ كائن تيار كوسيط ويحفظ ملف الصورة على التيار.

إذا تم إنشاء الصورة عن طريق تحديد أي من CreateOptions في بناء Image، يتم حفظ الصورة تلقائيًا على المسار أو التيار المقدم أثناء تهيئة فئة Image بالاستدعاء Save لطريقة التي لا تقبل أي معلمة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **ضبط لاستبدال الخطوط المفقودة**
يمكن للمطورين استخدام Aspose.PSD for .NET API لتحميل ملفات الصور PSD الموجودة لأغراض مختلفة، على سبيل المثال، لتعيين اسم خط الطباعة الافتراضي عند حفظ مستندات PSD كصورة نقطية (في تنسيق PNG، JPG، و BMP). يجب استخدام هذا الخط الافتراضي كاستبدال لكافة الخطوط المفقودة (الخطوط التي لم يتم العثور عليها في نظام التشغيل الحالي). بمجرد تعديل الصورة، سيتم حفظ الملف على القرص.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
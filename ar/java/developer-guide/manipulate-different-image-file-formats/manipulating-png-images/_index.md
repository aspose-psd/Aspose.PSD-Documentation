---
title: تلاعب بصور PNG
type: docs
weight: 30
url: /ar/java/manipulating-png-images/
---

## **تحديد الشفافية لصور PNG**
واحدة من مزايا حفظ الصور في شكل PNG هي أنه يمكن أن يكون لـ PNG خلفية شفافة. توفر Aspose.PSD for Java ميزة تحديد الشفافية لفئات PngImage & RasterImage كما هو موضح في القسم أدناه. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for Java لضبط أي لون كشفاف أثناء إنشاء صور PNG جديدة أو تحويل الصور الحالية إلى شكل PNG. لهذه الأغراض، قامت واجهة برمجة التطبيقات Aspose.PSD for Java بتعريض خاصية TransparentColor وتعداد PngColorType التي يمكن تحديدها لتحديد أي لون يجب عرضه كشفاف في الصورة PNG. يوضح مقتطف الكود الوارد أدناه كيفية تحويل صورة PSD حالية إلى صورة PNG عبر استخدام البناء المعمول به مسبقاً لـ PngImage وتحديد اللون المرغوب كشفاف.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **ضبط الدقة لصور PNG**
تعرض Aspose.PSD for Java فئة ResolutionSetting التي يمكن استخدامها لضبط الدقة لجميع تنسيقات الصور بما في ذلك PNG. يوضح هذا المقال استخدام واجهة برمجة التطبيقات Aspose.PSD for Java لتعيين معلمات الدقة الأفقية والرأسية لتنسيق الصور PNG. يحمل مقتطف الكود أدناه صورة PSD حالية ويحولها إلى تنسيق PNG كما يقوم بتغيير الدقة.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **ضغط ملفات PNG**
شكل الشبكة المحمولة الرسومية (PNG) هو تنسيق ضغط لا فقدان لنقل بيتماب عبر الشبكات. عندما تقوم بحفظ صورة كملف PNG في أي برنامج، قد يطلب منك اختيار مستوى ضغط في نطاق من 0 إلى أي مستوى قصوى. تحديد قيمة هذا الإعداد يضغط في الواقع حجم الملف دون التأثير على جودة الصورة. يصف هذا المقال كيفية سماح واجهة برمجة التطبيقات Aspose.PSD بالتحكم بحجم ملف PNG. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD لتعيين مستويات الضغط لتنسيق ملف PNG باستخدام فئة PngOptions التي تحتوي على خاصية ضغط من نوع int. تقبل هذه الخاصية قيمة من 0 إلى 9 حيث 9 هو أقصى ضغط. يوضح مقتطف الكود الوارد أدناه كيفية تحديد مستويات الضغط باستخدام واجهة برمجة التطبيقات Aspose.PSD for Java.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **تحديد عمق البت لصور PNG**
يتمثل عمق البت في التصوير في عدد البتات المستخدمة للإشارة إلى لون بكسل واحد في صورة نقطية. مثل جميع تنسيقات البتماب الأخرى، يتم تمثيل عمق لون PNG أيضاً بالبتات مثل 1 بت (2 ألوان)، 2 بت (4 ألوان)، 4 بت (16 لون) و 8 بت (256 لون). يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for Java لتعيين عمق البت لصور PNG باستخدام خاصية BitDepth المكشوفة بواسطة فئة PngOptions. في الوقت الحالي، يمكن تعيين خاصية BitDepth على 1، 2، 4 أو 8 بتات لأنواع الألوان اللون الرمادي والفهرسة. لأنواع الألوان الأخرى فقط 8 بتات معتمدة. يوضح مقتطف الكود الوارد أدناه كيفية تعيين عمق البت لصورة PNG.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **تطبيق طرق الفلترة على صور PNG**
تعرض واجهة برمجة التطبيقات Aspose.PSD for Java تعداد PngFilterType الذي يمكن استخدامه لتعيين نوع الفلترة لصورة PNG. يوضح مقتطف الكود الوارد أدناه كيفية تطبيق الفلترة على ملف PSD حالي إلى صورة PNG عبر استخدام PngFilterType.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **تغيير لون الخلفية لصورة PNG شفافة**
يمكن أن تحتوي صور الشكل PNG على خلفية شفافة. توفر Aspose.PSD for Java ميزة تغيير لون الخلفية لصورة PNG التي تحتوي على خلفية شفافة. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for Java لضبط/تغيير لون صورة PNG شفافة. يوضح مقتطف الكود الوارد أدناه كيفية ضبط/تغيير لون الخلفية لصورة PNG شفافة.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
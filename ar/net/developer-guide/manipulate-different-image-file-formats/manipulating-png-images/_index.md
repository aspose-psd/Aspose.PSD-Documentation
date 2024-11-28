---
title: Manipulating PNG Images
type: docs
weight: 40
url: /ar/net/manipulating-png-images/
---

## **تحديد الشفافية لصور PNG**
أحد مزايا حفظ الصور بتنسيق PNG هو أن PNG يمكن أن يكون لها خلفية شفافة. Aspose.PSD for .NET يوفر ميزة تحديد الشفافية لصور PNG وصور الرسم النقطي كما هو موضح في القسم أدناه. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for .NET لتعيين أي لون كشفاف أثناء إنشاء صور PNG جديدة أو تحويل الصور الحالية إلى تنسيق PNG. لهذه الأغراض، قامت واجهة برمجة التطبيقات Aspose.PSD for .NET بتعريض خاصية [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) وتعريف [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) الذي يمكن تعيينه لتحديد أي لون ليتم عرضه على أنه شفاف في صورة PNG. يوضح مقتطف الكود الذي يتم توفيره أدناه كيفية تحويل صورة PSD حالية إلى صورة PNG عن طريق تحديد اللون المطلوب كشفافًا.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **تعيين الدقة لصور PNG**
يكشف Aspose.PSD for .NET عن فئة ResolutionSetting التي يمكن استخدامها لتعيين الدقة لجميع تنسيقات الصور بما في ذلك PNG. يوضح هذا المقال كيفية استخدام واجهة برمجة التطبيقات Aspose.PSD for .NET لتعيين معلمات الدقة الأفقية والرأسية لتنسيق صور PNG. يقوم مقتطف الكود أدناه بتحميل صورة PSD حالية وتحويلها إلى تنسيق PNG مع تغيير الدقة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **ضغط ملفات PNG**
الصورة النقطية المحمولة PNG هي تنسيق ضغط لا فقد في نقل البيانات النقطية عبر الشبكات. عند حفظ صورة كملف PNG في أي برنامج، قد يُطلب منك اختيار مستوى ضغط في نطاق من 0 إلى أي مستوى كحد أقصى. تقوم هذه القيمة بالضغط على حجم الملف ولا تقلل من جودة الصورة. يصف هذا المقال كيفية السماح لك بالتحكم في حجم ملفات PNG باستخدام واجهة برمجة التطبيقات Aspose.PSD. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD لتعيين مستويات الضغط لتنسيق ملف PNG باستخدام فئة PngOptions التي تحتوي على خاصية [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) من النوع int. تقبل هذه الخاصية قيمة من 0 إلى 9 حيث 9 هو أقصى درجة ضغط. يوضح مقتطف الكود الذي يتم توفيره أدناه كيفية تعيين مستويات الضغط باستخدام واجهة برمجة التطبيقات Aspose.PSD for .NET.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **تحديد عمق البت لصور PNG**
عمق البت في التصوير هو عدد البتات المستخدمة للإشارة إلى لون واحد لبكسل مفرد في صورة نقطية. مثل جميع تنسيقات الصور النقطية الأخرى، يتم تمثيل عمق ألوان PNG أيضًا بالبتات مثل 1 بت (2 ألوان)، 2 بت (4 ألوان)، 4 بت (16 لون) و 8 بت (256 لون). يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for .NET لتعيين عمق البت لصور PNG باستخدام [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) الذي تقدمه فئة PngOptions. في الوقت الحالي، يمكن تعيين خاصية BitDepth إلى 1 أو 2 أو 4 أو 8 بتات لأنواع الألوان الرمادية والألوان المؤشرة. فقط يدعم 8 بتات لجميع أنواع الألوان الأخرى. يوضح مقتطف الكود الذي يتم توفيره أدناه كيفية تعيين عمق البت لصورة PNG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **تطبيق طرق تصفية على صور PNG**
عمق البت في التصوير هو عدد البتات المستخدمة للإشارة إلى لون واحد لبكسل مفرد في صورة نقطية. مثل جميع تنسيقات الصور النقطية الأخرى، يتم تمثيل عمق ألوان PNG أيضًا بالبتات مثل 1 بت (2 ألوان)، 2 بت (4 ألوان)، 4 بت (16 لون) و 8 بت (256 لون). يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for .NET لتعيين عمق البت لصور PNG باستخدام خاصية BitDepth التي تقدمها فئة PngOptions. في الوقت الحالي، يمكن تعيين خاصية BitDepth إلى 1 أو 2 أو 4 أو 8 بتات لأنواع الألوان الرمادية والألوان المؤشرة. فقط يدعم 8 بتات لجميع أنواع الألوان الأخرى. يوضح مقتطف الكود الذي يتم توفيره أدناه كيفية تعيين عمق البت لصورة PNG.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **تغيير لون الخلفية لصورة PNG شفافة**
تستطيع صور PNG تنسيق الصور PNG أن تحتوي على خلفية شفافة. يوفر Aspose.PSD for .NET ميزة تغير لون الخلفية لصورة PNG التي تحتوي على خلفية شفافة. يمكن استخدام واجهة برمجة التطبيقات Aspose.PSD for .NET لتعيين/تغيير لون صورة PNG شفافة. يوضح مقتطف الكود الذي يتم توفيره أدناه كيفية تعيين/تغيير لون خلفية صورة PNG شفافة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
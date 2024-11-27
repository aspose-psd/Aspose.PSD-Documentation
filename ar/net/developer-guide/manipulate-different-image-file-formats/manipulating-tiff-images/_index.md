---
title: تلاعب بصور TIFF
type: docs
weight: 50
url: /ar/net/تلاعب-بصور-tiff/
---

## **إضافة أطر بإعدادات مختلفة**
صيغة TIFF هي صيغة مرنة للغاية وتسمح بإضافة إطارات مختلفة، بأبعاد مختلفة، ضغط وإعدادات أخرى. تُسمح لك واجهات برمجة التطبيقات لـ Aspose.PSD بإضافة أي إطار TIFF بأي حجم مما يساعد في إنشاء وثائق معقدة. إذا كان هناك حاجة لضبط الإطارات أثناء عملية الإضافة لجعلها جميعًا متساوية ، فقم بإجراء الخطوات التالية:

- إنشاء إطار فارغ جديد بالخيارات المطلوبة أو نسخ الإطار الأصلي بالخيارات الناتجة المحددة باستخدام الطريقة CreateFrameFrom.
- قم بتغيير حجم الإطار / الصورة الأصلية إلى الأبعاد المطلوبة باستخدام الطريقة Resize.
- قم بإضافة بكسلات الإطار / الصورة الأصلية إلى الإطار الجديد.
- أضف الإطار الجديد إلى صورة TIFF الناتجة.

## **تصدير طبقات صورة PSD إلى صيغة ملف Multi Page Tiff**
أحيانًا تحتاج إلى تصدير طبقات صورة PSD إلى صيغة ملف TIFF متعددة الصفحات. ستقدم هذه المقالة كيف يمكننا القيام بهذه المهمة باستخدام Aspose.PSD لـ.NET API. أولاً ، سنقوم بتحميل صورة PSD من القرص. ثم سنكرر طبقات صورة PSD وننشئ TiffFrame من الطبقات المطابقة. وأخيرًا ، سنقوم بحفظ صورة Tiff الناتجة في ملف واحد على القرص.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **تكوين خيارات TiffOptions**
يمكن للمطورين ضبط خصائص مختلفة لـ [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class للحصول على النتائج المرغوبة. في هذا المستند ، سنركز على 4 خصائص رئيسية تتحكم في سمات الصورة الناتجة.

تمت سرد هذه الخصائص أدناه.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

عندما نقوم بتهيئة هيكل TiffOptions فارغ ، يتم تعيين كل خيار إلى قيمته الافتراضية ، على سبيل المثال يتم تعيين ضغط لا شيء، تم تعيين BitsPerSample كـ 1 و Photometric على أنه MinIsWhite. حفظ في هذا الشكل سوف يجعل الصورة النهائية أسود وأبيض وهذا هو السلوك المتوقع لمثل هذه التركيبات للخيارات. من أجل الحصول على النتائج الملونة يجب ضبط كل الخصائص المذكورة أعلاه على القيم التي تتوافق مع الفضاء اللوني المرغوب أو يمكنك تهيئة هيكل TiffOptions بالإعدادات المحددة مسبقًا كما يتم مناقشته في هذا المقال لاحقًا. فيما يلي جدول يصف قيم المعلمات المتوقعة التي يمكن تعيينها من أجل تحقيق النتائج المرغوبة. يرجى ملاحظة أنه يجب ضبط جميع الأعمدة الأربعة من خلال TiffOptions من أجل حفظ أي صورة تم تحميلها / إنشاؤها في تنسيق TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/بدون ضغط|1/4/8/16 (لوحة الألوان، وضع الألوان) قناة واحدة فقط|لا شيء|
|MinIsWhite/MinIsBlack|LZW/بدون ضغط|1/4/8/16 (وضع رمادي) قناة واحدة فقط|لا شيء|
|Palette|LZW/بدون ضغط|8 (لوحة الألوان، وضع الألوان) قناة واحدة فقط|أفقي (تحقيق ضغط أكبر من خلال LZW لنفس الأنماط)|
|MinIsWhite/MinIsBlack|LZW/بدون ضغط|8 (وضع رمادي) قناة واحدة فقط|أفقي (تحقيق ضغط أكبر من خلال LZW لنفس الأنماط)|
|RGB|LZW/بدون ضغط|[8,8,8] (3 قنوات RGB)|لا شيء/أفقي|
|RGB|LZW/بدون ضغط|[8,8,8,8] (3 قنوات RGB وقناة ألفا إضافية قد تم تعيينها من خلال TiffOptions.AlphaStorage) في الواقع يتم دعم أي عدد إضافي لقنوات ولكن يجب أن تكون لكل قناة حجم 8 بت مثل [8,8,8,8,8,8]|لا شيء/أفقي|
يجب ضبط جميع الخصائص الأربعة من خلال TiffOptions من أجل حفظ أي تنسيق صورة إلى تنسيق Tiff. أثناء استخدام تركيبات مختلفة ، قد ترفض بعض المشاهد (بما في ذلك Windows Photo Viewer) عرض الصورة الناتجة بسبب الدعم المحدود الذي يقدمونه. في مثل هذه الحالة ، يرجى اختيار مشاهد مختلفة للاختبارات الخاصة بك.

### **إعدادات محددة مسبقًا لـ فئة TiffOptions**
من أجل تيسير استخدام المستخدمين وتجنب عدم التكوين السليم لمثيل كائن TiffOptions ، يوفر Aspose.PSD for .NET API بناء آخر يقبل معلمة من نوع [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). استنادًا إلى القيمة المحددة من تعداد TiffExpectedFormat ، يقوم الAPI بتهيئة تلقائيًا جميع الخصائص الإلزامية لمثيل TiffOptions من أجل إنتاج النتائج المرغوبة. قبل أن ننتقل نحو الشيفرة المصدرية عينيةً ، إليك قائمة بحقول TiffExpectedFormat وتفاصيلها لفهم أفضل للطريقة الصحيحة لاستخدامها.

- TiffExpectedFormat.Default: ضبط هذا الحقل على Default يعمل بشكل مماثل لمنشئ الافتراضي لـ فئة TiffOptions بدون ضغط وتعيين BitsPerPixel إلى 1 من أجل إنشاء نتيجة أسود وأبيض. من المستحسن استخدام هذا الحقل عندما يكون هناك حاجة إلى ضبط خصائص معينة للتنسيق وفقًا للنتائج المرغوبة.
- TiffExpectedFormat.TiffCcitRle: محدد لترميز RLE أثناء حفظ النتيجة في تنسيق TIFF بـ 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffCcittFax3: محدد لترميز CCITT Fax3 أثناء حفظ النتيجة في تنسيق TIFF بـ 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffCcittFax4: محدد لترميز CCITT Fax4 أثناء حفظ النتيجة في تنسيق TIFF بـ 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffDeflateBW: محدد لضغط Deflate أثناء حفظ النتيجة بصيغة TIFF بـ 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffDeflateRGB: محدد لضغط Deflate أثناء حفظ النتيجة بصيغة TIFF RGB (ملون).
- TiffExpectedFormat.TiffJpegRGB: محدد لضغط Jpeg أثناء حفظ النتيجة بصيغة TIFF RGB (ملون).
- TiffExpectedFormat.TiffJpegYCBCR: محدد لضغط Deflate أثناء حفظ النتيجة بصيغة TIFF YCBCR (ملون).
- TiffExpectedFormat.TiffLzwBW: محدد لضغط LZW أثناء حفظ النتيجة بصيغة TIFF بـ 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffLzwRGB: محدد لضغط LZW أثناء حفظ النتيجة بصيغة TIFF RGB (ملون).
- TiffExpectedFormat.TiffLzwRGBA: محدد لضغط LZW أثناء حفظ النتيجة بصيغة TIFF RGBA (ملون مع شفافية).
- TiffExpectedFormat.TiffNoCompressionBW: محدد لصيغة TIFF غير المضغوطة أثناء حفظ النتيجة بأشكال 1 BitsPerPixel (أسود وأبيض).
- TiffExpectedFormat.TiffNoCompressionRGB: محدد لصيغة TIFF غير المضغوطة أثناء حفظ النتيجة بصيغة RGB (ملون).
- TiffExpectedFormat.TiffNoCompressionRGBA: محدد لصيغة TIFF غير المضغوطة أثناء حفظ النتيجة بصيغة RGBA (ملون مع شفافية).

يوضح مقتطف الشيفرة التالي استخدام حقول TiffExpectedFormat أثناء إنشاء مثيل لفئة TiffOptions.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **الدعم لضغط Deflate وضغط Adobe Deflate**
صيغة ملف TIFF (Tagged Image File Format) تدعم أنواع مختلفة من ضغوط البيانات حيث يتم تخزين نوع الضغط كعلامة (قيمة صحيحة) في الملف. أحد هذه الطرق للضغط هو Adobe Deflate (المعروف سابقًا باسم Deflate). تدعم Aspose.PSD for .NET API هذه الطريقة للضغط لتصدير وإنشاء صور TIFF.

### **حفظ الصورة في TIFF بضغط Deflate**
يمكن تحويل الصور المحملة إلى صيغة TIFF بضغط Deflate/Adobe Deflate بسهولة كما يلي.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}

### **إنشاء صورة TiffImage بضغط Adobe Deflate**
يوضح المثال أدناه استخدام Aspose.PSD for .NET API لإنشاء صورة من البداية باستخدام طريقة ضغط Adobe Deflate.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}

### **ضغط صور TIFF**
يمكن استخدام Aspose.PSD for .NET API لتحويل صور PSD إلى صيغة صورة TIFF وحتى تغيير ضغط الصورة TIFF الناتجة. يمكن أيضًا استخدام الواجهة البرمجية
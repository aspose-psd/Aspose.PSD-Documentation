---
title: تلاعب في صور JPEG
type: docs
weight: 30
url: /ar/net/manipulating-jpeg-images/
---

## **استخدام فئة ExifData لقراءة وتعديل وسوم Jpeg EXIF**
تقوم معظم الكاميرات الرقمية (بما في ذلك الهواتف الذكية)، والماسحات الضوئية، والأنظمة الأخرى التي تتعامل مع الصور بحفظ الصور بمعلومات EXIF (ملف تبادل الصور). تسجل الإعدادات الخاصة بالكاميرا ومعلومات الحالة من قبل الكاميرا في ملف الصورة. تتضمن بيانات EXIF أيضًا سرعة الغالق، وتاريخ ووقت التقاط الصورة، والبعد البؤري، وتعويض التعريض، ونمط قياس الضوء، وما إذا تم استخدام الفلاش أم لا. لقد قامت واجهات برمجة التطبيقات (API) لـ Aspose.Imaging بجعل استخراج معلومات EXIF من صورة معينة أمرًا سهلاً وبسيطًا للغاية. قد يقوم المطورون أيضًا بكتابة بيانات EXIF إلى الصور أو تعديل المعلومات الحالية وفقًا لاحتياجاتهم. لقد قدمت Aspose.PSD فئة [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) لقراءة، كتابة وتعديل البيانات EXIF، بينما تحتوي مساحة الأسماء [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) على التعدادات ذات الصلة المستخدمة في العملية.
### **قراءة البيانات EXIF**
توفر واجهات برمجة التطبيقات (API) لـ Aspose.PSD وسيلة لقراءة بيانات EXIF من صورة معينة. توضح الخطوات المقدمة أدناه استخدام فئة ExifData لقراءة معلومات EXIF من صورة.

- تحميل صورة PSD باستخدام الطريقة القياسية Load.
- العثور على الصورة المصغرة Jpeg بين موارد PSD.
- استخراج مثيل من فئة ExifData.

احصل على المعلومات المطلوبة واكتبها على وحدة التحكم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}

بالإضافة إلى ذلك، يمكن للمطورين أيضًا الحصول على المعلومات الخاصة باستخدام مقتطف الشفرة التالي.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **كتابة وتعديل بيانات EXIF**
باستخدام واجهات برمجة التطبيقات (API) لـ Aspose.PSD، يمكن للمطورين كتابة بيانات EXIF جديدة وتعديل البيانات EXIF الحالية لصورة. كلا العمليتين (الكتابة والتعديل) تتطلب تحميل الصورة والحصول على بيانات EXIF في مثيل من فئة ExifData. يمكن للمطور ثم الوصول إلى الخصائص التي توفرها فئة ExifData لضبطها وفقًا لذلك. يرجى ملاحظة أن الصور التي يجب تلاعبها يجب أن تكون صور Jpeg أو Tiff التي تكون عادة مصغرات PSD. الشفرة العينية لتوضيح الاستخدام كما يلي:
{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **استخراج المصغرات من موارد PSD**
المصغرات هي نسخ مصغرة من الصور، تُستخدم لعرض جزء هام من الصورة بدلاً من الإطار الكامل. بعض ملفات الصور (خاصة تلك التي تم التقاطها بكاميرا رقمية) تحتوي على صورة مصغرة مضمنة في الملف. تسمح واجهة برمجة تطبيقات Aspose.PSD بمعالجة المصغرات من موارد PSD وتخزينها بشكل منفصل على القرص الصلب. تحتوي موارد المصغرات على خاصية صورة مصغرة ExifData.[صورة مصغرة](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) التي يمكن أن تسترد البيانات المصغرة. توضح مقتطف الشفرة التالي كيفية استخدامه.
{{< gist "aspose-com-gists" "bd34ce856d342fc7c0ce974175c8a4" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}
---
title: Manipulating JPEG Images
type: docs
weight: 20
url: /ar/java/manipulating-jpeg-images/
---

## **استخدام فئة ExifData لقراءة وتعديل علامات EXIF في صور JPEG**

تقوم معظم الكاميرات الرقمية (بما في ذلك الهواتف الذكية)، والماسحات الضوئية، والأنظمة الأخرى التي تتعامل مع الصور بحفظ الصور مع معلومات EXIF (ملف تبادل الصور القابل للتبديل). تقوم الكاميرا بتسجيل إعدادات الكاميرا ومعلومات المشهد في ملف الصور. تشمل بيانات EXIF أيضًا سرعة الغالق، وتاريخ ووقت التقاط الصورة، والبعد البؤري، وتعويض التعرض، ونمط القياس، وما إذا تم استخدام الفلاش. APIs Aspose.Imaging قد جعل من الممكن استخراج معلومات EXIF من الصورة المعطاة بطريقة سهلة وبسيطة للغاية. يمكن للمطورين أيضًا كتابة بيانات EXIF إلى الصور أو تعديل المعلومات الحالية وفقًا لاحتياجاتهم. قدمت Aspose.Imaging فئة ExifData لقراءة وكتابة وتعديل بيانات EXIF، حيث تحتوي فضاء الاسم Aspose.PSD.Exif.Enums على التصنيفات ذات الصلة المستخدمة في العملية.
### **قراءة بيانات EXIF**
توفر APIs Aspose.PSD وسيلة لقراءة بيانات EXIF من صورة معينة. توضح الخطوات الواردة أدناه استخدام فئة ExifData لقراءة معلومات EXIF من صورة.

- قم بتحميل صورة PSD باستخدام طريقة المصنع Load.
- ابحث عن الصورة المصغرة JPEG بين مراجع PSD.
- استخرج مثيلًا من فئة ExifData.

احصل على المعلومات المطلوبة واكتبها على الوحدة التحكم.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



بشكل بديل ، يمكن للمطورين أيضًا الحصول على المعلومات المحددة باستخدام مقتطف الكود التالي.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **كتابة وتعديل بيانات EXIF**
باستخدام APIs Aspose.PSD ، يمكن للمطورين كتابة بيانات EXIF جديدة وتعديل بيانات EXIF الحالية لصورة. كلا العمليتين (الكتابة والتعديل) تتطلب تحميل الصورة والحصول على بيانات EXIF في مثيل من فئة ExifData. يمكن بعد ذلك للوصول إلى الخصائص التي تعرضها فئة ExifData لضبطها على النحو المناسب. يرجى ملاحظة أن الصور التي يجب تلاعبها يجب أن تكون صور JPEG أو TIFF التي تكون عادة مصغرات PSD. الشيفرة البرمجية عينة لتوضيح الاستخدام كما يلي:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **استخراج المصغرات من موارد PSD**
المصغرات هي نسخ مصغرة من الصور، تُستخدم لعرض جزء مهم من الصورة بدلاً من الإطار الكامل. يحتوي بعض ملفات الصور (خاصة تلك التي تم التقاطها بواسطة كاميرا رقمية) على صورة مصغرة مضمنة في الملف. تسمح API Aspose.PSD بأستخراج مصغرات موارد PSD وتخزينها بشكل منفصل على القرص. تحتوي موارد المصغرات على خاصية ExifData.Thumbnail التي يمكن استخدامها لاسترداد البيانات المصغرة. يظهر المقتطف البرمجي أدناه كيفية استخدامه.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



استخدم النهج المناقش أعلاه لتخزين المصغرة في تنسيقات ملفات معتمدة أخرى. إذا كنت ترغب في تصدير بيانات المصغرة إلى تنسيقات صور أخرى مثل BMP و PNG، يرجى استخدام خيارات تصدير الصور الأخرى.


### **استخراج المصغرات من أقسام JFIF**
من الممكن أيضًا استخراج المصغرات من قسمي ExifData أو JFIF من موارد المصغرات PSD. يوضح الكود التالي كيفية أداء استخراج البيانات المصغرة من قسم JFIF أو ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



استخدم النهج المناقش أعلاه لتخزين المصغرة في تنسيقات ملفات معتمدة أخرى. إذا كنت ترغب في تصدير بيانات المصغرة إلى تنسيقات صور أخرى مثل BMP و PNG، يرجى استخدام خيارات تصدير الصور الأخرى.
### **إضافة مصغرة إلى قسم JFIF**
يوضح مقتطف الكود أدناه كيفية استخدام خاصية JFIF.Thumbnail لإضافة صورة مصغرة إلى قسم JFIF من صورة PSD المحمّلة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

لا يمكن لصور المصغرات مع بيانات قطعة أخرى أن تحتل أكثر من 65545 بايت بسبب مواصفات تنسيق ملف JPEG. في الحالات التي يتعين فيها ضبط صور كبيرة كصورة مصغرة، قد تحدث استثناءات.


### **إضافة مصغرة إلى قسم EXIF**
يوضح مقتطف الكود أدناه كيفية استخدام خاصية ExifData.Thumbnail لإضافة صورة مصغرة إلى قسم EXIF من صورة PSD المحمّلة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

في هذه الحالة، لا يمكن لواجهة برمجة التطبيقات Aspose.PSD تقدير حجم صورة المصغرة، لكنها يمكن الاطلاع على حجم قطعة البيانات EXIF بأكملها. هذا لا يمكن أن يكون أكبر من 65535 بايت.
## **استخدام فئة JpegExifData لقراءة وتعديل علامات EXIF لصور JPEG**
توفر APIs Aspose.PSD فئة JpegExifData التي حصرية لتنسيقات صور JPEG لاسترداد وتحديث معلومات EXIF. يوضح هذا المقال استخدام فئة JpegExifData لتحقيق نفس الهدف. تعد فئة Aspose.PSD.Exif.JpegExifData في مثابرة Aspose.PSD حاوية بيانات EXIF للصور JPEG، وتوفر وسائل لاسترداد علامات JPEG EXIF القياسية كما هو موضح أدناه:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **قائمة كاملة بعلامات EXIF**
المقتطف البرمجي أعلاه يقرأ بعض العلامات EXIF باستخدام الخصائص المقدمة من فئة Aspose.PSD.Exif.JpegExifData. تتوفر قائمة كاملة بهذه الخصائص هنا. يقرأ الشيفرة التالية جميع العلامات EXIF باستخدام فئة System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **تصحيح التوجيه التلقائي لصور JPEG**
يمكن التقاط الصور بكاميرا مدارة بزواية 90 درجة، 180 درجة، 270 درجة، أو بدون ميل (التوجيه الطبيعي). تخزن معظم الكاميرات الرقمية معلومات التوجيه جنبًا إلى جنب مع بيانات الصورة كعلامات EXIF للصور JPEG. يمكن استخدام هذه المعلومات لإجراء تدوير تلقائي للصور لتصحيح التوجيه. توفر APIs Aspose.PSD الطريقة AutoRotate لفئة JpegImage لتصحيح توجيه الصور JPEG تلقائيًا. هنا كيف يمكنك استخدام طريقة AutoRotate مع API Aspose.PSD للغة جافا.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **دعم لـ JPEG-LS مع CMYK و YCCK**
توفر API Aspose.PSD للغة Java دعمًا لنماذج الألوان CMYK و YCCK مع JPEG-LS. يوضح المقتطف البرمجي أدناه كيفية استخدام هذا الدعم لـ JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **دعم لـ 2-7 بت في صور JPEG-LS**
توفر API Aspose.PSD للغة Java دعمًا لصور JPEG-LS بـ 2-7 بت لكل عينة. يوضح المقتطف البرمجي أدناه كيفية استخدام هذا الدعم لـ JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **تعيين نوع اللون ونوع الضغط لصور JPEG**

توفر API Aspose.PSD للغة Java دعمًا لنوع اللون ونوع الضغط وضبطها على الدرجات الرمادية والتدريجية لصور JPEG. يوضح المقتطف البرمجي أدناه كيفية استخدام هذا الدعم.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}
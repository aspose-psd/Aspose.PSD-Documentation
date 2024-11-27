---
title: تحويل الصور
type: docs
weight: 20
url: /ar/net/converting-images/
---

## **تحويل الصور إلى أبيض وأسود ودرجات اللون الرمادي**
أحيانًا قد تحتاج إلى تحويل الصور الملونة إلى صور أبيض وأسود أو درجات الرمادي لأغراض الطباعة أو الأرشفة. يوضح هذا المقال استخدام Aspose.PSD لـ .NET API لتحقيق ذلك باستخدام طريقتين كما هو موضح أدناه.

- تحويل ثنائي
- تحويل إلى درجات الرمادي

### **تحويل ثنائي**
من أجل فهم مفهوم التحويل الثنائي، من الضروري تعريف الصورة الثنائية؛ وهي صورة رقمية يمكن أن تكون لها قيمتان ممكنتان فقط لكل بكسل. عادةً ما تكون اللونين المستخدمين للصورة الثنائية هما الأسود والأبيض على الرغم من أنه يمكن استخدام أي لونين. يعد التحويل الثنائي عملية تحويل الصور إلى مستوى ثنائي، معنى ذلك هو أن يتم تخزين كل بكسل كبتة واحدة (0 أو 1) حيث يعني 0 عدم وجود لون و1 يعني وجود لون. تدعم حاليًا واجهة برمجة التطبيقات Aspose.PSD لـ .NET اثنتين من طرق التحويل الثنائي.
  
#### **التحويل الثنائي بعتبة ثابتة**
تُظهر مقتطفات الكود التالية كيف يمكن استخدام تحويل الثنائي بعتبة ثابتة على الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}

#### **تحويل الثنائي بعتبة Otsu**
تُظهر مقاطع الكود التالية كيف يمكن تطبيق تحويل الثنائي بعتبة Otsu على الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}

### **تحويل إلى درجات الرمادي**
تعتبر درجات الرمادي هي عملية تحويل الصورة المستمرة إلى صورة تحتوي على درجات رمادية متقطعة. تُظهر مقطع الكود التالي كيفية استخدام تحويل إلى درجات الرمادي.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **تحويل طبقات صور GIF إلى صورة TIFF**
أحيانًا يكون من الضروري استخراج وتحويل طبقات صورة PSD إلى تنسيق صورة نقطية أخرى لتلبية احتياجات التطبيق. يدعم Aspose.PSD API ميزة استخراج وتحويل طبقات صورة PSD إلى تنسيق صورة نقطية آخرى. أولاً، سننشئ مثيلًا من الصورة ونحمل صورة PSD من القرص المحلي، ثم سنكرر كل طبقة في خاصية الطبقات. ثم سوف نحول الكتلة إلى صورة TIFF. يُظهر مقتطف الكود التالي كيفية تحويل طبقات صورة PSD إلى صور TIFF.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **تحويل ملف CMYK PSD إلى TIFF CMYK**
باستخدام Aspose.PSD لـ .NET، يمكن للمطورين تحويل ملف CMYK PSD إلى تنسيق TIFF CMYK. يوضح هذا المقال كيفية تصدير/تحويل ملف CMYK PSD إلى تنسيق TIFF CMYK باستخدام Aspose.PSD. باستخدام Aspose.PSD لـ .NET يمكنك تحميل الصور PSD ومن ثم يمكنك تعيين خصائص مختلفة باستخدام [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class وحفظ أو تصدير الصورة. مقتطف الكود التالي يوضح كيفية تحقيق هذه الميزة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **تصدير الصور**
بجانب مجموعة غنية من الوظائف لمعالجة الصور، يوفر Aspose.PSD فئات متخصصة لتحويل تنسيقات ملفات PSD إلى تنسيقات أخرى. باستخدام هذه المكتبة، يكون تحويل صور PSD بسيطًا وبديهيًا للغاية. فيما يلي بعض الفئات المتخصصة لهذا الغرض ضمن [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) فضاء الاسم.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

من السهل تصدير صور PSD باستخدام Aspose.PSD لـ .NET API. كل ما تحتاجه هو كائن من الفئة المناسبة ضمن [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) فضاء الاسم. باستخدام هذه الفئات، يمكنك بسهولة تصدير أي صورة أنشأت أو نمذجت أو تم تحميلها ببساطة باستخدام Aspose.PSD لـ .NET لأي تنسيق مدعوم.

## **دمج الصور**
يستخدم هذا المثال فئة Graphics ويظهر كيفية دمج صورتين أو أكثر في صورة واحدة كاملة. لتوضيح العملية، تقوم الأمثلة بإنشاء PsdImage جديد وترسم الصور على سطح القماش باستخدام طريقة رسم الصورة المكشوفة بواسطة فئة Graphics. باستخدام فئة Graphics، يمكن دمج صورتين أو أكثر بطريقة تجعل الصورة الناتجة تبدو كصورة كاملة دون فجوات بين أجزاء الصورة ودون صفحات. يجب أن يكون حجم القماش متساويًا بحجم الصورة الناتجة. فيما يلي استعراض الكود الذي يوضح كيفية استخدام [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) بالفئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لدمج الصور في صورة واحدة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **توسيع وقص الصور**
تتيح واجهة API لـ Aspose.PSD للمطورين توسيع أو قص صورة أثناء عملية تحويل الصورة. يحتاج المطور إلى إنشاء مستطيل بإحداثيات X و Y وتحديد عرض وارتفاع مربع المستطيل. ستظهر إحداثي X و Y والعرض والارتفاع للمستطيل توسيع أو قص الصورة المحملة. إذا كان من الضروري توسيع أو قص الصورة أثناء عملية تحويل الصورة، يتوجب على المطور إجراء الخطوات التالية:

1. إنشاء مثيل من [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) فئة وتحميل الصورة الحالية.
1. إنشاء مثيل لفئة ImageOption.
1. إنشاء مثيل من [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) فئة وتهيئة X، Y والعرض والارتفاع للمستطيل.
1. استدعاء طريقة [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) من فئة RasterImage مع تمرير اسم ملف الإخراج، خيارات الصورة وكائن المستطيل كمعلمات.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **قراءة بيانات XMP وكتابتها على الصور**
XMP (Extensible Metadata Platform) هو معيار ISO. يوحد XMP نموذج البيانات، وتنسيق التسلسل والخصائص الأساسية لتعريف ومعالجة البيانات الوصفية القابلة للتوسيع. كما يوفر إرشادات لتضمين معلومات XMP في صورة شائعة مثل JPEG دون أن تفقد قابلية قراءتها بواسطة التطبيقات التي لا تدعم XMP. باستخدام Aspose.PSD لـ .NET API، يمكن للمطورين قراءة أو كتابة البيانات الوصفية XMP للصور. يوضح هذا المقال كيفية قراءة بيانات XMP من صورة وكتابة بيانات XMP على الصور.
### **إنشاء بيانات وصفية XMP وكتابتها وقراءتها من الملف**
بمساعدة مساحة الأسماء Xmp يمكن للمطور إنشاء كائن بيانات وصفية XMP وكتابته على صورة. يوضح مقتطف الكود التالي كيفية استخدام حزم XmpHeaderPi، XmpTrailerPi، XmpMeta، XmpPacketWrapper، PhotoshopPackage وDublinCorePackage الموجودة ضمن [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp) مساحة الأسماء.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}

## **تصدير الصور في بيئة متعددة الخيوط**
Aspose.PSD لـ .NET الآن يدعم تحويل الصور في بيئة متعددة الخيوط. يضمن Aspose.PSD لـ .NET أداء العمليات المحسن خلال تنفيذ الشفرة في بيئة متعددة الخيوط. جميع فئات خيارات الصور (مثل BmpOptions، TiffOptions، JpegOptions، إلخ.) في Aspose.PSD لـ .NET تنفيذ واجهة IDisposable. لذلك من الضروري أن يتصرف المطور بشكل صحيح للتخلص من كائن فئة خيارات الصور في حال تم تعيين خاصية الأصل. يوضح مقتطف الكود التالي هذه الوظيفة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD الآن يدعم خاصية SyncRoot أثناء العمل في بيئة متعددة الخيوط. يمكن للمطور استخدام هذه الخاصية لمزامنة الوصول إلى تدفق المصدر. يوضح مقتط
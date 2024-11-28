---
title: تحويل الصور
type: docs
weight: 20
url: /ar/java/converting-images/
---

## **تحويل الصور إلى أبيض وأسود وتدرج الرمادي**
أحيانًا قد تحتاج إلى تحويل الصور الملونة إلى أبيض وأسود أو تدرج الرمادي لأغراض الطباعة أو الأرشفة. يظهر هذا المقال استخدام Aspose.PSD لواجهة برمجة التطبيقات في جافا لتحقيق ذلك باستخدام طريقتين كما هو مذكور أدناه.

- التثنية
- تدرج الرمادي
### **التثنية**
من أجل فهم مفهوم التثنية، من المهم تعريف الصورة الثنائية؛ وهي صورة رقمية يمكن أن تحتوي على قيمتين ممكنتين فقط لكل بكسل. عادةً، اللونين المستخدمين للصورة الثنائية هما الأسود والأبيض على الرغم من أنه يمكن استخدام أي لونين. التثنية هي عملية تحويل الصورة إلى ثنائية المستوى بحيث يتم تخزين كل بكسل على أنه بت واحد (0 أو 1) حيث يشير 0 إلى عدم وجود لون ويعني 1 وجود لون. تدعم واجهة Aspose.PSD لجافا حاليًا طريقتين للتثنية.
#### **التثنية بحدود ثابتة**
يظهر مقتطف الكود التالي كيف يمكن استخدام التثنية بحدود ثابتة على صورة.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **التثنية بحد الـ Otsu**
يظهر مقتطف الكود التالي كيف يمكن تطبيق التثنية بحد الـ Otsu على صورة.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **تدرج الرمادي**
تدرج الرمادي هو عملية تحويل صورة مستمرة الدرجات إلى صورة مع درجات رمادية متقطعة. يظهر مقتطف الكود التالي كيفية استخدام تدرج الرمادي.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **تحويل طبقات صورة GIF إلى صورة TIFF**
أحيانًا يتعين استخراج وتحويل طبقات صورة PSD إلى تنسيق صورة نقطية أخرى لتلبية احتياج تطبيق ما. تدعم واجهة Aspose.PSD إمكانية استخراج وتحويل طبقات صورة PSD إلى تنسيق صورة نقطية آخرى. أولاً، سنقوم بإنشاء نموذج للصورة وتحميل صورة PSD من القرص المحلي، ثم سنكرر كل طبقة في خاصية الطبقة. ثم سنقوم بتحويل الكتلة إلى صورة TIFF. يظهر مقتطف الكود التالي كيفية تحويل طبقات صورة PSD إلى صور TIFF.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **تحويل PSD CMYK إلى TIFF CMYK**
باستخدام Aspose.PSD لجافا، يمكن للمطورين تحويل ملف PSD CMYK إلى تنسيق TIFF CMYK. يوضح هذا المقال كيفية تصدير/تحويل ملف PSD CMYK إلى تنسيق TIFF CMYK باستخدام Aspose.PSD. باستخدام Aspose.PSD لجافا، يمكنك تحميل صور PSD ثم يمكنك ضبط خصائص مختلفة باستخدام فئة TiffOptions وحفظ أو تصدير الصورة. يظهر مقتطف الكود التالي كيفية تحقيق هذه الميزة.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **تصدير الصور**
توفر Aspose.PSD إلى جانب مجموعة غنية من التوابع لمعالجة الصور، فئات متخصصة لتحويل تنسيقات ملف PSD إلى تنسيقات أخرى. بإستخدام هذه المكتبة، تكون عملية تحويل الصور PSD بسيطة وبديهية للغاية. أدناه بعض الفئات المتخصصة لهذا الغرض في نطاق فئة ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

من السهل تصدير صور PSD بواسطة Aspose.PSD لواجهة برمجة التطبيقات في جافا. كل ما تحتاج إليه هو كائن من الفئة المناسبة من فئة ImageOptions. باستخدام هذه الفئات، يمكنك بسهولة تصدير أي صورة تم إنشاؤها، أو تم تحريرها أو ببساطة تحميلها باستخدام Aspose.PSD إلى أي تنسيق مدعوم.
## **دمج الصور**
يستخدم هذا المثال فئة Graphics ويوضح كيفية دمج صورتين أو أكثر في صورة واحدة كاملة. لتوضيح العملية، يقوم المثال بإنشاء PsdImage جديد ويقوم برسم الصور على سطح القماش باستخدام الأسلوب الذي تطرحه فئة Graphics بإظهار الصور. باستخدام فئة Graphics، يمكن دمج صورتين أو أكثر بطريقة تجعل الصورة الناتجة تبدو كصورة كاملة دون فجوات بين أجزاء الصورة ودون صفحات. يجب أن يكون حجم القماش متطابقًا تمامًا مع حجم الصورة الناتجة. فيما يلي عرض الشيفرة البرمجية التوضيحية التي تُظهر كيفية استخدام الأسلوب Draw Image من فئة Graphics لدمج الصور في صورة واحدة.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **توسيع وتقليم الصور**
تسمح Aspose.PSD بتوسيع أو تقليم صورة أثناء عملية تحويل الصورة. يحتاج المطور إلى إنشاء مستطيل بإحداثيات X و Y وتحديد عرض وارتفاع مربع المستطيل. تُظهر X، Y والعرض والارتفاع للمستطيل التوسيع أو التقليم للصورة المحملة. إذا كانت هناك حاجة إلى توسيع أو تقليم الصورة أثناء عملية تحويل الصورة، قم باتباع الخطوات التالية:

1. إنشاء مثيل من فئة RasterImage وتحميل الصورة الحالية.
1. إنشاء مثيل ImageOption class.
1. إنشاء مثيل من الفئة Rectangle وتهيئة الإحداثيات X، Y والعرض، الارتفاع للمستطيل
1. استدعاء الأسلوب Save من فئة RasterImage بتمرير اسم ملف الإخراج، خيارات الصورة وكائن المستطيل كمعلمات.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **قراءة وكتابة بيانات XMP إلى الصور**
XMP (منصة البيانات الوسيعة القابلة للتوسيع) هي معيار ISO. يقوم XMP بتوحيد نموذج البيانات وتنسيق التسلسل والخصائص الأساسية لتعريف ومعالجة البيانات الوسيعة القابلة للتوسيع. كما يوفر إرشادات لتضمين المعلومات XMP في صور شهيرة مثل JPEG، دون تعطيل قراءتها بواسطة التطبيقات التي لا تدعم XMP. باستخدام Aspose.PSD لواجهة برمجة التطبيقات في جافا يمكن للمطورين قراءة أو كتابة بيانات XMP إلى الصور. يظهر هذا المقال كيف يمكن قراءة بيانات XMP من الصورة وكتابة بيانات XMP إلى الصورة.
### **إنشاء بيانات XMP، كتابتها وقراءتها من الملف**
بمساعدة مساحة الأسماء XMP يمكن للمطور إنشاء كائن بيانات XMP وكتابته في الصورة. يظهر مقتطف الكود التالي كيفية استخدام الباقات XmpHeaderPi و XmpTrailerPi و XmpMeta و XmpPacketWrapper و PhotoshopPackage و DublinCorePackage الموجودة في مجال الأسماء XMP.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **تصدير الصور في بيئة متعددة المواضيع**
Aspose.PSD لجافا تدعم الآن تحويل الصور في بيئة متعددة المواضيع. تضمن Aspose.PSD لجافا أداء العمليات المحسنة أثناء تنفيذ الكود في بيئة متعددة المواضيع. تنفذ جميع فئات خيارات الصور (مثل BmpOptions و TiffOptions و JpegOptions، إلخ) في Aspose.PSD لجافا واجهة IDisposable. لذلك من الضروري أن يتخلص المطور بشكل صحيح من كائن فئات خيارات الصور في حالة تحديد خاصية Source. يوضح الكود التالي هذه الوظيفة.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



في Aspose.PSD تدعم SyncRoot property أثناء العمل في بيئة متعددة المواضيع. يمكن للمطور استخدام هذه الخاصية لتزامن الوصول إلى مصدر التيار. يوضح الكود التالي كيفية استخدام خاصية SyncRoot.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
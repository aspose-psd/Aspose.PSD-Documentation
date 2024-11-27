---
title: تلاعب بتنسيقات Adobe Photoshop
type: docs
weight: 20
url: /ar/net/manipulating-adobe-photoshop-formats/
---

## **دمج طبقات PSD في طبقات أخرى**

## **تصدير الصورة إلى PSD**
تعتبر PSD، وثيقة PhotoShop، هي تنسيق الملف الافتراضي المستخدم من قبل Adobe Photoshop للعمل مع الصور. تسمح Aspose.PSD لك بتحميل وتحرير وحفظ الملفات إلى PSD بحيث يمكن فتحها وتحريرها في Photoshop. يوضح هذا المقال كيفية حفظ ملف إلى PSD باستخدام Aspose.PSD، ويناقش أيضًا بعض الإعدادات التي يمكن استخدامها عند الحفظ بهذا التنسيق. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) هو فئة متخصصة في مساحة [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) تستخدم لتصدير الصور إلى PSD. للتصدير إلى PSD، قم بإنشاء مثيل من الفئة Image، إما بتحميله من ملف صورة موجود (كمصغرات على سبيل المثال) أو إنشاءه من الصفر. يشرح هذا المقال كيفية القيام بذلك. في الأمثلة أدناه، يتم إنشاء صورة من الصفر. بمجرد إنشاء الصورة وملأ البيانات بالبكسل، قم بحفظ الصورة باستخدام طريقة Save التابعة لفئة Image، وقم بتوفير كائن PsdOptions كالمعامل الثاني. يمكن تعيين العديد من خصائص فئة PsdOptions للتحويل المتقدم. بعض الخصائص هي ColorMode، [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) و Version. يدعم Aspose.PSD طرق ضغط التالية من خلال تعداد CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

يتم دعم وضع الألوان التالية من خلال تعداد [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


يمكن إضافة مصادر إضافية، مثل مصادر الصور المصغرة لـ PSD v4.0 و v5.0 والأعلى، أو شبكة المرشدين والمرشدين لـ PSD v4.0 وأعلى. ينشئ الكود أدناه ملف صورة من الصفر، يملأ البكسلات ويحفظه في شكل PSD بضغط RLE ووضع ألوان grayscale. يوضح مقتطف الكود أدناه كيفية تصدير الصورة إلى PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **استيراد الصورة إلى طبقة PSD**
يوضح هذا المقال استخدام Aspose.PSD لإضافة أو استيراد صورة إلى طبقة PSD. تسمح واجهات برمجة التطبيقات في Aspose.PSD باستخدام طرق فعالة وسهلة الاستخدام لتحقيق هذا الهدف. قام Aspose.PSD بفتح طرق الأداء الخاصة بطبقة Layer لإضافة/استيراد صورة في ملف PSD. تحتاج طريقة DrawImage للفئة Layer إلى مواقع وقيم صورة لإضافة/استيراد صورة في ملف PSD. الخطوات لاستيراد صورة إلى طبقة PSD بسيطة كما يلي:

- قم بتحميل ملف PSD كصورة باستخدام الطريقة المصنعة Load المكشوفة من قبل فئة Image.
- إنشاء مثيل لفئة Layer من التيار مع Png ، Jpeg ، Tiff ، Gif ، Bmp ، Psd أو j2k file
- إضافة Layer to Psd باستخدام طريقة AddLayer
- حفظ النتائج.


يوضح مقتطف الكود أدناه كيفية استيراد الصورة إلى طبقة PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **استبدال الألوان في طبقات PSD**
يوضح هذا المقال الاستخدام الرائع لـ Aspose.PSD لإضافة أو استيراد صورة إلى طبقة PSD. قامت واجهات برمجة التطبيقات في Aspose.PSD بتعريض طرق فعالة وسهلة الاستخدام لتحقيق هذا الهدف. لقد قام Aspose.PSD بتعريض طريقة DrawImage من فئة Layer لإضافة/استيراد صورة إلى ملف PSD. تحتاج طريقة DrawImage إلى تحديد موقع قيم الصورة لإضافة/استيراد صورة إلى ملف PSD. الخطوات لاستيراد صورة إلى طبقة PSD بسيطة كما يلي:

- تحميل ملف PSD كصورة باستخدام الطريقة المصنعة Load المكشوفة من قبل فئة Image.
- إنشاء مثيل لفئة Layer وتعيين طبقة صورة PSD لها.
- تحميل الصورة التي يجب إضافتها أو إنشاء واحدة من البداية.
- استدعاء طريقة Layer.DrawImage مع تحديد الموقع ومثيل الصورة.
- حفظ النتائج.


يوضح مقتطف الكود أدناه كيفية استيراد الصورة إلى طبقة PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **إنشاء المصغرات من ملفات PSD**
يعتبر PSD هو التنسيق الوثيق الأصلي لتطبيق Photoshop التابع لشركة Adobe. يقوم Adobe Photoshop (الإصدار 5.0 وما بعده) بتخزين معلومات المصغرة لعرض المعاينة في كتلة موارد الصورة التي تتكون من رأس بدءي بـ 28 بايتًا، تليها مصغرة JFIF بترتيب RGB (أحمر، أخضر، أزرق). يوفر Aspose.PSD API آلية سهلة الاستخدام للوصول إلى موارد ملف PSD. تتضمن هذه الموارد أيضًا مورد المصغرة الذي بدوره يمكن الحصول عليه وحفظه على القرص حسب احتياجات التطبيق. يوضح مقتطف الكود أدناه كيفية إنشاء المصغرات من ملفات PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **إنشاء ملفات PSD المؤشرة**
يمكن لواجهة برمجة التطبيقات Aspose.PSD for .NET إنشاء ملفات PSD المؤشرة من البداية. يوضح هذا المقال استخدام PsdOptions و[PsdImage](https://reference.aspose.com/psd/itm/aspose.psd.fileformats.psd/psdimage) لإنشاء ملف PSD مؤشرة أثناء رسم بعض الأشكال على قماش الذي تم إنشاؤه حديثًا. المراحل البسيطة التالية مطلوبة لإنشاء ملف PSD مؤشرة.

- إنشاء مثيل من PsdOptions وتعيين مصدره.
- ضبط خاصية ColorMode في PsdOptions إلى ColorModes.Indexed.
- إنشاء لوحة جديدة من الألوان من فضاء RGB وتعيينه كخاصية Palette لـ PsdOptions.
- ضبط خاصية CompressionMethod إلى خوارزمية الضغط المطلوبة.
- إنشاء صورة PSD جديدة باستدعاء طريقة PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- رسم الرسومات أو أداء العمليات الأخرى حسب الحاجة.
- استدعاء طريقة PsdImage.Save لتنفيذ جميع التغييرات.


يوضح مقتطف الكود أدناه كيفية إنشاء ملفات PSD المؤشرة.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **تصدير طبقة PSD إلى صورة منخفضة الدقة**
يسمح Aspose.PSD for .NET بتصدير الطبقات في ملف PSD إلى صور نقطية. يرجى استخدام [طريقة Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) لتصدير الطبقة إلى الصورة. يقوم الكود المصدر التالي بتحميل ملف PSD وتصدير كل طبقاته إلى صورة PNG باستخدام طريقة Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. بمجرد تصدير جميع الطبقات إلى صور PNG، يمكنك فتحها باستخدام برنامج عرض الصور المفضل لديك. يوضح مقتطف الكود أدناه كيفية تصدير طبقة PSD إلى صورة نقطية.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **تحديث طبقة النص في ملف PSD**
يسمح Aspose.PSD for .NET بتعديل النص في طبقة النص في ملف PSD. يُرجى استخدام [فئة Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) لتحديث النص في طبقة PSD. يوضح مقتطف الكود التالي كيفية تحميل ملف PSD، والوصول إلى طبقة النص، تحديث النص وحفظ الملف PSD باسم جديد بواسطة [طريقة Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **اكتشاف PSD المسطحة**
يسمح Aspose.PSD for .NET بكشف ما إذا كان ملف PSD معين مسطحًا أو لا. تم إدخال خاصية IsFlatten في فئة Aspose.PSD.FileFormats.Psd.PsdImage لتحقيق هذه الوظيفة. يوضح مقتطف الكود التالي كيفية تحميل ملف PSD والوصول إلى الخاصية [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **دمج طبقات PSD**
يوضح هذا المقال كيفية دمج الطبقات في ملف PSD أثناء تحويل ملف PSD إلى JPG باستخدام Aspose.PSD. في المثال أدناه، يتم تحميل ملف PSD موجود عن طريق تمرير مسار الملف إلى الطريقة الستاتيكية Load من فئة Image. بمجرد تحميله، يتم تحويل / صب الصورة إلى PsdImage. انشئ مثيل لفئة JpegOptions وضع العديد من خصائصه. الآن ادعو طريقة Save لمثيل PsdImage. يوضح مقتطف الكود الت
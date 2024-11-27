---
title: إنشاء، فتح وحفظ ملفات PSD
type: docs
weight: 10
url: /ar/java/إنشاء-فتح-وحفظ-ملفات-psd/
---

## **تصدير الصورة إلى PSD**
ملف PSD، وهو معروف أيضًا باسم مستند PhotoShop، هو تنسيق الملف الافتراضي الذي يستخدمه Adobe PhotoShop للعمل مع الصور. تسمح Aspose.PSD لك بتحميل وتحرير وحفظ الملفات إلى PSD بحيث يمكن فتحها وتحريرها في PhotoShop. يوضح هذا المقال كيفية حفظ ملف إلى PSD باستخدام Aspose.PSD، ويناقش أيضًا بعض الإعدادات التي يمكن استخدامها عند الحفظ في هذا التنسيق. PsdOptions هو فئة متخصصة في فضاء أسماء ImageOptions تُستخدم لتصدير الصور إلى PSD. لتصدير إلى PSD، قم بإنشاء نسخة من فئة Image، إما منتقاة من ملف صورة موجود (على سبيل المثال، المصغرات) أو إنشائها من البداية. يشرح هذا المقال كيفية القيام بذلك. في الأمثلة أدناه، يتم إنشاء صورة من الصفر. بمجرد إنشائها وملأ بيانات البكسل، قم بحفظ الصورة باستخدام طريقة Save في فئة الصورة، وقم بتوفير كائن PsdOptions كالمعامل الثاني. يمكن تعيين العديد من خصائص فئة PsdOptions للتحويل المتقدم. بعض الخصائص هي الوضع اللوني، طريقة الضغط والإصدار. تدعم Aspose.PSD طرق الضغط التالية من خلال تعداد CompressionMethod:

- طريقة الضغط: Raw
- طريقة الضغط: RLE
- طريقة الضغط: ZipWithoutProtection
- طريقة الضغط: ZipWithProtection

يتم دعم وسائط الألوان التالية من خلال تعداد ColorModes:

- وسائط الألوان: Bitmap
- وسائط الألوان: Grayscale
- وسائط الألوان: RGB



يمكن إضافة موارد إضافية، مثل موارد المصغرات لـ PSD v4.0، v5.0 والأعلى، أو موارد الشبكة والأدلة لـ PSD v4.0 وما فوق. ينشئ الكود أدناه ملف BMP من الصفر، يملأ البكسلات ويحفظه إلى PSD بضغط RLE ووضع ألوان الرمادي. الكود المعروض أدناه يوضح كيفية تصدير الصورة إلى PSD.



{{<gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java">}}
## **استيراد الصورة إلى طبقة PSD**
يوضح هذا المقال استخدام Aspose.PSD لإضافة أو استيراد صورة إلى طبقة PSD. قد قدمت واجهات تطبيقات برمجة التطبيقات (APIs) الخاصة بـ Aspose.PSD أساليب فعالة وسهلة الاستخدام لتحقيق هذا الهدف. قد قدمت Aspose.PSD الأسلوب DrawImage في فئة Layer لإضافة/استيراد صورة إلى ملف PSD. يتطلب الأسلوب DrawImage وضع وقيمة الصورة لإضافة/استيراد صورة إلى ملف PSD. الخطوات لاستيراد الصورة إلى طبقة PSD بسيطة كما يلي:

- قم بتحميل ملف PSD كصورة باستخدام الأسلوب المصنع المعروض بواسطة فئة Image.
- قم بإنشاء نسخة من فئة Layer وقم بتعيين طبقة الصورة PSD لها.
- قم بتحميل الصورة التي تحتاج إلى إضافتها أو إنشاء واحدة من البداية.
- استدعي أسلوب DrawImage في الطبقة وأحدد الموقع ونموذج الصورة.
- قم بحفظ النتائج. 



الكود المعروض أدناه يوضح كيفية استيراد الصورة إلى طبقة PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}

## **إنشاء مصغرات من ملفات PSD**
تعتبر PSD تنسيق مستند أساسي لتطبيق Adobe Photoshop. يخزن Adobe Photoshop (الإصدار 5.0 وما بعده) معلومات المصغرات لعرض المعاينة في كتلة موارد الصورة التي تتألف من رأس بدءي بطول 28 بايتًا، تتبعه مصغرة JFIF في ترتيب RGB (أحمر، أخضر، أزرق). يوفر واجهة برمجة تطبيقات (API) Aspose.PSD آلية سهلة الاستخدام للوصول إلى موارد ملف PSD. تتضمن هذه الموارد أيضًا مورد المصغرات الذي من الممكن أن يتم الوصول إليه بدوره ويمكن حفظه على القرص وفقًا لاحتياجات التطبيق. الكود المعروض أدناه يوضح كيفية إنشاء مصغرات من ملفات PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}

## **إنشاء ملفات PSD مؤشرة**
يمكن لواجهة برمجة تطبيقات Aspose.PSD للجافا إنشاء ملفات PSD مؤشرة من البداية. يوضح هذا المقال استخدام فئتي PsdOptions وPsdImage لإنشاء PSD مؤشرة برسم بعض الأشكال فوق القماش الذي تم إنشاؤه حديثًا. الخطوات البسيطة التالية مطلوبة لإنشاء ملف PSD مؤشرة:

- قم بإنشاء نسخة من PsdOptions وقم بتعيين مصدرها.
- قم بتعيين خاصية ColorMode لـ PsdOptions إلى ColorModes.Indexed.
- إنشاء لوحة ألوان جديدة من مساحة RGB وقم بتعيينها كخاصية Palette لـ PsdOptions.
- قم بتعيين خاصية CompressionMethod إلى خوارزمية الضغط المطلوبة.
- إنشاء صورة PSD جديدة بتسمية طريقة PsdImage.Create.
- رسم الرسومات أو تنفيذ عمليات أخرى وفقًا للاحتياج.
- استدعي أسلوب PsdImage.Save لتنفيذ جميع التغييرات.



الكود المعروض أدناه يوضح كيفية إنشاء ملفات PSD مؤشرة.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}

## **تصدير طبقة PSD إلى صورة بيكسلية**
تسمح Aspose.PSD للجافا بتصدير الطبقات في ملف PSD إلى صور بيكسلية. يرجى استخدام طريقة Aspose.PSD.FileFormats.Psd.Layers.Layer.Save لتصدير الطبقة إلى صورة. يقوم الكود العيني التالي بتحميل ملف PSD وتصدير كل طبقة منه إلى صورة PNG باستخدام Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. بمجرد تصدير جميع الطبقات إلى صور PNG، يمكنك فتحها باستخدام عارض الصورة المفضل لديك. الكود المعروض أدناه يوضح كيفية تصدير طبقة PSD إلى صورة بيكسلية.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}

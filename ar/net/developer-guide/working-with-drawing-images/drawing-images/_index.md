---
title: رسم الصور
type: docs
weight: 10
url: /ar/net/drawing-images/
---

## **رسم الخطوط**
هذا المثال يستخدم فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم أشكال الخطوط على سطح الصورة. لتوضيح العملية، يقوم المثال بإنشاء صورة جديدة ورسم الخطوط على سطح الصورة باستخدام الطريقة [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) المكشوفة بواسطة فئة Graphics. أولاً، سنقوم بإنشاء PsdImage محددا ارتفاعه وعرضه.

بمجرد إنشاء الصورة، سنستخدم الطريقة Clear المكشوفة بواسطة فئة Graphics لتعيين لون خلفية الصورة. تستخدم الطريقة [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) من فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم خط على صورة يربط بين اثنين من هياكل النقاط. تأخذ هذه الطريقة عدة تحميلات تقبل نسخة من فئة Pen وأزواج الإحداثيات أو هياكل Point/PointF كوسائط. تعرّف فئة Pen على كائن يستخدم لرسم الخطوط والمنحنيات والأشكال. تحتوي فئة Pen على العديد من المنشئات المحملة لرسم الخطوط بلون وعرض وفرشاة محددين. تُستخدم فئة SolidBrush للرسم المتواصل بألوان محددة. في النهاية يتم تصدير الصورة إلى تنسيق ملف bmp. يوضح المقتطف البرمجي التالي كيفية رسم أشكال الخطوط على سطح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}

## **رسم القطعة الناقصة**
مثال رسم القطعة الناقصة هو المقال الثاني في سلسلة رسم الأشكال. سنستخدم فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم الشكل البيضاوي على سطح الصورة. لتوضيح العملية، يقوم المثال بإنشاء صورة جديدة ورسم شكل البيضاوي على سطح الصورة باستخدام طريقة DrawEllipse المكشوفة بواسطة فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). أولاً، سنقوم بإنشاء PsdImage محددا ارتفاعه وعرضه.

بعد إنشاء الصورة، سنقوم بإنشاء وتهيئة كائن فئة Graphics وتعيين لون خلفية الصورة باستخدام الطريقة Clear من فئة Graphics. تستخدم الطريقة DrawEllipse من فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم شكل البيضاوي على سطح صورة محدد بواسطة هيكل مستطيل الحدود. تأخذ هذه الطريقة عدة تحميلات تقبل نسخ Pen و Rectangle/RectangleF أو نقطة زوج واحدة من الإحداثيات وارتفاع وعرض كوسائط. تعرّف فئة Pen على كائن يستخدم لرسم الخطوط والمنحنيات والأشكال. تحتوي فئة Pen على العديد من المنشئات المحملة لرسم الخطوط بلون وعرض وفرشاة محددين. تخزن فئة Rectangle مجموعة من أربعة أعداد صحيحة تمثل موقع وحجم مستطيل معين. تحتوي فئة Rectangle على العديد من المنشئات المحملة لرسم مستطيل بتعريف حجم وموقع محدد. تُستخدم فئة SolidBrush للرسم المتواصل بألوان محددة. في النهاية يتم تصدير الصورة إلى تنسيق ملف bmp. يوضح المقتطف البرمجي التالي كيفية رسم شكل البيضاوي على سطح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}

## **رسم المستطيل**
في هذا المثال سنقوم برسم شكل المستطيل على سطح الصورة. لتوضيح العملية، سيقوم المثال بإنشاء صورة جديدة ورسم شكل المستطيل على سطح الصورة باستخدام طريقة DrawRectangle المكشوفة بواسطة فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). أولاً، سنقوم بإنشاء PsdImage محددا ارتفاعه وعرضه. ثم سنقوم بتعيين لون خلفية الصورة باستخدام الطريقة Clear من فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

تستخدم الطريقة DrawRectangle من فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم شكل المستطيل على سطح صورة محدد بواسطة هيكل مستطيل. تأخذ هذه الطريقة عدة تحميلات تقبل نسخ Pen و Rectangle/RectangleF أو زوجي الإحداثيات وعرض وارتفاع كوسائط. تحتوي فئة Rectangle على مجموعة من أربعة أعداد صحيحة تمثل الموقع والحجم لمستطيل. تحتوي فئة Rectangle على العديد من المنشئات المحملة لرسم مستطيل بتحديد الحجم والموقع. في النهاية يتم تصدير الصورة إلى تنسيق ملف bmp. يوضح المقتطف البرمجي التالي كيفية رسم شكل المستطيل على سطح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}

## **رسم القوس**
في هذا الجلسة من سلسلة رسم الأشكال، سنقوم برسم شكل القوس على سطح الصورة. سنستخدم طريقة DrawArc من [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لتوضيح العملية على صورة BMP. أولاً، سنقوم بإنشاء PsdImage محددا ارتفاعه وعرضه. بمجرد إنشاء الصورة، سنستخدم الطريقة Clear المكشوفة بواسطة فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لتعيين لون خلفية الصورة.

تستخدم طريقة DrawArc من فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم شكل القوس على سطح صورة. يمثل DrawArc جزءًا من شكل بيضاوي محدد بواسطة هيكل مستطيل الحدود أو زوج الإحداثيات. تأخذ هذه الطريقة عدة تحميلات تقبل نسخ فئات Pen وهيكلي Rectangle/RectangleF أو زوج الإحداثيات وعرض وارتفاع كوسائط. في النهاية يتم تصدير الصورة إلى تنسيق ملف bmp. يوضح المقتطف البرمجي التالي كيفية رسم شكل القوس على سطح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}

## **رسم البيزيه**
يستخدم هذا المثال فئة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم شكل البيزيه على سطح الصورة. لتوضيح العملية، سيقوم المثال بإنشاء صورة جديدة ورسم شكل البيزيه على سطح الصورة باستخدام طريقة DrawBezier المكشوفة بواسطة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). أولاً، سنقوم بإنشاء PsdImage محددا ارتفاعه وعرضه. بمجرد إنشاء الصورة، سنستخدم الطريقة Clear المكشوفة بواسطة [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لتعيين لون خلفية الصورة.

تستخدم طريقة DrawBezier من [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) لرسم شكل SPLINE البيزيه على سطح الصورة المحدد بواسطة أربعة هياكل Point. تأخذ هذه الطريقة عدة تحميلات تقبل نسخ فئة Pen وأربع نقاط ترتيبية أو أربع هياكل Point/PointF أو مصفوفة من هياكل Point/PointF. تعرّف فئة Pen كائن يستخدم لرسم الخطوط والمنحنيات والأشكال. تحتوي فئة Pen على العديد من المنشئات المحملة لرسم الخطوط بلون وعرض وفرشاة محددين. في النهاية يتم تصدير الصورة إلى تنسيق ملف bmp. يوضح المقتطف البرمجي التالي كيفية رسم شكل البيزيه على سطح الصورة.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}

## **رسم الصور باستخدام الوظائف الأساسية**
Aspose.PSD هو مكتبة توفر العديد من الميزات القيمة بما في ذلك إنشاء الصور من البداية. رسم باستخدام الوظائف الأساسية مثل تلاعب بمعلومات البتماب الخاصة بالصورة، أو استخدام ميزات متقدمة مثل [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) و[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) لرسم الأشكال على سطح الصورة بمساعدة فرشاة مختلفة وأقلام مختلفة. باستخدام فئة RasterImage من Aspose.PSD، يمكنك استرداد معلومات بكسل منطقة الصورة وتلاعبها. تحتوي فئة RasterImage على كامل وظائف الرسم الأساسية، مثل الحصول على بكسل وتعيينها وطرق أخرى لتلاعب الصورة. قم بإنشاء صورة جديدة باستخدام أي من الطرق الموصوفة في إنشاء الملفات وتعيينها لمثيل فئة RasterImage. استخدم طريقة LoadPixels في فئة RasterImage لاسترداد معلومات البكسل من جزء من صورة. بمجرد الحصول على مصفوفة البكسل، يمكنك تلاعبها عن طريق تغيير لون كل بكسل، على سبيل المثال. بعد تلاعب بمعلومات البكسل، قم بإعادتها إلى المنطقة المطلوبة في الصورة باستخدام طريقة SavePixels في فئة RasterImage. يوضح المقتطف البرمجي التالي كيفية رسم الصور باستخدام الوظائف الأساسية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
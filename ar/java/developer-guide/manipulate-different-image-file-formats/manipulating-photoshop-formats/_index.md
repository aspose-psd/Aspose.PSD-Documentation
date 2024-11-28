---
title: تعديل صيغ فوتوشوب
type: docs
weight: 10
url: /ar/java/manipulating-photoshop-formats/
---

## **استبدال الألوان في طبقات PSD** 
تسمح Aspose.PSD للجافا بتغيير لون الخلفية لكل طبقة من ملف PSD. يرجى استخدام فئة Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor لتغيير لون خلفية الطبقة في طبقة PSD. تعرض كود الشريحة التالي ملف PSD وصول الطبقة، تحديث اللون الخلفي وحفظ ملف PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.java" >}}

## **تحديث طبقة النص في ملف PSD**
تسمح Aspose.PSD للجافا بالتلاعب في النص في طبقة النص من ملف PSD. يرجى استخدام فئة Aspose.PSD.FileFormats.Psd.Layers.TextLayer لتحديث النص في طبقة PSD. يعرض كود الشريحة التالي تحميل ملف PSD، وصول طبقة النص، تحديث النص، وحفظ ملف PSD باسم جديد باستخدام طريقة Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}

## **الكشف عن PSD المسطح**
تسمح Aspose.PSD للجافا بالكشف عما إذا كان ملف PSD المعطى مسطحًا أم لا. تم إدخال خاصية IsFlatten في فئة Aspose.PSD.FileFormats.Psd.PsdImage لتحقيق هذه الوظيفة. يعرض كود الشريحة التالي تحميل ملف PSD ووصول إلى خاصية IsFlatten.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}

## **دمج طبقات PSD**
يوضح هذا المقال كيفية دمج الطبقات في ملف PSD أثناء تحويل ملف PSD إلى JPG باستخدام Aspose.PSD. في المثال أدناه، يتم تحميل ملف PSD موجود عن طريق تمرير مسار الملف إلى طريقة التحميل الثابتة للفئة Image. بمجرد تحميله، قم بتحويل/صب الصورة إلى PsdImage. أنشئ نسخة من فئة JpegOptions و قم باعدادها بخصائصها المختلفة. الآن قم بنداء طريقة Save من مثيل PsdImage. يعرض الكود المقدم التالي كيفية دمج طبقات PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergePSDLayers-MergePSDLayers.java" >}}

## **دعم الألوان الرمادية مع ألفا لملف PSD**
يوضح هذا المقال كيفية دعم اللون الرمادي مع الألفا لملف PSD أثناء تحويل ملف PSD إلى PNG باستخدام Aspose.PSD. في المثال أدناه، يتم تحميل ملف PSD موجود عن طريق تمرير مسار الملف إلى طريقة التحميل الثابتة للفئة Image. بمجرد تحميله، قم بتحويل/صب الصورة إلى PsdImage. أنشئ نسخة من فئة PngOptions و قم باعداد خصائصها المختلفة. اضبط خاصية ColorType على TruecolorWithAlpha. الآن قم بنداء طريقة Save من مثيل PngOptions. الكود المقدم يظهر لك كيفية تحويل PNG إلى Alphagray.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}

## **دعم تأثيرات الطبقات لملف PSD**
يوضح هذا المقال كيفية دعم تأثيرات مختلفة مثل **Blur**, **Inner** **Glow**, **Outer Glow** لطبقة PSD. يوضح الكود المقدم كيفية دعم تأثيرات الطبقات.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.java" >}}

## **دعم تاريخ ووقت إنشاء الطبقة**
يوضح هذا المقال كيفية دعم إنشاء طبقة تاريخ ووقت في طبقة PSD. يعرض الكود المقدم كيفية إنشاء الطبقات.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.java" >}}

## **دعم تسليط الضوء على ألوان الورقة**
يوضح هذا المقال كيفية تحميل صور PSD ثم تغيير وتسليط الضوء على ألوان الورقة وحفظ ذلك كصورة. تم توفير كود المثال.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.java" >}}

## **دعم طبقات النص عند التشغيل**
يوضح هذا المقال كيفية إضافة طبقات نص عند التشغيل لصور PSD. تم توفير كود المثال أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.java" >}}

## **دعم طبقات التعديل**
يوضح هذا المقال كيفية ضبط الطبقات ومزجها إذا كانت الطبقة فارغة ثم تحفظ كصور PSD. تم توفير كود المثال أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.java" >}}

## **إدارة سطوع وتباين الطبقات في طبقات التعديل**
يوضح هذا المقال كيفية تكرار الطبقات وإدارة سطوع وتباين الطبقات ومن ثم حفظها كصور PSD. تم توفير كود المثال أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageBrightnessContrastAdjustmentLayer-ManageBrightnessContrastAdjustmentLayer.java" >}}

## **إدارة طبقات التعديل للتعرض**
يوضح هذا المقال كيفية إضافة وتحرير طبقات التعرض وإدارتها ثم حفظها كصور PSD. تم توفير كود المثال أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageExposureAdjustmentLayer-ManageExposureAdjustmentLayer.java" >}}

## **إدارة طبقات خلاط القنوات للتعديل**
يوضح هذا المقال كيفية إدارة طبقات التعديل وتعيين ألوان مختلفة ومن ثم حفظها كصور PSD. تم توفير كود المثال أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ManageChannelMixerAdjusmentLayer-ManageChannelMixerAdjusmentLayer.java" >}}

## **دمج طبقات PSD في طبقات أخرى**
يوضح هذا المقال كيفية دمج الطبقات في طبقات أخرى في ملف PSD باستخدام Aspose.PSD. في المثال أدناه، يتم تحميل ملف PSD موجود عن طريق تمرير مسار الملف إلى طريقة التحميل الثابتة للفئة Image. الآن اندفع بنداء طريقة Save من مثيل PsdImage. الكود المقدم يظهر لك كيفية دمج طبقات PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergeOnePSDlayerToOther-MergeOnePSDlayerToOther.java" >}}

## **دعم لـ نطاق حاوية النص**
يوضح هذا المقال كيفية دعم نطاق حاوية النص في ملف PSD باستخدام Aspose.PSD. في المثال أدناه، يتم تحميل ملف PSD موجود عن طريق تمرير مسار الملف إلى طريقة التحميل الثابتة للفئة Image. TextBoundBox هو أقصى حجم لطبقة النص. الآن اندفع بنداء طريقة Save من مثيل PsdImage. الكود المقدم يظهر لك كيفية دمج طبقات PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-TextLayerBoundBox-TextLayerBoundBox.java" >}}

## **دعم للموارد الخارجية IOPA**
يوضح هذا المقال كيفية دعم المصادر IOPA في ملف PSD باستخدام Aspose.PSD. الكود المقدم يظهر لك كيفية دعم IOPA في طبقات PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddIopaResource-AddIopaResource.java" >}}

## **إدارة الشفافية للطبقات**
يوضح هذا المقال كيفية إدارة الشفافية للطبقات في ملف PSD باستخدام Aspose.PSD. تم توفير الكود المقدم أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-FillOpacityOfLayers-FillOpacityOfLayers.java" >}}

## **تقديم طبقات تعديل المنحنيات**
يوضح هذا المقال كيفية تقديم منحنيات التعديل للطبقات في ملف PSD وتقديمها إلى PNG أيضًا باستخدام Aspose.PSD. تم توفير الكود المقدم أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-RenderingOfCurvesAdjustmentLayer-RenderingOfCurvesAdjustmentLayer.java" >}}

## **إضافة طبقات تعديل المنحنيات**
يوضح هذا المقال كيفية إضافة طبقات تعديل المنحنيات في ملف PSD باستخدام Aspose.PSD. تم توفير الكود المقدم أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddCurvesAdjustmentLayer-AddCurvesAdjustmentLayer.java" >}}

## **إضافة طبقات تعديل مخفق القناة**
يوضح هذا المقال كيفية إضافة طبقات تعديل مخلط القناة وتعيين ألوان مختلفة ومن ثم حفظها كصور PSD. تم توفير الكود المقدم أدناه.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddChannelMixerAdjustmentLayer-AddChannelMixerAdjustmentLayer.java" >}}

## **تقديم طبقات تعديل مخلط القناة**
يوضح هذا الم
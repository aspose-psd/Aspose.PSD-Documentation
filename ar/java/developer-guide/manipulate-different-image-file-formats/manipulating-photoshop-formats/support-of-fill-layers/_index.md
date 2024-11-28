---
title: دعم طبقات التعبئة
type: docs
weight: 50
url: /ar/java/support-of-fill-layers/
---


## **دعم طبقات التعبئة بملء اللون**
يوضح هذا المقال كيفية ملء طبقة PSD باللون. يرجى استخدام Aspose.PSD.FileFormats.Psd.Layers.FillLayer لإضافة اللون في طبقة PSD. تحميل مقاطع الكود التالية ملف PSD، والوصول إلى فئة Filllayer وضبط اللون باستخدام خاصية FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **دعم طبقات التعبئة بملء التدرجات**
يوضح هذا المقال استخدام ملء التدرجات لملء طبقة PSD. لقد عرضت واجهات برمجة التطبيقات في Aspose.PSD طرقًا فعالة وسهلة لتحقيق هذا الهدف. لقد قدمت Aspose.PSD فئتي GradientColorPoint وGradientTransparencyPoint لإضافة تأثير التدرجات إلى طبقة.

الخطوات التالية تُظهر كيفية ملء طبقة PSD بملء تدرجي:

- قم بتحميل ملف PSD كصورة باستخدام طريقة الصناعة Load التي تم عرضها بواسطة Image class.
- ضبط خصائص إعدادات كائن FillLayer.
- إنشاء قائمة من ColorPoints بالألوان المطلوبة وموضع اللون.
- إنشاء قائمة transparencyPoints بالشفافية المطلوبة وموضع نقطة الشفافية.
- استدعاء طريقة FillLayer.Update.
- حفظ النتائج.


الكود التالي يظهر لك كيفية إضافة ملء تدرجي لملء طبقة PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **تأثير الحدود مع ملء اللون**
يوضح هذا المقال كيفية عرض تأثير الحدود مع ملء اللون. يتم استخدام تأثير الحدود لإضافة حدود وخطوط إلى الطبقات والأشكال. يمكن استخدامه لإنشاء خطوط لون صلبة، تدرجات ملونة، وكذلك حدود نمطية.

الخطوات لعرض تأثير الحدود بملء اللون بسيطة كالتالي:

- ضبط خاصية **LoadEffectsResource**.
- قم بتحميل ملف PSD كصورة باستخدام طريقة الصناعة Load التي تم عرضها بواسطة Image class وتحديد **PsdLoadOptions**.
- ضبط خصائص إعدادات **ColorFillSetting.**
- حفظ النتائج.

الكود التالي يظهر لك كيفية عرض تأثير الحدود مع ملء اللون.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




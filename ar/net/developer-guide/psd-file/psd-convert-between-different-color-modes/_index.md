---
title: تحويل PSD بين أوضاع الألوان المختلفة
type: docs
weight: 50
url: /ar/net/psd-convert-between-different-color-modes/
---

يمكنك تعلم أوضاع الألوان المدعومة من Aspose.PSD من هذا المقال.

على سبيل المثال، يدعم Aspose.PSD تحويل من 8 إلى 16 بت لكل بكسل والعكس. تحويلات CMYK ICC-Profile وحوار آخر من عمق بت نوع واحد إلى آخر. هنا يمكنك رؤية أمثلة على كيفية التحويل إلى الدرجات الرمادية في ملف PSD.
## **تحويل من CMYK، RGB، الدرجات الرمادية إلى وضع الألوان الرمادي**
الكود المعروض أدناه يوضح كيفية إجراء تحويل CMYK أو RGB أو Grayscale دون الحاجة إلى Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}
## **صورة فوتوشوب 16 بت إلى وضع الألوان الأشباح 8 بت**
ولكن ماذا لو كنت بحاجة إلى تحويل صورة Photoshop 16 بت إلى وضع الألوان الأشباح 8 بت؟ يجب عليك استخدام قطعة الكود التالية. 8 بت هو عمق بت شائع في ملفات PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingIMages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}
## **تحويل من الدرجات الرمادية إلى RGB**
والحالة المعقدة الأخرى إذا كنت بحاجة إلى تحويل صورة Grayscale PSD إلى صورة RGB.

الصور الرمادية تحتوي على قناة واحدة فقط، لكن الصور RGB تحتوي على 3 قنوات: R - أحمر، G - أخضر، B - أزرق. يمكن لـ Aspose.PSD تحويل الصورة الرمادية إلى RGB.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingIMages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
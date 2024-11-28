---
title: دعم طبقات التعبئة
type: docs
weight: 90
url: /ar/net/support-of-fill-layers/
---

## **تعبئة الطبقات بنمط التعبئة**
يوضح هذا المقال كيفية ملء الطبقة [PSD](https://wiki.fileformat.com/image/psd/) بنمط التعبئة. نمط* هو صورة أو لون أو ظل أو خط يُستخدم لملء منطقة في صورة. يرجى استخدام فئة Aspose.PSD.FileFormats.Psd.Layers.FillLayer لإضافة النمط في الطبقة PSD. تحمل مقاطع الكود التالية ملفًا PSD، تصل إلى [فئة Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) وتعيين النمط باستخدام خصائص [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}


هنا مثال آخر يوضح كيف يقوم [Aspose.PSD](https://products.aspose.com/psd/net) بعرض النمط باستخدام [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) و[IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **تعبئة الطبقات بنمط التدرج**
يوضح هذا المقال كيفية استخدام التدرج لملء الطبقة PSD. لقد قامت APIs الخاصة بـAspose.PSD بتعريض طرق فعالة وسهلة لتحقيق هذا الهدف. لقد قامت Aspose.PSD بتعريض فئتي [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) و[GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) لإضافة تأثير التدرج إلى طبقة.

الخطوات لملء [طبقة PSD](https://wiki.fileformat.com/image/psd/) بتدرج التعبئة بسيطة كما يلي:

- قم بتحميل ملف PSD كصورة باستخدام الطريقة المصنعة [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) التي توفرها فئة [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- قم بتعيين خصائص إعدادات [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- قم بإنشاء قائمة من [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) بألوان مطلوبة ومواقع الألوان.
- قم بإنشاء قائمة نقاط الشفافية بشفافية مطلوبة وموقع نقطة الشفافية.
- اتصل بطريقة [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- احفظ النتائج.

المقطع البرمجي التالي يظهر لك كيفية إضافة تدرج التعبئة لملء طبقة PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

هنا مثال آخر يستخدم [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype) لملء طبقة PSD بتدرج تعبئة. يدعم Aspose.PSD أنواع التدرج التالية من خلال تعداد GradientType:

- **GradientType.Linear:** في تدرج خطي، يتحول اللون من اللون البدائي إلى النهاية في خط مستقيم.
- **GradientType.Radial:** في تدرج شعاعي، تنتشر الألوان من نقطة البداية في نمط دائري.
- **GradientType.Angle:** في تدرج الزاوية، يتحرك التدرج باتجاه عقارب الساعة حول نقطة البداية.
- **GradientType.Reflected:** في تدرج معكوس، يتم انعكاس اللون على الجانبين من نقطة البداية.
- **GradientType.Diamond:** تقوم تدرج الماس بإنشاء شكل ماسي من نقطة البداية.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **دعم خاصية التدرج لطبقة التعبئة**
يوضح هذا المقال كيفية تحجيم طبقة FillLayer بالتدرج بالملء باستخدام Aspose.PSD لـ.NET. لهذا الغرض، تمت إضافة خاصية جديدة [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) في [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

فيما يلي عرض الكود الذي يظهر كيفية استخدام خاصية **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **تعبئة الطبقات باللون**
يوضح هذا المقال كيفية ملء الطبقة [PSD](https://wiki.fileformat.com/image/psd/) باللون. يرجى استخدام فئة [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) لإضافة لون إلى طبقة PSD. مقطع الكود التالي يحمل ملف PSD، يصل إلى فئة الطبقة الخاصة بالملء ويعين اللون باستخدام خاصية [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
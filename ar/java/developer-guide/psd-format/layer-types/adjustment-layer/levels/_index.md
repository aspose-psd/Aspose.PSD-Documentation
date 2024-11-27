---
title: طبقة التعديل الأبيض والأسود
type: docs
weight: 30
url: /ar/java/layer-types/adjustment-layer/levels/
---

## العمل مع طبقة تعديل مستويات Photoshop في Java

في هذه المقالة، سنتعلم كيفية ضبط نطاق التوهج وتوازن الألوان لصورة في تنسيق ملف [PSD](/psd/ar/java/psd-format/) برمجيًا في Java. نحن لا نستخدم محرر الصور Adobe® Photoshop® نفسه. بدلاً من ذلك، نستخدم مكتبة Aspose.PSD لـ Java التي تعمل بشكل مستقل للتلاعب في وثيقة Photoshop.

على الرغم من أن Aspose.PSD لـ Java يدعم ما يكفي من [الأدوات لتحرير الصور](/psd/ar/java/manipulating-images/) كما نريد، دعنا **نتبع واجهة برمجة تطبيقات (API) لطبقة تعديل المستويات** التي تُعتبر واحدة من أبسط وأسرع الطرق للقيام بالعمل.

## نظرة عامة على الواجهة البرمجية (API)

التنفيذ الحالي (الإصدار 20.6 في وقت كتابة المقال) لواجهة برمجة تطبيقات طبقة تعديل المستويات **يدعم جميع الميزات الأساسية لمستويات Photoshop** ، وهي ضبط مستويات الإدخال والإخراج لقناة الحاسوب المركبة (RGB) وكذلك لكل قناة لونية رئيسية (أحمر، أخضر وأزرق).

واجهة برمجة تطبيقات طبقة تعديل المستويات مباشرة. الفئة [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) هي نقطة الدخول إلى تعديل المستويات. تحتوي على عدة أساليب للوصول إلى قنوات الألوان: getMasterChannel و getChannel(int). تعود كلتا الطريقتين باسترجاع [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) الذي يحتوي على خصائص تتناغم مع تلاعب مستويات الإدخال والإخراج. الفرق هو أن getMasterChannel يخدم لضبط قناة اللون المركبة (RGB) بينما يُسمح لـ getChannel بالوصول إلى قناة لونية معينة (أحمر، أخضر أو أزرق) عن طريق فهرسها.

## التوافق مع أوضاع الألوان

من الجدير بالإشارة أن طبقة تعديل المستويات **متوافقة مع غالبية أوضاع الألوان** وفقًا لمستويات Photoshop. لذا، يمكن ضبط المستويات للصور في أوضاع اللون الرمادي (قناة رمادية)، RGB (RGB، قنوات الأحمر والأخضر والأزرق)، CMYK (CMYK، قنوات السماوي والقرمزي والأصفر والأسود)، Duotone (قناة أحادية اللون) و LAB (سطوع، قناتي a و b).

## ضبط نطاق التوهج

ببساطة، التصحيح التوهجي يطبق على الصورة لإعادة تعيين الظلال والضوء القوي لتوزيع أفضل للمتوسطات. بشكل عام، **تجعل الصورة تبدو أكثر تباينًا** ، إذا تمت بشكل صحيح. على سبيل المثال، دعنا نأخذ صورة لكلب (b) ونقوم بضبط نطاق توهجها (a - يتم التقاط لقطة الشاشة من نافذة Photoshop Levels للوضوح) لجعل الصورة تبدو أكثر تباينًا (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levels Layer الشكل 1](levels-adjustment-figure-1.png)|

لـ **ضبط نطاق التوهج العام** للصورة، يجب تعيين مستويات الإدخال لقناة الماستر:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **مؤقت** )21);
    masterChannel.setInputMidtoneLevel(( **عائم** )1.19);
    masterChannel.setInputHighlightLevel(( **مؤقت** )229);

يلزم أن تكون مستويات الإدخال في النطاق من 0 إلى 253 للظلال، من 9.99 إلى 0.01 للمتوسطات، ومن 2 إلى 255 للضوء القوي. يجب أن يكون نطاق المستويات الناتجة بين 0 و 255.

هل تحتاج المزيد من الأمثلة؟ يمكنك العثور عليها على [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) وفي [قاعدة المعرفة](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## الاستنتاج

للختام، تتمتع Aspose.PSD لـ Java بواجهة برمجية مفيدة وبسيطة لتغيير نطاق التوهج وتوازن الألوان لصورة متوافقة تقريبًا مع جميع أوضاع الألوان. واجهة برمجة طبقة تعديل المستويات في المكتبة تشابه مستويات Photoshop، لذلك يُسهل البدء حتى إذا لم تكن قد عملت مع المكتبة من قبل.
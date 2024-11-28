---
title: العمل مع الطبقات
type: docs
weight: 150
url: /ar/net/working-with-layers/
---

## **إنشاء مجموعة طبقات**
تتكون مجموعة الطبقات من طبقة أو أكثر وتساعد في تنظيم الطبقات المماثلة أو ذات الصلة. باستخدام Aspose.PSD لـ .NET يمكنك إنشاء مجموعة طبقات. لهذا الغرض، تمت إضافة طريقة جديدة [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) في فئة [PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage) لإضافة المجموعة الطبقية.

الخطوات اللازمة لإنشاء مجموعات الطبقات بسيطة كما يلي:

- قم بإنشاء نسخة من الصورة باستخدام فئة PsdImage مع تحديد العرض والارتفاع وخيارات الصورة.
- قم بإنشاء [LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) بتحديد اسم المجموعة والفهرس.
- قم بإنشاء نسخة من الفئة Layer وقم بتعيين صورة PSD لها.
- أضف الطبقة التي تم إنشاؤها إلى مجموعة الطبقات باستخدام الطريقة AddLayer المكشوفة بواسطة فئة LayerGroup.
- احفظ النتائج.

تُظهر المقطع البرمجي التالي كيفية إنشاء مجموعة طبقات.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **إعادة تسمية طبقة**
يمكنك استخدام أي اسم ترغب فيه، ولكن الممارسة النموذجية هي استخدام وصف عام للكائن أو العنصر الذي يتواجد على تلك الطبقة. توضح هذه المقالة كيف يمكنك تغيير اسم الطبقة باستخدام Aspose.PSD لـ .NET. لهذا الغرض، تمت إضافة خاصية جديدة [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) في فئة Layer لعرض اسم الطبقة بشكل صحيح. لقد لُوحظ أنه عندما يحفظ Photoshop اسم طبقة باستخدام خاصية [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name)، يتم تخزين الأحرف الكورية كبايت 63'?' في ASCII. لذلك، إذا كنت ترغب في عرض اسم الطبقة بشكل صحيح، استخدم خاصية **DisplayName** لأن الخاصية **Name** لا تدعم الأحرف الكورية.

يوضح المثال البرمجي التالي كيفية إعادة تسمية طبقة.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **دعم الطبقات المرتبطة**
ربط الطبقات يشبه تجميع الطبقات. إذا كنت تربط طبقتين أو أكثر فإنه سيسمح لك بإجراء تغييرات معينة على كل من الطبقات المرتبطة. على سبيل المثال، إذا قمت بتطبيق التحويلات على طبقة واحدة، فسيتم تطبيقها على جميع الطبقات المرتبطة الأخرى أيضًا. توضح هذه المقالة كيفية الحصول على الطبقات المرتبطة وإلغاء ربطها باستخدام [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
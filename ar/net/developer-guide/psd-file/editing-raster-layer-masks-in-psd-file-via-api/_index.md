---
title: تحرير أقنعة طبقة الراستر في ملف PSD عبر API
type: docs
weight: 20
url: /ar/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **نظرة عامة**
**لتأتين تحرير تنسيق PSD وتغيير ملف PSD بدون Adobe® Photoshop® يمكنك استخدام Aspose.PSD API المقدمة أدناه. هناك مقتطفات من الرمز C# و.NET التي يمكن أن تساعدك في تعديل ملفات PSD.**

باستخدام أقنعة الطبقة والفيكتور في PSD ، يمكننا إخفاء وإظهار بكسلات الطبقة بدون حذفها بشكل دائم. تُسمى الأقنعة الراسترية أيضًا قناع الطبقة أو قناع المستخدم. توفر الوصول إلى الأقنعة الراسترية والفيكتورية في Aspose.PSD من خلال [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) خاصية الطبقة التي يمكن أن تكون نموذجًا من 'LayerMaskDataShort' و 'LayerMaskDataFull' وتُوفره الفئات الفرعية 'LayerMaskData' المجردة. إذا كان للطبقة كل من الأقنعة الراستر والفيكتور ، يتم توفير حالة [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)المثيل. إذا كان للطبقة قناعان فقط أحدهما راستري أو فيكتوري ، يتم توفير حالة [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)المثيل. إذا كانت خاصية LayerMaskData مجهولة فإن الطبقة ليس لديها أقنعة أو لديها فقط قناع فيكتوري معطل.

|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>قناع راستري وقناع فيكتور معطل LayerMaskDataShort</p><p>قناع راستري معطل LayerMaskDataShort</p><p>قناع راستري وقناع فيكتور LayerMaskDataFull</p><p>قناع راستري LayerMaskDataShort</p><p>قناع فيكتوري LayerMaskDataShort</p><p>قناع فيكتور معطل فارغ (لكن المورد الفيكتوري موجود)</p>|
| :- | :- |

## **كيفية الحصول على قناع راستري للطبقة في ملف PSD?**
أولاً ، يجب علينا أن نعرف ما إذا كانت للطبقة كل من الأقنعة الفيكتورية والطبقية:

يوضح الرمز العيني أدناه كيفية الحصول على قناع راستري للطبقة

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

إلا إذا كان نوع الخاصية LayerMaskData طبقة LayerMaskDataShort. في هذه الحالة ، دعونا نتحقق مما إذا كانت الطبقة تحتوي فقط على قناع راستري عن طريق فحص خاصية Flags. لا يجب أن تحتوي على مؤشرات الطبقة [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** ، وإلا فإن القناع هو ذاكرة احتياطية لقناع فيكتوري.

الحصول على مقتطف الكود:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

إذا كنت بحاجة إلى **استخراج قناع راستري** كـ LayerMaskDataShort (للتلاعب اللاحق) حتى عند وجود كلا القناعين ، يجب استخراج LayerMaskDataFull وتحويلها إلى LayerMaskDataShort. يمكن استخدام الرمز التالي لكلا الحالتين:

استخراج قناع راستري من PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}

## **كيفية التحقق مما إذا كانت الطبقة في ملف PSD لها قناع راستري؟**
قد تساعدك الرمز التالي باللغة C# في التحقق مما إذا كانت الطبقة تحتوي على قناع راستري:

كيفية معرفة ما إذا كان هناك قناع راستري تم تطبيقه على [طبقة PSD](/psd/ar/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}

## **كيفية إزالة / إضافة / تحديث قناع راستري في ملف PSD؟**
مجرد إزالة / إضافة / تحديث LayerMaskData ليس كافيًا للحفظ الصحيح لأن القنوات لم يتم تحديثها. على الرغم من أنه قد يوفر الأداء الصحيح. هذا لا يؤثر على قنوات القناع:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

يجب علينا استخدام طريقة AddLayerMask الخاصة بالطبقة للإزالة / الإضافة / التحديث.

هذا يضيف/يحدث كل من القناع والقنوات:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

هذا يزيل كل من القناع والقنوات:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}

## **إزالة قناع راستري لطبقة في صورة PSD**
أولاً ، نتحقق مما إذا كان القناع في الصيغة القصيرة وإذا لم يكن قناعًا فيكتوريًا يمكننا فقط استدعاء طريقة AddLayerMask بقيمةً غير محددة لحذف القناع الراستري. ولكن إذا كان في الصيغة الكاملة ، يجب علينا تحويله إلى صيغة قصيرة مما يترك القناع الفكتوري فقط. لحذف قناع الطبقة يمكن استخدام الكود التالي بلغة C# .NET:

مقتطف الكود حول كيفية إزالة قناع الطبقة من ملف PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

## **تحديث قناع راستري لطبقة في صورة PSD**
هذا بسيط: إذا كان القناع في الصيغة القصيرة يجب علينا تغيير ImageData و MaskRectangle إذا كان الأمر ضروريًا ، في حالة أخرى يجب تغيير [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)و [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle). يمكن استخدام مقتطف الكود التالي بلغة C# .NET لتحديث قناع الطبقة:

تحديث قناع طبقة PSD مع C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

هنا مثال على الإجراءات الممكنة التي تغير قناعًا راستريًا. يقوم هذا بعكس قناع المستخدم في الطبقة:

تحديث قناع PSD للطبقة مع C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}

## **تحديث قناع فيكتوري في ملف PSD عند وجود قناع راستري لمستوى الطبقة**
يُفترض أن المستخدم قد قام بتغيير مورد المسار الفيكتوري بالفعل. يمكنه بعد ذلك تحديث القناع الفيكتوري ببساطة عن طريق استدعاء طريقة AddLayerMask الفئة [PSD Layer Vector Mask ](/psd/ar/net/layer-vector-mask/) :

تحديث [قناع طبقة PSD الفيكتوري](/psd/ar/net/layer-vector-mask/) بلغة C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}

## **إضافة قناع راستري لطبقة في ملف PSD**
إذا لم يكن للطبقة أي قناع يمكننا إضافة القناع الراستري المعطى عن طريق استدعاء طريقة AddLayerMask .

إذا لم تحتوي القناع على [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)فإنه بالفعل يحتوي على قناع راستري ويجب تحديثه كما هو موضح أعلاه. وإلا ، إذا كان هذا القناع في الصيغة القصيرة نحوله إلى الصيغة الكاملة. إذا لم يكن كذلك ، فيجب علينا استخدامه كما هو. ثم يتم تحديث UserMaskData و UserMaskRectangle وخصائص أخرى بخصائص القناع المحددة. يمكن استخدام مقتطف الكود التالي بلغة C# .NET لإضافة (تحديث) قناع الطبقة:

إضافة قناع طبقة جديد إلى PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **كيفية التحقق مما إذا كان قناع الطبقة مفعّلًا؟**
لمعرفة حالة تمكين قناع الطبقة الراستري ، يمكننا التحقق من حالة العلم LayersMaskFlags.Disabled في الخاصية Flags لـ LayerMaskDataShort أو في RealFlags لـ LayerMaskDataFull. يمكن استخدام مقتطف الكود التالي بلغة C# .NET للحصول على حالة تمكين قناع الطبقة:

تحقق مما إذا كان القناع مفعلًا:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}

## **كيفية تمكين أو تعطيل قناع طبقة راستري؟**
لتمكين أو تعطيل قناع طبقة راستري يمكننا تغيير حالة العلم LayerMaskFlags.Disabled في الخاصية Flags لـ LayerMaskDataShort أو في RealFlags لـ LayerMaskDataFull. يمكن استخدام مقتطف الكود التالي بلغة C# .NET لتغيير حالة تمكين قناع الطبقة:

تمكين أو تعطيل قناع راستري:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
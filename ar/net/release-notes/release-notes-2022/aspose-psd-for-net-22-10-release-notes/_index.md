---
title: أسبوز بي اس دي لـ .NET 22.10 - ملاحظات الإصدار
type: docs
weight: 30
url: /ar/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أسبوز بي اس دي لـ .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- هذا الإصدار به خطأ انحدار في حالة الصدور على 16 بت، لذا نوصي بالحذر عند استخدام هذه الميزة في هذا الإصدار.
يرجى عدم تحديث أسبوز بي اس دي إلى 22.9-22.10 إذا كان معالجة الصور بـ 16 بت هي وظيفتك الأساسية.

نحن نعمل على حلول لهذه المشاكل.

{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1287|إزالة الخصائص القديمة في مصدر Lfx2|تحسين|
|PSDNET-1071|أسبوز بي اس دي لا يمكن فتح PSD (RGB/16بت) مع ضغط ZipWithoutPrediction|خلل|
|PSDNET-1257|تختفي تأثيرات الجدول الزمني وتظهر بطريقة غريبة. (في فوتوشوب)|خلل|
|PSDNET-1278|الشفافية لا تعمل لتأثير السكتة مع وضع الداخل|خلل|
|PSDNET-1279|انحدار: خطأ عند فتح ملف PSD|خلل|
|PSDNET-1284|تحديث النص يفشل مع بعض الرموز الآسيوية. خطأ في تحليل رمز محدد|خلل|
|PSDNET-1291|تحديث النص يفشل مع بعض الرموز الآسيوية. خطأ في تقديم رمز محدد|خلل|
|PSDNET-1292|خطأ عند فتح الملف المصدر بواسطة فوتوشوب بعد حفظ رموز آسيوية محددة|خلل|


## **تغييرات الواجهة الخارجية**
## **واجهات برمجة التطبيقات المضافة:**
- لا شيء


## **واجهات برمجة التطبيقات المحذوفة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity

## **أمثلة الاستخدام:**

**PSDNET-1071. أسبوز بي اس دي لا يمكن فتح PSD (RGB/16بت) مع ضغط ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. تختفي تأثيرات الجدول الزمني وتظهر بطريقة غريبة. (في فوتوشوب)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // إنشاء جدول زمني مع عدة إطارات.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. الشفافية لا تعمل لتأثير السكتة مع وضع الداخل**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. انحدار: خطأ عند فتح ملف PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. تحديث النص يفشل مع بعض الرموز الآسيوية. خطأ في تحليل رمز محدد**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // تحديد الرمز المشكل

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. إزالة الخصائص القديمة في مصدر Lfx2**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // تحديث خيار وضع الخلط للتأثير
    effect.BlendMode = BlendMode.Darken;

    // تحديث خيار الشفافية للتأثير
    effect.Opacity = 128; // 50%

    // تحديث تعبئة لون تأثير السكتة
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. تحديث النص يفشل مع بعض الرموز الآسيوية. خطأ في تقديم رمز محدد**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // تحديد الرموز المشكلة

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. خطأ عند فتح الملف المصدر بواسطة فوتوشوب بعد حفظ رموز آسيوية محددة**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
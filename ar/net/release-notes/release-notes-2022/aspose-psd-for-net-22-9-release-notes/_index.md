---
title: ملاحظات الإصدار Aspose.PSD for .NET 22.9
type: docs
weight: 40
url: /ar/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


{{% alert color="warning" %}}

- هذا الإصدار يحتوي على انحدار في حالة تصدير الصور بعمق 16 بت، لذلك نوصي بالحذر عند استخدام هذه الخاصية في هذا الإصدار. يرجى عدم تحديث Aspose.PSD إلى الإصدار 22.9 إذا كانت معالجة الصور بعمق 16 بت هي وظيفتك الأساسية.
- لبعض إصدارات Photoshop، قد يواجه المستخدمون نافذة تظهر خطأ في قراءة الطبقة، ولن يؤثر هذا على العمل مع ملف PSD.

نحن نعمل على حلول لهذه المشاكل.

{{% /alert %}}


|**الرقم**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1237|إنشاء نموذج طبقة داخلي يحتوي على تأثيرات وبيانات ذات صلة لاستخدام النموذج الواحد في مصادر التأثيرات Lfx2 و lmfx و mlst|تعزيز|
|PSDNET-1227|إضافة قراءة وكتابة لهياكل 'Lefx' مع معلومات تأثيرات لحالات الطبقات في نماذج TimeLine|ميزة|
|PSDNET-1230|تطبيق حالة طبقة TimeLine على الطبقة في PsdImage|ميزة|
|PSDNET-1072|شفافية غير صحيحة عند حفظ ملف PSD (RGB/16 بت) عند التصدير إلى 8 بت|خلل|
|PSDNET-1140|استثناء عند تحميل خطوة موارد الطبقة العالمية عند فتح مستند PSB|خلل|
|PSDNET-1266|تسرب الذاكرة أثناء معالجة ملفات معينة|خلل|


## **تغييرات الواجهة العامة**
# **APIs المضافة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs المحذوفة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **أمثلة الاستخدام:**

**PSDNET-1072. شفافية غير صحيحة عند حفظ ملف PSD (RGB/16 بت) عند التصدير إلى 8 بت**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // خيارات الحفظ 16 بت
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // حفظ الصورة بألوان 16 بت
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. استثناء عند تحميل خطوة موارد الطبقة العالمية عند فتح مستند PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // يجب أن لا يكون هناك استثناء.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. إضافة قراءة وكتابة لهياكل 'Lefx' مع معلومات تأثيرات لحالات الطبقات في نماذج TimeLine**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. تطبيق حالة طبقة TimeLine على الطبقة في PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // تغيير الإطار النشط من 0 إلى 1 لتفعيل تطبيق LayerState على الطبقة
    timeLine.ActiveFrame = 1;

    // تطبيق التغييرات على PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. تسرب الذاكرة أثناء معالجة ملفات معينة**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total used bytes before test: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // CheckOpenSaving
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total used bytes after test: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "تسرب ذاكرة في الوظيفة الأساسية تم اكتشافه!");
{{< /highlight >}}
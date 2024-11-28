---
title: تحديثات Aspose.PSD لـ .NET 22.11
type: docs
weight: 20
url: /ar/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}
هذه الصفحة تحتوي على تحديثات إصدار [Aspose.PSD لـ .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

{{% alert color="warning" %}}
- يحتوي هذا التحديث على عيب في حالة تصدير الصور بعمق 16 بت، لذا نوصي بالحذر عند استخدام هذه الميزة في هذا الإصدار.
الرجاء عدم تحديث Aspose.PSD إلى الإصدارات من 22.9 إلى 22.11 إذا كان معالجة الصور بعمق 16 بت هي وظيفتك الأساسية.

نحن نعمل على حلول لهذه المشكلات.
{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1320|تعذر تصدير ملفات PSB كبيرة للغاية|تعزيز|
|PSDNET-659|جعل مركز التدرج الإشعاعي قابل للتحريك|ميزة|
|PSDNET-1330|طريقة ضغط ZipWithoutPrediction غير مدعومة للملفات المحددة|ميزة|
|PSDNET-735|بعد استخدام طريقة التحويل لطبقة واحدة فقط، يكون حاوي الطبقة الذي تم حفظه به علامة ارتباط غير صحيحة|خلل|
|PSDNET-1234|استثناء عند تحميل صورة PSD تحتوي على نمط|خلل|
|PSDNET-1244|فشل تصدير الصورة (فهرس خارج النطاق) عند حفظ ملف PSD يحتوي على رموز صينية|خلل|
|PSDNET-1303|تطبيق الإطار الزمني يكون غير صحيح|خلل|
|PSDNET-1307|عيب 22.7: عدم تقديم صحيح للنصوص التي تحتوي على أحرف عربية|خلل|
|PSDNET-1321|لقناع الشكل النووي على طبقة المجموعة يعمل بشكل غير صحيح. الصورة النهائية تحتوي على حفرة سوداء ولكن يجب ألا تحتوي|خلل|


## **التغييرات العامة في واجهة البرمجة التطبيقية**
# **APIs المضافة:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)

# **APIs المحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-659. جعل مركز التدرج الإشعاعي قابل للتحريك**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // تحديث نقطة الإزاحة
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. بعد استخدام طريقة التحويل لطبقة واحدة فقط، يكون حاوي الطبقة الذي تم حفظه به علامة ارتباط غير صحيحة**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // تحديد حجم جديد لطبقة النص
    const int NewWidth = 250;
    const int NewHeight = 250;

    // تحديد آلية كيف ستعيد الدالة تحديد الحجم للطبقة
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // آلية جديدة لتغيير حجم طبقة النص
    // ستتغير ليس فقط الطبقة ولكن أيضًا مصفوفة التحويل الخاصة بطبقة النص
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // السبب في الفارق هو اختلاف الخط الأفتراضي
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // كل شيء على ما يرام
    }
    else
    {
        throw new Exception("يوجد خطأ في نقطة الموقع");
    }
}
{{< /highlight >}}

**PSDNET-1234. استثناء عند تحميل صورة PSD تحتوي على نمط**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. فشل تصدير الصورة (فهرس خارج النطاق) عند حفظ ملف PSD يحتوي على رموز صينية**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // لا يجب أن يحدث هناك أي استثناء
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. تطبيق الإطار الزمني يكون غير صحيح**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. عيب 22.7: عدم تقديم صحيح للنصوص التي تحتوي على أحرف عربية**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. تعذر تصدير ملفات PSB كبيرة للغاية**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. لقناع الشكل النووي على طبقة المجموعة يعمل بشكل غير صحيح. الصورة النهائية تحتوي على حفرة سوداء ولكن يجب ألا تحتوي**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. طريقة ضغط ZipWithoutPrediction غير مدعومة للملفات المحددة**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
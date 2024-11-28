---
title: گزارش نسخه‌های منتشر شده Aspose.PSD برای .NET 22.10
type: مستندات
weight: 30
url: /fa/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی گزارش نسخه برای [Aspose.PSD برای .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

{{% alert color="warning" %}}

- این نسخه دارای یک مشکل در مورد صدور 16 بیته است، بنابراین توصیه می‌شود در استفاده از این قابلیت در این نسخه با احتیاط عمل نمایید. لطفاً Aspose.PSD را به 22.9-22.10 ارتقا ندهید اگر پردازش تصاویر 16 بیتی عملکرد اصلی شما است.

ما در حال کار بر روی رفع این مشکلات هستیم.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-1287|حذف ویژگی‌های قدیمی در منبع Lfx2|افزایش کارآمدی|
|PSDNET-1071|Aspose.PSD نمی‌تواند فایل PSD (RGB/16بیتی) با فشرده‌سازی ZipWithoutPrediction را باز کند|خطا|
|PSDNET-1257|اثرات زمان‌بندی ناپدید شده و به شکل عجیبی نمایش داده می‌شوند. (در فتوشاپ)|خطا|
|PSDNET-1278|شفافیت برای اثر Stroke با موقعیت داخلی کار نمی‌کند|خطا|
|PSDNET-1279|رگرسیون: خطا در بازکردن فایل PSD|خطا|
|PSDNET-1284|به‌روزرسانی متن با خطاهای نمادهای آسیایی. خطا در تجزیهٔ نماد خاص|خطا|
|PSDNET-1291|به‌روزرسانی متن با خطاهای نمادهای آسیایی. خطا در رندر کردن نماد خاص|خطا|
|PSDNET-1292|خطا در بازکردن فایل صادرشده توسط فتوشاپ پس از ذخیره نمادهای آسیایی خاص|خطا|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- هیچ


# **API‌های حذف شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **مثال‌های استفاده:**

**PSDNET-1071. Aspose.PSD نمی‌تواند فایل PSD (RGB/16بیتی) با فشرده‌سازی ZipWithoutPrediction را باز کند**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. اثرات زمان‌بندی ناپدید شده و به شکل عجیبی نمایش داده می‌شوند. (در فتوشاپ)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // تولید زمان‌بندی با چند فریم.
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

**PSDNET-1278. شفافیت برای اثر Stroke با موقعیت داخلی کار نمی‌کند**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. رگرسیون: خطا در بازکردن فایل PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. به‌روزرسانی متن با خطاهای نمادهای آسیایی. خطا در تجزیهٔ نماد خاص**

{{< highlight csharp >}}
string testData = @"尐..."; // انتخاب نماد مشکل‌دار

testData = testData.Substring(25, 1);

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. حذف ویژگی‌های قدیمی در منبع Lfx2**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // به‌روزرسانی گزینهٔ BlendMode اثر
    effect.BlendMode = BlendMode.Darken;

    // به‌روزرسانی گزینهٔ Opacity اثر
    effect.Opacity = 128; // 50%

    // به‌روزرسانی گزینهٔ Color پر کردن اثر stroke
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. به‌روزرسانی متن با خطاهای نمادهای آسیایی. خطا در رندر کردن نماد خاص**

{{< highlight csharp >}}
string testData = @"..."; // انتخاب نمادهای مشکل‌دار

testData = testData.Substring(40, 25);

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. خطا در بازکردن فایل صادرشده توسط فتوشاپ پس از ذخیره نمادهای آسیایی خاص**

{{< highlight csharp >}}
string testData = @"尐...";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}

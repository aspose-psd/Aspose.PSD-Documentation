---
title: یادداشت های نسخه Aspose.PSD برای.NET 22.11
type: docs
weight: 20
url: /fa/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت های نسخه برای [Aspose.PSD برای .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

{{% alert color="warning" %}}

- این نسخه دارای یک عود در مورد صادرات 16 بیتی است ، بنابراین توصیه می‌شود احتیاط ورودی به کار در این نسخه. 
لطفا Aspose.PSD را به 22.9-22.11 به‌روز نکنید اگر پردازش تصویر 16 بیتی عملکرد اصلی شما باشد.

ما در حال کار بر روی راه‌حل برای این مشکلات هستیم.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-1320|نمی‌توان فایل‌های PSB بسیار بزرگ را صادر کرد|افزوده شده|
|PSDNET-659|مرکز گرادیان شعاعی قابل حرکت شود|ویژگی|
|PSDNET-1330|روش فشرده‌سازی ZipWithoutPrediction برای فایل‌های خاص پشتیبانی نمی‌شود|ویژگی|
|PSDNET-735|بعد از استفاده از یک متد تبدیل فقط برای یک لایه ، لایه ذخیره شده دارای جعبه محدود نادرست می‌شود|خطا|
|PSDNET-1234|استثناء در بارگذاری تصویر PSD با الگو|خطا|
|PSDNET-1244|صادرات تصویر ناموفق (IndexOutOfRangeException) در ذخیره فایل PSD با نمادهای چینی|خطا|
|PSDNET-1303|TimeLine ActiveFrame بدون موقعیت اعمال می‌شود|خطا|
|PSDNET-1307|عود 22.7: بازنمایی نادرست متن با کاراکترهای عربی|خطا|
|PSDNET-1321|پوشش برداری در لایه گروه برداری اشتباه کار می‌کند. تصویر نهایی دارای چاله سیاه است ولی نباید داشته باشد|خطا|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.Psd.ResizeType)


# **API‌های حذف شده:**
- هیچ کدام


## **مثال‌های استفاده:**

**PSDNET-659. مرکز گرادیانِ شعاعی قابل حرکت شود**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // بروزرسانی نقطه آفست
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. بعد از استفاده از یک متد تبدیل فقط برای یک لایه ، لایه ذخیره شده دارای جعبه محدود نادرست می‌شود**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // اندازه جدید لایه متن را تنظیم می‌کند
    const int NewWidth = 250;
    const int NewHeight = 250;

    // مکانیزمی که نحوه تغییر اندازه تابع را تغییر می‌دهد
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // مکانیزم جدید تغییر اندازه برای لایه متن که در اینجا استفاده شده است
    // نه تنها لایه بلکه همچنین ماتریس تبدیل لایه متن تغییر می‌کند
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // دلیل اختلاف مکانی نوع فونت پیش‌فرض متفاوت است
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // همه چیز خوب است
    }
    else
    {
        throw new Exception("مکان نقطه اشتباه است");
    }
}
{{< /highlight >}}

**PSDNET-1234. استثناء در بارگذاری تصویر PSD با الگو**

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

**PSDNET-1244. صادرات تصویر ناموفق (IndexOutOfRangeException) در ذخیره فایل PSD با نمادهای چینی**

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

    // در اینجا باید هیچ استثنا باشد.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame بدون موقعیت اعمال می‌شود**

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

**PSDNET-1307. عود 22.7: بازنمایی نادرست متن با کاراکترهای عربی**

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

**PSDNET-1320. نمی‌توان فایل‌های PSB بسیار بزرگ را صادر کرد**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. پوشش بردارِ روی لایه گروه اشتباه کار می‌کند. تصویر نهایی دارای چاله سیاه است ولی نباید داشته باشد**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. روش فشرده‌سازی ZipWithoutPrediction برای فایل‌های خاص پشتیبانی نمی‌شود**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}

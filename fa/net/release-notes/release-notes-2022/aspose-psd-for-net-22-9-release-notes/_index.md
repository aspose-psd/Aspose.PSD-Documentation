---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 22.9
type: docs
weight: 40
url: /fa/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD برای .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- این نسخه دارای یک عقب‌نشینی در مورد صدور 16 بیت دارد، بنابراین توصیه می‌کنیم که در استفاده از این ویژگی در این نسخه محتاط باشید. لطفاً Aspose.PSD را به نسخه ۲۲.۹ ارتقا ندهید اگر پردازش تصویر ۱۶ بیتی، اصلی‌ترین ویژگی شماست.
- برای چند نسخه از فتوشاپ، کاربران ممکن است با پنجره‌ای که خطای خواندن لایه در آن وجود دارد مواجه شوند، این مورد بر روی کار با فایل PSD تاثیری نخواهد گذاشت.

ما در حال پیگیری راه‌حل‌های این مشکلات هستیم.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-1237|ایجاد مدل داخلی لایه‌ای که حاوی اثرات و داده‌های مرتبط برای استفاده از مدل تک در منابع اثرات Lfx2، lmfx و mlst است|بهبود|
|PSDNET-1227|افزودن خواندن و نوشتن ساختارهای 'Lefx' با اطلاعات اثرات برای وضعیت‌های لایه در مدل‌های TimeLine|ویژگی|
|PSDNET-1230|اعمال وضعیت لایه TimeLine به لایه در PsdImage|ویژگی|
|PSDNET-1072|شفافیت نادرست در ذخیره فایل PSD (RGB/16 بیتی) در زمان صدور به 8 بیت|اشکال|
|PSDNET-1140|استثناء در مرحله بارگذاری منابع لایه سراسری هنگام باز کردن سند PSB|اشکال|
|PSDNET-1266|نشتی حافظه در پردازش فایل‌های خاص|اشکال|


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
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


# **API‌های حذف شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **مثال‌های استفاده:**

**PSDNET-1072. شفافیت نادرست در ذخیره فایل PSD (RGB/16 بیتی) در زمان صدور به 8 بیت**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // گزینه‌های صدور 16 بیتی
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // ذخیره تصویر با رنگ‌های 16 بیتی
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. استثناء در مرحله بارگذاری منابع لایه سراسری هنگام باز کردن سند PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // اینجا نباید استثنا وجود داشته باشد.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. اضافه کردن خواندن و نوشتن ساختارهای 'Lefx' با اطلاعات اثرات برای وضعیت‌های لایه در مدل‌های TimeLine**

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

**PSDNET-1230. اعمال وضعیت لایه TimeLine به لایه در PsdImage**

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

    // تغییر جلوترین فریم از ۰ به ۱ برای فعال کردن اعمال LayerState به Layer
    timeLine.ActiveFrame = 1;

    // اعمال تغییرات بر روی PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. نشتی حافظه در پردازش فایل‌های خاص**

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

    // بررسی باز کردن و ذخیره
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
Assert.IsTrue(Math.Abs(memCount - max) < 20, "نشتی حافظه در عملکرد اساسی یافت شد!");
{{< /highlight >}}

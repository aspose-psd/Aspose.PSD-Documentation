---
title: یادداشت های نسخه Aspose.PSD برای .NET 22.12
type: docs
weight: 10
url: /fa/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- در این نسخه یک بازگشتی با صادرات 16 بیتی برطرف شد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-1336|افزودن ویژگی TextOrientation قابل ویرایش به رابط IText|ویژگی|
|PSDNET-725|تغییر اندازه فایل PSD مشخص شده با لایه ماسک باعث ایجاد ماسک نادرست می شود|خطا|
|PSDNET-1277|افزودن قابلیت ذخیره و بارگذاری ماسک برای 16 تصویر|خطا|
|PSDNET-1281|شفافیت نادرست در ذخیره کردن تصویر 16 بیتی به تصویر 16 یا 8 بیتی|خطا|
|PSDNET-1375|رفع مشکل CMYK در رنگ 16 بیت|خطا|


## **تغییرات در API عمومی**
# **API های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **API های حذف شده:**
- هیچکدام


## **مثال های استفاده:**

**PSDNET-725. تغییر اندازه فایل PSD مشخص شده با لایه ماسک باعث ایجاد ماسک نادرست می شود**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// باز کردن فایل PSD منبع
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // تغییر اندازه
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// باز کردن فایل PSD تغییر اندازه داده شده
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // رندر کردن به PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. افزودن قابلیت ذخیره و بارگذاری ماسک برای 16 تصویر**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // گزینه‌ها به ما اجازه ذخیره رنگ 16 بیتی را می‌دهد
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // فایل PSD با شفافیت ذخیره می‌شود
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. شفافیت نادرست در ذخیره کردن تصویر 16 بیتی به تصویر 16 یا 8 بیتی**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// باز کردن فایل psd 16 بیتی رنگ (با شفافیت) و ذخیره به رنگ 16 بیتی
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// فایلی که به فرمت psd 16 بیتی رنگ ذخیره شده است به فایل png با شفافیت رندر می‌شود
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. اضافه کردن ویژگی TextOrientation قابل ویرایش به رابط IText**

{{< highlight csharp >}}
// کد زیر نشان دهنده قابلیت ویرایش ویژگی TextOrientation است.
// این تاثیری بر روی رندرینگ در حالت داده شده ندارد، بلکه فقط به شما امکان ویرایش مقدار ویژگی را می‌دهد.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // خواندن صحیح
    }
    else
    {
        throw new Exception("خواندن نادرست از مقدار ویژگی TextOrientation");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // خواندن صحیح
    }
    else
    {
        throw new Exception("خواندن نادرست از مقدار ویژگی TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. رفع CMYK در رنگ 16 بیت**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// تنظیم گزینه های تبدیل
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// تبدیل و ذخیره
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// باز کردن فایل تبدیل شده و رندر کردن به PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

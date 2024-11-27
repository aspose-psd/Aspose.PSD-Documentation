---
title: گزارش‌های ویرایش Aspose.PSD برای .NET 24.1
type: docs
weight: 120
url: /fa/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی گزارش‌های ویرایش برای [Aspose.PSD برای .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                                       | **دسته‌بندی** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [فرمت AI] افزودن قابلیت هندلینگ پایه برای تصاویر AI چندصفحه‌ای                            |   ویژگی   |
| PSDNET-718  | اثر متن پیچیده بر روی متن اعمال نمی‌شود                                                       |     اشکال     |
| PSDNET-1620 | نادرست رندر کردن ماسک در فایل خاص                                                         |     اشکال     |
| PSDNET-1855 | NullReferenceException در Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor    |     اشکال     |
| PSDNET-1883 | [فرمت AI] رفع مشکل مصرف حافظه در AiExporterUtils                                            |     اشکال     |



## **تغییرات API عمومی**
# **API های اضافه شده:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDNET-718. اثر متن پیچیده بر روی متن اعمال نمی‌شود**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. نادرست رندر کردن ماسک در فایل خاص**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [فرمت AI] افزودن قابلیت هندلینگ پایه برای تصاویر AI چندصفحه‌ای**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// بارگذاری تصویر AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // به طور پیش‌فرض، ActivePageIndex 0 است.
    // بنابراین اگر تصویر AI را بدون تغییر در این ویژگی ذخیره کنید، صفحه اول رندر و ذخیره خواهد شد.
    image.Save(firstPageOutputPng, new PngOptions());

    // فهرست صفحات فایل AI را مشاهده کنید.
    image.ActivePageIndex = 1;

    // دومین صفحه تصویر AI را به عنوان تصویر PNG ذخیره کنید.
    image.Save(secondPageOutputPng, new PngOptions());

    // فهرست صفحات فایل AI را مشاهده کنید.
    image.ActivePageIndex = 2;

    // سومین صفحه تصویر AI را به عنوان تصویر PNG ذخیره کنید.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException در Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [فرمت AI] رفع مشکل مصرف حافظه در AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// بارگذاری تصویر AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // صفحه اول تصویر AI را به عنوان تصویر PNG ذخیره کنید.
    image.Save(firstPageOutputPng, new PngOptions());

    // فهرست صفحات فایل AI را مشاهده کنید.
    image.ActivePageIndex = 1;

    // دومین صفحه تصویر AI را به عنوان تصویر PNG ذخیره کنید.
    image.Save(secondPageOutputPng, new PngOptions());

    // فهرست صفحات فایل AI را مشاهده کنید.
    image.ActivePageIndex = 2;

    // سومین صفحه تصویر AI را به عنوان تصویر PNG ذخیره کنید.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("مصرف حافظه بیش از حد است. " + memoryUsed + " به جای " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}

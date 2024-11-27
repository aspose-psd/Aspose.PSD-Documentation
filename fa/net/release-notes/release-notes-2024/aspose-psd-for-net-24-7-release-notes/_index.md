---
title: Aspose.PSD برای .NET 24.7 - یادداشت‌های نسخه
type: docs
weight: 60
url: /fa/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

صفحه حاوی یادداشت‌های نسخه برای [Aspose.PSD برای .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

| **کلید**   | **خلاصه**                                                                                          | **دسته‌بندی** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | استثنای "بارگذاری تصویر ناموفق است." هنگام باز کردن سند AI                  | باگ     |
| PSDNET-2022 | متن به طور نادرست در فایل‌های PDF خروجی نمایش داده می‌شود                    | باگ     |
| PSDNET-2061 | رفع استثنای ImageSaveException: صدور تصویر برای فایل داده شده در لینوکس ناموفق است    | باگ     |
| PSDNET-2080 | رفع مشکلات بارگذاری فونت‌ها هنگام استفاده از Aspose.Drawing                      | باگ     |
| PSDNET-2085 | 'عملیات حسابی به یک سیلان منجر می‌شود' هنگام ایجاد لایه Smart Object با استفاده از JPEG بزرگ       | باگ     |
| PSDNET-2100 | فایل AI نمی‌تواند به یک فایل JPG تبدیل شود                                           | باگ     |

## **تغییرات API‌های عمومی**
# **API‌های اضافه شده:**
- هیچ‌کدام

# **API‌های حذف شده:**
- هیچ‌کدام

## **مثال‌های استفاده:**

**PSDNET-1029. استثنای "بارگذاری تصویر ناموفق است." هنگام باز کردن سند AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. متن به طور نادرست در فایل‌های PDF خروجی نمایش داده می‌شود**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. رفع استثنای ImageSaveException: صدور تصویر برای فایل داده شده در لینوکس ناموفق است**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. رفع مشکلات بارگذاری فونت‌ها هنگام استفاده از Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- پیش از به‌روزرسانی. تعداد فونت‌های نصب شده: " + installedFonts.Families.Length);
    Console.WriteLine("- پلتفرم: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- تازه سازی حافظه نهان فونت با سعی در گرفتن نام فونت آدوب برای 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- پس از به‌روزرسانی. تعداد فونت‌های نصب شده: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'عملیات حسابی به یک سیلان منجر می‌شود' هنگام ایجاد لایه Smart Object با استفاده از JPEG بزرگ**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. فایل AI نمی‌تواند به یک فایل JPG تبدیل شود**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

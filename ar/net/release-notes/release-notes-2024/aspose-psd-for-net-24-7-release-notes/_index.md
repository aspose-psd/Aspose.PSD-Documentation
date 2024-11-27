---
title: أصبوز.PSD لـ .NET 24.7 - ملاحظات الإصدار
type: docs
weight: 60
url: /ar/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [أصبوز.PSD لـ .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص** | **الفئة** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | استثناء "فشل تحميل الصورة" عند فتح مستند AI | خلل |
| PSDNET-2022 | تقديم النص بشكل غير صحيح في ملفات PDF الناتجة | خلل |
| PSDNET-2061 | إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux | خلل |
| PSDNET-2080 | إصلاح تحميل الخطوط عند استخدام Aspose.Drawing | خلل |
| PSDNET-2085 | 'العملية الحسابية أدت إلى تجاوز' عند إنشاء طبقة كائن ذكي باستخدام JPEG كبير | خلل |
| PSDNET-2100 | لا يمكن تحويل ملف AI إلى ملف JPG | خلل |

## **تغييرات الAPI العامة**
# **APIs المضافة:**
- لا شيء

# **APIs المحذوفة:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-1029. استثناء "فشل تحميل الصورة" عند فتح مستند AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. تقديم النص بشكل غير صحيح في ملفات PDF الناتجة**

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

**PSDNET-2061. إصلاح استثناء ImageSaveException: فشل تصدير الصورة للملف المعطى على نظام Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. إصلاح تحميل الخطوط عند استخدام Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- قبل التحديث. عدد الخطوط المثبتة: " + installedFonts.Families.Length);
    Console.WriteLine("- النظام: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- قم بتحديث ذاكرة التخزين المؤقتة للخطوط عن طريق محاولة الحصول على اسم الخط Adobe لـ 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- بعد التحديث. عدد الخطوط المثبتة: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'العملية الحسابية أدت إلى تجاوز' عند إنشاء طبقة كائن ذكي باستخدام JPEG كبير**

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

**PSDNET-2100. لا يمكن تحويل ملف AI إلى ملف JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
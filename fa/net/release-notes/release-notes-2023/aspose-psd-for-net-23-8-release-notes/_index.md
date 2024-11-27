---
title: Aspose.PSD for .NET 23.8 - یادداشت های نسخه
type: docs
weight: 50
url: /fa/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت های نسخه [Aspose.PSD برای .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

| **کلید**     | **خلاصه**                                                                                                  | **دسته‌بندی** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | اضافه کردن نوع تغییر شکل جدید (پرچم) | ویژگی |
| PSDNET-1621 | اضافه کردن انواع جدید تغییر شکل: پیچ بالا، پیچ پایین، کره | ویژگی |
| PSDNET-1682 | پیاده سازی‌‌ ادغام جدید PsdImage.AddPosterizeAdjustmentLayer برای اضافه کردن لایه جدید پوسراز | ویژگی |
| PSDNET-913  | اطلاعات PSD در هنگام فقط باز کردن و ذخیره کردن از بین می‌روند | باگ     |
| PSDNET-1352 | بارگیری تصویر ناموفق بود | باگ     |
| PSDNET-1553 | بارگیری تصویر ناموفق بود: قادر به تبدیل شیء از نوع UnknownStructure به نوع DescriptorStructure نیست | باگ     |
| PSDNET-1631 | فایل تغییر کرد در کتابخانه شخص ثالث پرونده PSD را فاسد می‌کند اما می توان آن را در فتوشاپ باز کرد | باگ     |


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **API‌های حذف شده:**
- هیچکدام


## **مثال‌های استفاده:**

**PSDNET-913. اطلاعات PSD در هنگام فقط باز کردن و ذخیره کردن از بین می‌روند**

{{< highlight csharp >}}
string src = "فایل اصلی.psd";
string outputPsd = "خروجی_فایل اصلی.psd";
string outputPng = "خروجی_فایل اصلی.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. بارگیری تصویر ناموفق بود**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. بارگیری تصویر ناموفق بود: قادر به تبدیل شیء از نوع UnknownStructure به نوع DescriptorStructure نیست**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // باید به درستی بارگیری شود
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. فایل تغییر کرد در کتابخانه شخص ثالث پرونده PSD را فاسد می‌کند اما می توان آن را در فتوشاپ باز کرد**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. اضافه کردن نوع تغییر شکل جدید (پرچم)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. اضافه کردن انواع جدید تغییر شکل: پیچ بالا، پیچ پایین، کره**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. پیاده سازی‌‌ ادغام جدید PsdImage.AddPosterizeAdjustmentLayer برای اضافه کردن لایه جدید پوسراز**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// چک کردن تغییرات ذخیره شده
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "اشیاء مساوی نیستند.");
    }
}
{{< /highlight >}}

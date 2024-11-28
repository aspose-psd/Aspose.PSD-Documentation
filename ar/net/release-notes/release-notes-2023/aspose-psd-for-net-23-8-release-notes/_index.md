---
title: Aspose.PSD for .NET 23.8 - Release Notes
type: docs
weight: 50
url: /ar/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **الرقم**    | **الملخص**                                                                                                      | **الفئة** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | إضافة نوع جديد من التشويه (العلم) | ميزة |
| PSDNET-1621 | إضافة أنواع جديدة من التشويه: قوس لأعلى، قوس لأسفل، كرة | ميزة |
| PSDNET-1682 | تنفيذ طريقة جديدة PsdImage.AddPosterizeAdjustmentLayer لإضافة طبقة Posterize جديدة | ميزة |
| PSDNET-913  | فقدان معلومات PSD فقط عند فتحها وحفظها | خلل     |
| PSDNET-1352 | فشل تحميل الصورة | خلل     |
| PSDNET-1553 | فشل تحميل الصورة: تعذر على صنف من النوع UnknownStructure أن يتحول إلى نوع DescriptorStructure | خلل     |
| PSDNET-1631 | تغيير الملف في مكتبة الطرف الثالث يفسد ملف PSD ولكن يمكن فتحه في Photoshop | خلل     |


## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المضافة:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **APIs المحذوفة:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDNET-913. فقدان معلومات PSD فقط عند فتحها وحفظها**

{{< highlight csharp >}}
string src = "ملف أصلي.psd";
string outputPsd = "ناتج_ملف أصلي.psd";
string outputPng = "ناتج_ملف أصلي.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. فشل تحميل الصورة**

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

**PSDNET-1553. فشل تحميل الصورة: تعذر على صنف من النوع UnknownStructure أن يتحول إلى نوع DescriptorStructure**

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
            // يجب أن يتم التحميل بشكل صحيح
        }
    }
}
{{< /highlight >}}



**PSDNET-1631. تغيير الملف في مكتبة الطرف الثالث يفسد ملف PSD ولكن يمكن فتحه في Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. إضافة نوع جديد من التشويه (العلم)**

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

**PSDNET-1621. إضافة أنواع جديدة من التشويه: قوس لأعلى، قوس لأسفل، كرة**

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


**PSDNET-1682. تنفيذ طريقة جديدة PsdImage.AddPosterizeAdjustmentLayer لإضافة طبقة Posterize جديدة**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// التحقق من التغييرات المحفوظة
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
        throw new Exception(message ?? "الكائنات غير متساوية.");
    }
}
{{< /highlight >}}
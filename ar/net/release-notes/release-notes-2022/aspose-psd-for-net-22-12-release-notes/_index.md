---
title: Aspose.PSD لـ .NET 22.12 - ملاحظات الإصدار
type: docs
weight: 10
url: /ar/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- تم إصلاح خطأ في هذا الإصدار يتعلق بتصدير 16 بت.

{{% /alert %}}

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1336|إضافة خاصية التوجيه القابلة للتحرير إلى واجهة IText|ميزة|
|PSDNET-725|تغيير حجم ملف PSD المحدد مع إنتاج التنميق غير الصحيح للطبقة المنقولة|خطأ|
|PSDNET-1277|إضافة القدرة على حفظ وتحميل قناع لـ 16 صورة|خطأ|
|PSDNET-1281|شفافية غير صحيحة عند حفظ صورة 16 بت إلى صورة 16 بت أو 8 بت|خطأ|
|PSDNET-1375|إصلاح نموذج CMYK في 16 بت لون|خطأ|


## **تغييرات واجهة برمجة التطبيقات العامة**
# **APIs المضافة:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **APIs المزالة:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDNET-725. تغيير حجم ملف PSD المحدد مع إنتاج التنميق غير الصحيح للطبقة المنقولة**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// يتم فتح ملف PSD المصدر
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // يتم تغيير الحجم 
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// يتم فتح ملف PSD المغيّر الحجم
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // يتم إنشاء PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. إضافة القدرة على حفظ وتحميل قناع لـ 16 صورة**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // الخيارات تسمح بحفظ لون 16 بت
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // سيتم حفظ ملف PSD بشفافية
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. شفافية غير صحيحة عند حفظ صورة 16 بت إلى صورة 16 بت أو 8 بت**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// سيتم فتح ملف PSD لون 16 بت (مع الشفافية) وحفظه بلون 16 بت
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// سيتمتع ملف PSD الذي تم حفظه بلون 16 بت بالتنميق إلى ملف png مع الشفافية
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. إضافة خاصية التوجيه القابلة للتحرير إلى واجهة IText**

{{< highlight csharp >}}
// يوضح الكود التالي القدرة على تحرير خاصية التوجيه الجديدة.
// هذا لا يؤثر على التشكيل في الوقت الحالي، ولكن يسمح لك بتحرير قيمة الخاصية فقط.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // قراءة صحيحة
    }
    else
    {
        throw new Exception("قراءة غير صحيحة لقيمة خاصية التوجيه");
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
        // قراءة صحيحة
    }
    else
    {
        throw new Exception("قراءة غير صحيحة لقيمة خاصية التوجيه");
    }
}
{{< /highlight >}}

**PSDNET-1375. إصلاح نموذج CMYK في 16 بت لون**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// تعيين خيارات التحويل
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// التحويل والحفظ
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// فتح الملف المحول والتنميق إلى PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
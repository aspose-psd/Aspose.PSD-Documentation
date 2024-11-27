---
title: تحديثات إصدار Aspose.PSD لـ .NET 24.1
type: docs
weight: 120
url: /ar/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على تحديثات إصدار لـ [Aspose.PSD لـ .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **الرمز**   | **الملخص**                                                                                       | **التصنيف** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [صيغة AI] إضافة معالجة أساسية لصور AI متعددة الصفحات                                         |   ميزة      |
| PSDNET-718  | تأثير تحريف النص لا يُطبق على النص                                                            |     خطأ    |
| PSDNET-1620 | تقديم غير صحيح للقناع في الملف المحدد                                                      |     خطأ    |
| PSDNET-1855 | استثناء NullReferenceException في Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor |    خطأ    |
| PSDNET-1883 | [صيغة AI] إصلاح استخدام الذاكرة في AiExporterUtils                                          |    خطأ    |



## **تغييرات الواجهة البرمجية العامة**
# **APIs المضافة:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs التي تمت إزالتها:**
- لا شيء


## **أمثلة الاستخدام:**

**PSDNET-718. تأثير تحريف النص لا يُطبق على النص**

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

**PSDNET-1620. تقديم غير صحيح للقناع في الملف المحدد**

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

**PSDNET-1835. [صيغة AI] إضافة معالجة أساسية لصور AI متعددة الصفحات**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// تحميل الصورة AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // بشكل افتراضي، ActivePageIndex هو 0.
    // لذا إذا قمت بحفظ الصورة AI دون تغيير هذه الخاصية، سيتم تقديم الصفحة الأولى وحفظها.
    image.Save(firstPageOutputPng, new PngOptions());

    // تغيير مؤشر الصفحة الفعالة إلى الصفحة الثانية.
    image.ActivePageIndex = 1;

    // حفظ الصفحة الثانية من الصورة AI كصورة PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // تغيير مؤشر الصفحة الفعالة إلى الصفحة الثالثة.
    image.ActivePageIndex = 2;

    // حفظ الصفحة الثالثة من الصورة AI كصورة PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. استثناء NullReferenceException في Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

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

**PSDNET-1883. [صيغة AI] إصلاح استخدام الذاكرة في AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// تحميل الصورة AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // حفظ الصفحة الأولى من الصورة AI كصورة PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // تغيير مؤشر الصفحة الفعالة إلى الصفحة الثانية.
    image.ActivePageIndex = 1;

    // حفظ الصفحة الثانية من الصورة AI كصورة PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // تغيير مؤشر الصفحة الفعالة إلى الصفحة الثالثة.
    image.ActivePageIndex = 2;

    // حفظ الصفحة الثالثة من الصورة AI كصورة PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("استخدام الذاكرة كبير جدًا. " + memoryUsed + " بدلاً من " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
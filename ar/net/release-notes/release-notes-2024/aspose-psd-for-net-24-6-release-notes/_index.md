---
title: ملاحظات الإصدار لـ Aspose.PSD لـ .NET 24.6
type: docs
weight: 70
url: /ar/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **المفتاح** | **الملخص**                                                                         | **الفئة** |
|:------------|:-------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | تنفيذ دعم طبقة خريطة التدرج                                                                               | ميزة      |
| PSDNET-1670 | [تنسيق AI] إضافة دعم لبيانات الوحدة إلى تنسيق AI                                                                               | ميزة      |
| PSDNET-1831 | تنفيذ أنواع نفخ وضغط ولف الانحناءات                                                                               | ميزة      |
| PSDNET-1653 | لا يمكن لأوضاع RGB و Lab أن تحتوي على أقل من 3 قنوات وأكثر من 4 قنوات في الملف مع طبقات ArtBoard                                                                               | خلل      |
| PSDNET-1775 | يجب أن يكون موضع المعالجة العلوي موجبًا (المعلمة 'areaToProcess') عند معالجة ملف محدد                                                                               | خلل      |
| PSDNET-2052 | تم قص الصورة الموسعة فوق صورة القماش بعد الحفظ. يتم فقدان البيانات ولكن يبدو المعاينة صحيحة                                                                               | خلل      |

## **تغيرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة تطبيقات:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **تمت إزالة واجهات برمجة التطبيقات:**
- لا شيء

## **أمثلة الاستخدام:**

**PSDNET-1450. تنفيذ دعم طبقة خريطة التدرج**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // إضافة طبقة ضبط خارطة التدرج.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// التحقق من التغييرات المحفوظة
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "الكائنات ليست متساوية.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [تنسيق AI] إضافة دعم لبيانات الوحدة إلى تنسيق AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("الكائنات ليست متساوية.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("كائن الاختبار فارغ.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // تمت إضافة بيانات الوحدة.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // يمكننا الآن الوصول إلى حزم Xmp لملفات AI.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // ولدينا الوصول إلى محتوى هذه الحزم.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. تنفيذ أنواع نفخ وضغط ولف الانحناءات**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. لا يمكن لأوضاع RGB و Lab أن تحتوي على أقل من 3 قنوات وأكثر من 4 قنوات في الملف مع طبقات ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // يجب ألا يحدث استثناء هنا
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. يجب أن يكون موضع المعالجة العلوي موجبًا. (المعلمة 'areaToProcess') عند معالجة ملف محدد**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // لا ينبغي أن يحدث استثناء
}
{{< /highlight >}}

**PSDNET-2052. تم قص الصورة الموسعة فوق صورة القماش بعد الحفظ. يتم فقدان البيانات ولكن يبدو المعاينة صحيحة**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // لا ينبغي حدوث خطأ هنا
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // لا ينبغي حدوث خطأ هنا
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
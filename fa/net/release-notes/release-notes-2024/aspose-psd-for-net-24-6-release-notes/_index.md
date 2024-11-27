---
title: اسناد Aspose.PSD برای .NET 24.6 - یادداشت‌های انتشار
type: مستندات
weight: 70
url: /fa/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

| **کلید**    | **خلاصه**                                                                                       | **دسته‌بندی** |
|:------------|:-------------------------------------------------------------------------------------|:------------|
| PSDNET-1450 | پیاده سازی پشتیبانی از لایه نقشه‌ی گرادیان| قابلیت‌     |
| PSDNET-1670 | [فرمت AI] افزودن پشتیبانی از اطلاعات فراداده XPacket به فرمت AI                              | قابلیت‌     |
| PSDNET-1831 | پیاده سازی انواع تورم Inflate، Squeeze، و Twist                                 | قابلیت‌     |
| PSDNET-1653 | حالت‌های Rgb و Lab نمی‌توانند حاوی کمتر از 3 کانال یا بیش از 4 کانال در فایلهای با لایه‌های ArtBoard باشند| باگ      |
| PSDNET-1775 | بالای بخش پردازش باید مثبت باشد. (پارامتر 'areaToProcess') در پردازش فایل خاص                                                | باگ      |
| PSDNET-2052 | پس از ذخیره‌سازی، تصویر گسترده بر روی توپر کادر تصویر بریده می‌شود. داده از دست می‌رود اما پیش‌نمایش صحیح است                                               | باگ      |

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API‌های حذف شده:**
- هیچکدام

## **نمونه‌های کاربرد:**

**PSDNET-1450. پیاده سازی پشتیبانی از لایه نقشه‌ی گرادیان**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // افزودن لایه تنظیم گرادیان.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// بررسی تغییرات ذخیره‌شده
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
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [فرمت AI] افزودن پشتیبانی از اطلاعات فراداده XPacket به فرمت AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("اشیاء برابر نیستند.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("اشیاء آزمون تهی هستند.");
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
    // فراداده Xmp اضافه شد.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // حالا می‌توانیم به بسته‌های Xmp فایل‌های AI دسترسی پیدا کنیم.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // و دسترسی به محتوای این بسته‌ها را داریم.
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

**PSDNET-1831. پیاده سازی انواع تورم Inflate، Squeeze، و Twist**

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

**PSDNET-1653. حالت‌های Rgb و Lab نمی‌توانند حاوی کمتر از 3 کانال یا بیش از 4 کانال در فایلهای با لایه‌های ArtBoard باشند**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // اینجا نباید خطا ایجاد شود
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. بخش پردازش بالایی باید مثبت باشد. (پارامتر 'areaToProcess') در پردازش فایل خاص**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // باید خطا ایجاد نشود
}
{{< /highlight >}}

**PSDNET-2052. پس از ذخیره‌سازی، تصویر گسترده بر روی توپر کادر تصویر بریده می‌شود. داده از دست می‌رود اما پیش‌نمایش صحیح است**

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
    // اینجا نباید هیچ خطایی ایجاد شود
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // اینجا نباید هیچ خطایی ایجاد شود
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

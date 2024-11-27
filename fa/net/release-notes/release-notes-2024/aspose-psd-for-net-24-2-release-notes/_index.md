---
title: یادداشت‌های نسخه Aspose.PSD برای .NET 24.2
type: docs
weight: 110
url: /fa/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD نسخه 24.2 برای .NET](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **کلید**   | **خلاصه**                                                               | **دسته‌بندی** |
|:----------|:-------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Handle خاصیت زاویه برای PatternFillSettings                            |   قابلیت   |
| PSDNET-1719 | پشتیبانی از مقیاس عمودی و افقی برای TextLayer                     |     قابلیت     |
| PSDNET-1783 | [قالب AI] پیاده‌سازی صحیح تصویر زمینه در فرمت AI مبتنی بر PDF |     قابلیت     |
| PSDNET-1611 | تغییر مکانیزم Distort در warp                                        |     بهبود     |
| PSDNET-1802 | افزایش سرعت warp                                                     |     بهبود     |
| PSDNET-995  | استثناء "بارگذاری تصویر انجام نشد." هنگام باز کردن سند           |     باگ     |
| PSDNET-1491 | رفع ذخیره کردن پرونده‌های psd حاوی الگوی Stroke                 |     باگ     |
| PSDNET-1642 | استایل متن اشتباه است در یک شیوه هوشمند هنگام استفاده از ReplaceContents |     باگ     |
| PSDNET-1884 | [قالب AI] رفع اشکال رندرینگ Cubic Bezier در فایل AI             |     باگ     |

## **تغییرات در API عمومی**
# **API‌های اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API‌های حذف شده:**
- هیچ‌کدام

## **مثال‌های استفاده:**

**PSDNET-1503. Handle خاصیت زاویه برای PatternFillSettings**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. پشتیبانی از مقیاس عمودی و افقی برای TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [قالب AI] پیاده‌سازی صحیح تصویر زمینه در فرمت AI مبتنی بر PDF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. استثناء "بارگذاری تصویر انجام نشد." هنگام باز کردن سند**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "PRODUCT.ai");
string outputFile1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(sourceFile1))
{
    image.Save(outputFile1, new PngOptions());
}

string sourceFile2 = Path.Combine(baseFolder, "Dolota.ai");
string outputFile2 = Path.Combine(outputFolder, "Dolota.png");

using (AiImage image = (AiImage)Image.Load(sourceFile2))
{
    image.Save(outputFile2, new PngOptions());
}

string sourceFile3 = Path.Combine(baseFolder, "ARS_novelty_2108_out_01(1).ai");
string outputFile3 = Path.Combine(outputFolder, "ARS_novelty_2108_out_01(1).png");

using (AiImage image = (AiImage)Image.Load(sourceFile3))
{
    image.Save(outputFile3, new PngOptions());
}

string sourceFile4 = Path.Combine(baseFolder, "bit_gear.ai");
string outputFile4 = Path.Combine(outputFolder, "bit_gear.png");

using (AiImage image = (AiImage)Image.Load(sourceFile4))
{
    image.Save(outputFile4, new PngOptions());
}

string sourceFile5 = Path.Combine(baseFolder, "test.ai");
string outputFile5 = Path.Combine(outputFolder, "test.png");

using (AiImage image = (AiImage)Image.Load(sourceFile5))
{
    image.Save(outputFile5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. رفع ذخیره کردن پرونده‌های psd حاوی الگوی Stroke**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "StrokeShapePattern.psd");
string outputFile = Path.Combine(outputFolder, "StrokeShapePattern_output.psd");

Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] newPattern = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    PattResource pattResource;
    foreach (var globalLayerResource in image.GlobalLayerResources)
    {
        if (globalLayerResource is PattResource)
        {
            pattResource = (PattResource)globalLayerResource;
            PattResourceData patternItem = pattResource.Patterns[0]; // Stroke internal pattern data

            patternItem.PatternId = guid.ToString();
            patternItem.Name = newPatternName;
            patternItem.SetPattern(newPattern, newPatternBounds);

            break;
        }
    }

    strokeInternalFillSettings.PatternName = newPatternName;
    strokeInternalFillSettings.PatternId = guid.ToString() + "\0";

    shapeLayer.Update();

    image.Save(outputFile);
}

// بررسی داده‌های تغییر کرده.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    Assert.AreEqual(guid.ToString().ToUpper(), strokeInternalFillSettings.PatternId);
    Assert.AreEqual(newPatternName, strokeInternalFillSettings.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. استایل متن اشتباه است در یک شیوه هوشمند هنگام استفاده از ReplaceContents**

{{< highlight csharp >}}
string inputFile = Path.Combine(baseFolder, "source.psd");
string output2 = Path.Combine(outputFolder, "output.png");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, psdLoadOptions))
{
    SmartObjectLayer smartObject = (SmartObjectLayer)psdImage.Layers[1];

    using (PsdImage smartObjectImage = (PsdImage)smartObject.LoadContents(psdLoadOptions))
    {
        smartObject.ReplaceContents(smartObjectImage);
    }

    psdImage.Save(output2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [قالب AI] رفع اشکال رندرینگ Cubic Bezier در فایل AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Typography.ai");
string outputFilePath = Path.Combine(outputFolder, "Typography.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. تغییر مکانیزم Distort در warp**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "crow_grid.psd");
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

**PSDNET-1802. افزایش سرعت warp**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "output.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var sw = new Stopwatch();
sw.Start();

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}

sw.Stop();

// old value = 193300
// new value =  55500
int timeInSec = (int)sw.Elapsed.TotalMilliseconds;
if (timeInSec > 100000)
{
    throw new Exception("زمان پردازش خیلی طولانی است");
}
{{< /highlight >}}

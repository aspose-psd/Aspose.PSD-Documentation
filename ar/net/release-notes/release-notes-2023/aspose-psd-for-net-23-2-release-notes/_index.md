---
title: أصدر Aspose.PSD for .NET 23.2 - ملاحظات الإصدار
type: docs
weight: 110
url: /ar/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**الرقم**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-1359|إعادة تشكيل تقنية النص لتحسين توضيع النص والتقديم والدعم|تحسين|
|PSDNET-1270|إضافة القدرة على معالجة تأثير التحريف من خلال واجهة برمجة التطبيقات العامة|ميزة|
|PSDNET-1391|إضافة دعم لوضعيات القيادة Bottom-to-bottom وTop-to-Top من إعدادات الفقرة|ميزة|
|PSDNET-912|تغيير الخط واللون لطبقة النص في PSD|خلل|
|PSDNET-1022|تصدير غير صحيح للنص في اختبار TextUpdateTests، النص مفقود|خلل|
|PSDNET-1221|نقص النص الصغير الزائد بعد تغيير حجم صورة PSD الكبيرة|خلل|
|PSDNET-1301|تطبيق Aspose.Psd for .NET textLayer.UpdateText() يطبع '-' (شرطة) كشرطة سفلية بشكل عشوائي لمجموعات بيانات مختلفة|خلل|
|PSDNET-1379|إعدادات الدقة لا تطبق عند التصدير من PSD إلى PDF|خلل|


## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة التطبيقات العامة:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **تمت إزالة واجهات برمجة التطبيقات العامة:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **أمثلة على الاستخدام:**

**PSDNET-912. تغيير الخط واللون لطبقة النص في PSD**

{{< highlight csharp >}}
string fontsFolder = "الخطوط";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "النتيجة.psd";
string outputPng = "النتيجة.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. تصدير غير صحيح للنص في اختبار TextUpdateTests، النص مفقود**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("تم تحديث النص");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. نقص النص الصغير الزائد بعد تغيير حجم صورة PSD الكبيرة**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "الناتج.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. إضافة القدرة على معالجة تأثير التحريف من خلال واجهة برمجة التطبيقات العامة**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. تطبيق Aspose.Psd for .NET textLayer.UpdateText() يطبع '-' (شرطة) كشرطة سفلية بشكل عشوائي لمجموعات بيانات مختلفة**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "صورة الناتج.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAME":
                    textLayer.UpdateText("السيد جاك سميث");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    textLayer.UpdateText("OFFICER-001");
                    break;
                case "BLOODGROUP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADDRESS":
                    textLayer.UpdateText("BLOCK-A, STREET-7, APPT NO - 047, SECTOR-024");
                    break;
                case "PERMADDRESS":
                    textLayer.UpdateText("HOUSE NO - 42, LANE -025, PALM GREENS VIEW HOUSING SOCIETY, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. إعدادات الدقة لا تطبق عند التصدير من PSD إلى PDF**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. إضافة دعم لوضعيات القيادة Bottom-to-bottom وTop-to-Top من إعدادات الفقرة**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "الناتج_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // تغيير قيمة LeadingType   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // تغيير قيمة LeadingType   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
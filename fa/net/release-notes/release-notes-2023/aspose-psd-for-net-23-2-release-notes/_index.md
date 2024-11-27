---
title: Aspose.PSD برای .NET 23.2 - یادداشت‌های نسخه
type: docs
weight: 110
url: /fa/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD for .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-1359|بازطراحی رندرینگ متن برای بهبود قرارگیری، رندرینگ و پشتیبانی متن|افزایش امکانات|
|PSDNET-1270|افزودن قابلیت پردازش اثر کج|ویژگی|
|PSDNET-1391|افزودن پشتیبانی از حالت‌های بالا به پایین و پایین به بالای leading از تنظیمات پاراگراف|ویژگی|
|PSDNET-912|تغییر فونت و رنگ برای لایه متنی PSD|اشکال|
|PSDNET-1022|برون‌بری اشتباه متن در تست‌های TextUpdateTests، متن از دست رفته است|اشکال|
|PSDNET-1221|متن بسیار کوچک پس از تغییر اندازه تصویر PSD بزرگ از دست می‌رود|اشکال|
|PSDNET-1301|Aspose.Psd برای .NET textLayer.UpdateText() در چیدمان تصادفی برای مجموعه‌داده‌های مختلف '-' (خط تیره) را به‌صورت زیرخط چاپ می‌کند|اشکال|
|PSDNET-1379|ResolutionSettings در برون‌بری از PSD به PDF اعمال نمی‌شود|اشکال|


## تغییرات API عمومی
# **API‌های اضافه شده:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **API‌های حذف شده:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **مثال‌های استفاده:**

**PSDNET-912. تغییر فونت و رنگ برای لایه متنی PSD**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

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

**PSDNET-1022. برون‌بری اشتباه متن در تست‌های TextUpdateTests، متن از دست رفته است**

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
            layer.UpdateText("متن به‌روز شده است");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. متن بسیار کوچک پس از تغییر اندازه تصویر PSD بزرگ از دست می‌رود**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. افزودن قابلیت پردازش اثر کج از طریق API عمومی**

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

**PSDNET-1301. Aspose.Psd برای .NET textLayer.UpdateText() در چیدمان تصادفی برای مجموعه‌داده‌های مختلف '-' (خط تیره) را به‌صورت زیرخط چاپ می‌کند**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

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
                    textLayer.UpdateText("آقای جک اسمیت");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    textLayer.UpdateText("آفسر-001");
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

**PSDNET-1379. ResolutionSettings در برون‌بری از PSD به PDF اعمال نمی‌شود**

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

**PSDNET-1391. افزودن پشتیبانی از حالت‌های بالا به پایین و پایین به بالای leading از تنظیمات پاراگراف**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // تغییر مقدار LeadingType   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // تغییر مقدار LeadingType   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

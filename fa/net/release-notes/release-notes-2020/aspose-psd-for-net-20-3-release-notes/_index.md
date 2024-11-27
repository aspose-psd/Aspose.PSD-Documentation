---
title: راه‌اندازی Aspose.PSD برای .NET 20.3 - یادداشت‌های انتشار
type: docs
weight: 100
url: /fa/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

این صفحه شامل یادداشت‌های انتشار برای [Aspose.PSD برای .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-188|پشتیبانی از .Net Core|ویژگی|
|PSDNET-523|تبدیل فایل‌های Adobe Illustrator به PDF|ویژگی|
|PSDNET-212|افزودن قابلیت رندر کردن سبک‌های مختلف در یک لایه متن|ویژگی|
|PSDNET-144|پشتیبانی از لایه تنظیمات سیاه و سفید|ویژگی|
|PSDNET-233|افزودن پشتیبانی از صدور فرمت AI (نسخه 8) به سایر فرمت‌ها|ویژگی|
|PSDNET-540|پشتیبانی از پردازش حالت مخلوط (PassThrough Blending Mode) (فقط برای گروه لایه)|ویژگی|
|PSDNET-539|استثناء: بارگذاری تصویر انجام نشد بر روی تصویری با نام‌های آلفای یونیکد خالی|خطا|
|PSDNET-541|خروجی نادرست پس از تغییر دید پذیری یک گروه لایه|خطا|
|PSDNET-516|استثناء در هنگام بارگذاری تصویر PSD: بخش رنگ (منبع سایه پراکندگی) باید شامل 3 جزئیت رنگ برای RGB یا 4 جزئیت رنگ برای CMYK باشد|خطا|
|PSDNET-536|استثناء اگر سعی بر رسم بر روی لایه ایجاد شده تازه شود اگر نسخه ساده‌ی کانستراکتور استفاده شود|خطا|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**
**PSDNET-523. تبدیل فایل‌های Adobe Illustrator به PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. افزودن قابلیت رندر کردن سبک‌های مختلف در یک لایه متن**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // ویرایش سبک متن "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // ویرایش سبک متن "2\r"

    newPortions[2].Style.FauxBold = true; // ویرایش سبک متن "Bold"

    newPortions[3].Style.FauxItalic = true; // ویرایش سبک متن "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // ویرایش سبک متن "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // ویرایش سبک متن "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. افزودن پشتیبانی از صدور فرمت AI (نسخه 8) به سایر فرمت‌ها**

{{< highlight java >}}

 // مثال صدور فایل AI به فرمت PSD و PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. پشتیبانی از پردازش حالت مخلوط (PassThrough Blending Mode) (فقط برای گروه لایه).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "There is not 23rd layer.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "The 23rd layer is not a layer group.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "The 23rd layer name is not 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup layer should have 'pass through' blend mode.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. به‌روزرسانی متن لایه متن باعث پرتاب استثناء می‌شود**

{{< highlight java >}}

 // به‌روزرسانی متن لایه باعث پرتاب استثناء می‌شود

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. ذخیره تصویر PSD پس از عملیات چرخش و فلیپ فایلی فاسد ایجاد می‌کند که باز نشده است.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// باید بدون استثنا انجام شود

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // هیچ کاری انجام نده

}

{{< /highlight >}}

**PSDNET-539. استثناء: بارگذاری تصویر انجام نشد بر روی تصویری با نام‌های آلفای یونیکد خالی**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // اینجا نباید هیچ استثنا دریافت شود

{

    // هیچ کاری انجام نده

}

{{< /highlight >}}

**PSDNET-541. خروجی نادرست پس از تغییر دید پذیری یک گروه لایه**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// تغییراتی روی نام لایه‌ها اعمال کرده و آن را ذخیره کن

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // همه چیز داخل یک گروه را خاموش کن

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. استثناء در هنگام بارگذاری تصویر PSD: بخش رنگ (منبع سایه پراکندگی) باید شامل 3 جزئیت رنگ برای RGB یا 4 جزئیت رنگ برای CMYK باشد**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // اینجا نباید هیچ استثنا دریافت شود

{

    // هیچ کاری انجام نده

}

{{< /highlight >}}

**PSDNET-536. استثناء اگر سعی بر رسم بر روی لایه ایجاد شده تازه شود اگر نسخه ساده‌ی کانستراکتور استفاده شود**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // یک مستطیل با ابزار پن رسم کن

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // مستطیل دیگری با محور پریشان در رنگ آبی رسم کن

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

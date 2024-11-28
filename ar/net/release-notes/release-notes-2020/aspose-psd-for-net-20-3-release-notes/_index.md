---
title: تحديثات اصدار Aspose.PSD لـ .NET 20.3
type: docs
weight: 100
url: /ar/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

** 

|**المفتاح**|**الملخص**|**الفئة**|
| :- | :- | :- |
|PSDNET-188|دعم .Net Core|ميزة|
|PSDNET-523|تحويل ملفات Adobe Illustrator إلى ملفات PDF|ميزة|
|PSDNET-212|إضافة القدرة على عرض أنماط مختلفة في طبقة نص واحدة|ميزة|
|PSDNET-144|دعم طبقة التكيف السوداء والبيضاء|ميزة|
|PSDNET-233|إضافة دعم تصدير تنسيق AI (الإصدار 8) إلى تنسيقات أخرى|ميزة|
|PSDNET-540|دعم معالجة طبقة التداخل بنمط العبور (يستخدم لمجموعة الطبقات فقط)|ميزة|
|PSDNET-539|استثناء: فشل تحميل الصورة عند تحميل صورة بأسماء ألفا يونيكود فارغة|خلل|
|PSDNET-541|ناتج غير صحيح بعد تغيير رؤية مجموعة الطبقات|خلل|
|PSDNET-516|استثناء عند تحميل صورة PSD: يجب أن تحتوي القسم اللوني (مورد الظل المنسدل) على 3 مكونات لون لـ RGB أو 4 مكونات لون لـ CMYK|خلل|
|PSDNET-536|استثناء في حالة محاولة الرسم على طبقة مُنشأة حديثًا إذا تم استخدام الإصدار البسيط للمنشئ|خلل|

## **تغييرات واجهة برمجة التطبيقات العامة**
# **تمت إضافة واجهات برمجة التطبيقات الجديدة:**
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
# **تمت إزالة الواجهات البرمجية التالية:**
- None

## **أمثلة الاستخدام:**
**PSDNET-523. تحويل ملفات Adobe Illustrator إلى PDFs**

{{< highlight java >}}
 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. إضافة القدرة على عرض أنماط مختلفة في طبقة نص واحدة**

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

    newPortions[0].Style.Underline = true; // تحرير نمط النص "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // تحرير نمط النص "2\r"

    newPortions[2].Style.FauxBold = true; // تحرير نمط النص "Bold"

    newPortions[3].Style.FauxItalic = true; // تحرير نمط النص "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // تحرير نمط النص "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // تحرير نمط النص "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. إضافة دعم تصدير تنسيق AI (الإصدار 8) إلى تنسيقات أخرى**

{{< highlight java >}}
 // مثال على تصدير ملف AI إلى تنسيقي PSD و PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. دعم معالجة طبقة التداخل بنمط العبور (يستخدم لمجموعة الطبقات فقط).**

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

    AssertIsTrue(image.Layers.Length >= 23, "لا توجد طبقة رقم 23.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "الطبقة رقم 23 ليست مجموعة طبقات.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "اسم الطبقة رقم 23 ليس 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "يجب أن تكون طبقة مجموعة التعديل لها وضع امتزاج 'المرور'."); 

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. تحديث نص الطبقة يثير استثناء**

{{< highlight java >}}
 // تحديث نص الطبقة يثير استثناء

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

**PSDNET-182. حفظ صورة PSD بعد عملية RotateFlip ينتج ملفًا تالفًا لا يمكن فتحه.**

{{< highlight java >}}
 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// يجب تنفيذها دون حدوث استثناءات

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // لا توجد أي عمليات

}

{{< /highlight >}}

**PSDNET-539. استثناء: فشل تحميل الصورة عند تحميل صورة بأسماء ألفا يونيكود فارغة**

{{< highlight java >}}
 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // هنا يجب عدم حدوث أي استثناءات

{

    // لا توجد أي عمليات

}

{{< /highlight >}}

**PSDNET-541. الناتج غير صحيح بعد تغيير رؤية مجموعة الطبقات**

{{< highlight java >}}
 string sourceFile = "input.psd";

string outputFile = "output.psd";

// إجراء التغييرات في أسماء الطبقات وحفظها

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // إيقاف كل شيء داخل مجموعة

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. استثناء عند تحميل صورة PSD: يجب أن تحتوي القسم اللوني (مورد الظل المنسدل) على 3 مكونات لون لـ RGB أو 4 مكونات لون لـ CMYK**

{{< highlight java >}}
 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // هنا يجب عدم حدوث أي استثناءات

{

    // لا توجد أي عمليات

}

{{< /highlight >}}

**PSDNET-536. استثناء إذا تم محاولة الرسم على طبق
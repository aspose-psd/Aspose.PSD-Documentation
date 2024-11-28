---
title: فرار یاداشت‌ها برای Aspose.PSD برای .NET 23.7
type: docs
weight: 60
url: /fa/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [Aspose.PSD برای .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **کلید**    | **خلاصه**                                                                                                   | **دسته‌بندی** |
|:----------|:------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802 | افزودن قابلیت صادر کردن هر لایه از پرونده PSD به پرونده GIF متحرک                                    | ویژگی |
| PSDNET-1441 | نسبت دادن ویژگی پراکنش لایه شکل از منبع vscg                                                         | ویژگی |
| PSDNET-1534 | افزودن انواع جدیدی از انحنای (دایره و خم)                                                           | ویژگی |
| PSDNET-1543 | تغییر برنامه‌ای که پرونده PSD را ذخیره می‌کند به Aspose.PSD اگر ویژگی UpdateMetadata بر روی صحیح تنظیم شود | ویژگی |
| PSDNET-1567 | افزایش منطقه محاسباتی تصویر انحنا                                                               | ویژگی |
| PSDNET-1471 | لایه تنظیم سیاه و سفید فرآینده‌های نیمه‌شفافیت را اشتباه پردازش می‌کند                           | باگ     |
| PSDNET-1505 | جایگزینی SmartObjectContents (وقتی گزینه AllowWarpRepaint فعال است) پس از 2 دقیقه محاسبه متوقف می‌شود | باگ     |
| PSDNET-1585 | افزودن قابلیت به‌دست آوردن موضع حقیقی چپ و بالای لایه‌های گروه                                    | باگ     |
| PSDNET-1589 | تغییر اندازه لایه زمانی اشتباه کار می‌کند هنگامی که پرونده psd دارای VogkResource با ساختارها در نقاط است | باگ     |
| PSDNET-1608 | TextBound به عنوان انتظار کار نمی‌کند                                                         | باگ     |
| PSDNET-1612 | اضافه کردن لایه‌ای که با سازنده پیش فرض ایجاد شده به تصویر PSD منجر به اضافه شدن منابع پیش‌فرض به آن نمی‌شود | باگ     |
| PSDNET-1623 | تعداد LoopesCount در Timeline بی‌توجه است هنگام صادر کردن به GIF متحرک                                 | باگ     |


## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **API‌های حذف شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **نمونه‌های استفاده:**

**PSDNET-802. افزودن قابلیت صادر کردن هر لایه از پرونده PSD به پرونده GIF متحرک**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // ساخت فریم‌ها برای هر لایه.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // بروزرسانی حالت‌های فعلی
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. نسبت دادن ویژگی پراکنش لایه شکل از منبع vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// بررسی تغییرات ذخیره‌شده
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}
{{< /highlight >}}

**PSDNET-1471. لایه تنظیم سیاه و سفید فرآینده‌های نیمه‌شفافیت را اشتباه پردازش می‌کند**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// بررسی تغییرات ذخیره‌شده
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("لایه 2 باید BlackWhiteAdjustmentLayer باشد");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}
{{< /highlight >}}

**PSDNET-1505. جایگزینی SmartObjectContents (وقتی گزینه AllowWarpRepaint فعال است) پس از 2 دقیقه محاسبه متوقف می‌شود**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. افزودن انواع جدیدی از انحنای (دایره و خم)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. تغییر برنامه‌ای که پرونده PSD را ذخیره می‌کند به Aspose.PSD اگر ویژگی UpdateMetadata بر روی صحیح تنظیم شود**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // اگر می‌خواهید ابزار ایجاد کننده تغییر کند، اطمینان حاصل کنید که ویژگی "UpdateMetadata" بر روی true قرار داشته باشد. بر روی صحیح تنظیم شده است به طور پیش‌فرض.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // ذخیره تصویر. 
    image.Save(path, psdOptions);

    // بررسی ابزار ایجاد کننده در کد.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // اینجا اطلاعات ابزار ایجاد کننده به‌روز می‌شوند.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. افزایش منطقه محاسباتی تصویر انحنا**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. افزودن قابلیت به‌دست آوردن موضع حقیقی چپ و بالای لایه‌های گروه**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("اشیاء برابر نیستند.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // گرفتن گروه لایه.
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // محاسبه مواضع چپ، بالا، راست و پایین واقعی.
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // مواضع چپ، بالا، راست و پایین گروه لایه به درستی محاسبه می‌شوند.
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. اندازه‌گیری لایه کار نمی‌کند هنگامی که پرونده psd دارای VogkResource با ساختارها در نقاط است**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "اشیاء برابر نیستند.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound به عنوان انتظار کار نمی‌کند**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //مرحله: جایگزینی متن
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Text test replaced";

    //مرحله: بروزرسانی TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math
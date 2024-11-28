---
title: ملاحظات الإصدار Aspose.PSD لـ .NET 23.7
type: docs
weight: 60
url: /ar/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD لـ .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **الرقم**     | **الملخص**                                                                                                  | **الفئة** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | إضافة القدرة على تصدير كل طبقة من ملف PSD إلى ملف Animated Gif                                        | ميزة |
| PSDNET-1441 | تعيين خصائص الاملأ لطبقة الشكل من مصدر vscg                                                       | ميزة |
| PSDNET-1534 | إضافة أنواع جديدة من التواء (arc و arch)                                                                           | ميزة |
| PSDNET-1543 | تغيير التطبيق الذي يحفظ ملف PSD إلى Aspose.PSD إذا تم تعيين خاصية UpdateMetadata على true      | ميزة|
| PSDNET-1567 | زيادة منطقة الحساب لصورة التواء                                                              | ميزة |
| PSDNET-1471 | طبقة التعديل السوداء والبيضاء تعالج الشفافية النصفية بشكل خاطئ                                           | علة     |
| PSDNET-1505 | فشل SmartObject ReplaceContents (عندما تكون خيارات AllowWarpRepaint نشطة) بعد 2 دقيقة من الحساب   | علة     |
| PSDNET-1585 | إضافة القدرة على الحصول على موضع طبقة LayerGroup الحقيقي الأيسر والأعلى                                                | علة     |
| PSDNET-1589 | Resize of the layer works wrong when psd file has VogkResource with structures in points                     | علة     |
| PSDNET-1608 | TextBound is not working as expected                                                                         | علة     |
| PSDNET-1612 | Adding a layer created with default constructor to PSD image does not add default resources to it            | علة     |
| PSDNET-1623 | تتجاهل Timeline.LoopesCount عند التصدير إلى صورة GIF متحركة                                               | علة     |


## **تعديلات واجهات برمجة التطبيقات العامة**
# **الواجهات الجديدة:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **الواجهات المحذوفة:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **أمثلة الاستخدام:**

**PSDNET-802. إضافة القدرة على تصدير كل طبقة من ملف PSD إلى ملف Animated Gif**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // إنشاء إطارات لكل طبقة.
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

    // تحديث التعاليم الحالية
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

**PSDNET-1441. تعيين خصائص الاملأ لطبقة الشكل من مصدر vscg**

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

// تحقق من التغييرات التي تم حفظها
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
        throw new Exception(message ?? "الكائنان غير متساويان.");
    }
}
{{< /highlight >}}

**PSDNET-1471. تعامل طبقة التعديل السوداء والبيضاء مع الشفافية النصفية بشكل خاطئ**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// تحقق من التغييرات التي تم حفظها
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("الطبقة 2 ينبغي أن تكون BlackWhiteAdjustmentLayer");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "الكائنان غير متساويان.");
    }
}
{{< /highlight >}}

**PSDNET-1505. فشل SmartObject ReplaceContents (عندما تكون خيارات AllowWarpRepaint نشطة) بعد 2 دقيقة من الحساب**

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

**PSDNET-1534. إضافة أنواع جديدة من التواء (arc و arch)**

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

**PSDNET-1543. تغيير التطبيق الذي يحفظ ملف PSD إلى Aspose.PSD إذا تم تعيين خاصية UpdateMetadata على true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // إذا كنت تريد تغيير أداة الإنشاء، تأكد من تعيين الخاصية "UpdateMetadata" على true. إنها معينة على true افتراضيًا.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // حفظ الصورة.
    image.Save(path, psdOptions);

    // التحقق من أداة الإنشاء في الرمز.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // سيتم تحديث معلومات أداة الإنشاء هنا.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. زيادة منطقة الحساب لصورة التواء**

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

**PSDNET-1585. إضافة القدرة على الحصول على الموضع الأيسر والأعلى الحقيقي لطبقة LayerGroup**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("الكائنان غير متساويان.");
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
            // الحصول على الطبقة الجماعية.
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // حساب الموضع الأيسر والأعلى والأيمن والسفلي الحقيقيين.
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

            // تم حساب مواقع LayerGroup اليسرى والعلوية واليمنى والسفلية بشكل صحيح الآن.
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. يعمل تغيير حجم الطبقة بشكل خاطئ عندما يحتوي ملف psd على VogkResource بنيات في النقاط**

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
        throw new Exception(message ?? "الكائنان غير متساويان.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound لا يعمل كما هو متوقع**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //الخطوة: استبدل النص
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Text test replaced";

    //الخطوة: تحديث بيانات الطبقة النصية
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// التحقق من التغييرات
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // مجموعة خاصة للعث
    ال 

{{< /highlight >}}}
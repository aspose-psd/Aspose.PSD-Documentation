---
title: اصلاحات Aspose.PSD برای .NET 23.1 - یادداشت های انتشار
type: docs
weight: 120
url: /fa/net/aspose-psd-for-net-23-1-release-notes/
---

{{% alert color="primary" %}}

این صفحه حاوی یادداشت های انتشار برای [Aspose.PSD برای .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-401|پشتیبانی از vstkResource|ویژگی|
|PSDNET-1346|افزودن مشخصه قابل ویرایش BaselineDirection/IsStandardVerticalRomanAlignmentEnabled به رابط IText|ویژگی|
|PSDNET-181|تبدیل PSD به JPEG به درستی انجام نمی‌شود|باگ|
|PSDNET-958|شکست PSB به PDF برای فایل‌های بزرگ|باگ|
|PSDNET-1171|افزودن پردازش ماسک برش به لایه تنظیم|باگ|
|PSDNET-1252|بعد از تغییر اندازه تصویر کل و سپس پس از تغییر اندازه لایه خاص، Aspose.PSD استثنا را در زمان ذخیره لایه اندازه دهی می‌کند|باگ|


## **تغییرات API عمومی**
# **API های اضافه شده:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **API های حذف شده:**
- هیچکدام


## **مثال های استفاده:**

**PSDNET-181. تبدیل PSD به JPEG به درستی انجام نمی‌شود**

{{< highlight csharp >}}
string srcFile = "helicopter.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. پشتیبانی از vstkResource**

{{< highlight csharp >}}
string srcFile = "StrokeShapeTest1.psd";
string dstFile = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource vstkResource = (VstkResource)resource;
            vstkResource.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkResource.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

**PSDNET-958. شکست PSB به PDF برای فایل‌های بزرگ**

{{< highlight csharp >}}
string inputPath = "SteveKohli-CarTOP.psb";
string outputPath ="output.pdf";

using (var image = Image.Load(inputPath))
{
    image.Save(outputPath, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. افزودن پردازش ماسک برش به لایه تنظیم**

{{< highlight csharp >}}
string srcFile = "helicopter_part.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. بعد از تغییر اندازه تصویر کل و سپس پس از تغییر اندازه لایه خاص، Aspose.PSD استثنا را در زمان ذخیره لایه اندازه دهی می‌کند**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string imgFile1 = "img1.png";
string imgFile2 = "img2.png";

var loadOptions = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // First we resize whole image
    image.Resize(110, 90);
    var layers = image.Layers;

    var layerOk = layers[0];
    layerOk.Resize(100, 80);

    var layerException = layers[1];
    layerException.Resize(100, 80);

    // Here all will be fine
    layerOk.Save(imgFile1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // Now Here all will be fine
    layerException.Save(imgFile2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. افزودن مشخصه قابل ویرایش BaselineDirection/IsStandardVerticalRomanAlignmentEnabled به رابط IText**

{{< highlight csharp >}}
// کد زیر قابلیت ویرایش مشخصه جدید IsStandardVerticalRomanAlignmentEnabled را نشان می‌دهد.
// این تاثیری بر روی رندرینگ در حال حاضر ندارد، اما تنها به شما اجازه می‌دهد که مقدار مشخصه را ویرایش کنید.

string src = "1346test.psd";
string output = "out_1346test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // خواندن صحیح
    }
    else
    {
        throw new Exception("خواندن نادرست از مقدار مشخصه IsStandardVerticalRomanAlignmentEnabled");
    }

    textPortion.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (!textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // خواندن صحیح
    }
    else
    {
        throw new Exception("خواندن نادرست از مقدار مشخصه IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}} 

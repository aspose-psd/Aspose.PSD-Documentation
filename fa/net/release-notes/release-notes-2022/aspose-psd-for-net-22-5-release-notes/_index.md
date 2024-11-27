---
title: اسپوز.PSD برای .NET 22.5 - یادداشت‌های نسخه
type: docs
weight: 80
url: /fa/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت‌های نسخه برای [اسپوز.PSD برای .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد

{{% /alert %}}

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-952|افزودن خاصیت EffectType به رابط ILayerEffect|ویژگی|
|PSDNET-1146|بازسازی کلاس ChannelData|بهبود|
|PSDNET-657|اصلاح خاصیت opacity برای DropShadowEffect|اشکال|
|PSDNET-825|نقاشی نادرست لایه تنظیم از طریق لایه شفاف در یک حالت خاص|اشکال|
|PSDNET-1168|بهبود متد Colorize. رنگ‌آمیزی خاکستری + تنظیم رنگ صحیح زمانی که اشباع 100 نیست|اشکال|
|مقاله|[چگونگی اجرای اسپوز.PSD در Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|مستندات|


## **تغییرات عمومی API**

# **APIهای اضافه شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EffectType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.BevelEmboss


# **APIهای حذف شده:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **نمونه‌های استفاده:**

**PSDNET-657. اعمال کارایی خاصیت opacity برای DropShadowEffect**

{{< highlight csharp >}}
string inputFile = "input.psd";
string outputImage20 = "outputImage20.png";
string outputImage200 = "outputImage200.png";

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    Layer workLayer = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // مثال با Opacity = 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(outputImage20, new PngOptions());

    // مثال با Opacity = 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(outputImage200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. نقاشی نادرست لایه تنظیم از طریق لایه شفاف در یک حالت خاص**

{{< highlight csharp >}}
string sourceFile = "input_825.psd";
string outputPng = "out_psdnet825.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    foreach (var item in psdImage.Layers)
    {
        item.IsVisible = false;
    }
    var layer = psdImage.Layers[3];
    psdImage.Layers[1].IsVisible = true;
    psdImage.Layers[3].IsVisible = true;
    psdImage.Layers[4].IsVisible = true;
    psdImage.Layers[7].IsVisible = true;

    var width = layer.Width;
    var height = layer.Height;
    var layerBounds = new Rectangle(layer.Left, layer.Top, width, height);
    var bounds = new Rectangle(0, 0, width, height);
    var image = new PsdImage(bounds.Width, bounds.Height);

    image.SaveArgb32Pixels(bounds, psdImage.LoadArgb32Pixels(layerBounds));

    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. افزودن خاصیت EffectType به رابط ILayerEffect**

{{< highlight csharp >}}
string inputFile = "input.psd";
string outputWithout = "outputWithout.png";
string outputWith = "outputWith.png";

using (PsdImage psdImage = (PsdImage)Image.Load(inputFile, new LoadOptions()))
{
    psdImage.Save(outputWithout, new PngOptions());

    Layer workLayer = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = workLayer.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffect in workLayer.BlendingOptions.Effects)
    {
        if (iEffect.EffectType == LayerEffectsTypes.DropShadow)
        {
            // گرفته شد
            psdImage.Save(outputWith, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. بهبود متد Colorize. رنگ‌آمیزی خاکستری + تنظیم رنگ صحیح زمانی که اشباع 100 نیست**

{{< highlight csharp >}}
string srcFile = "Colorize.psd";            
string outputSimple = "output_simple.png";
string outputColorize = "output_colorize.png";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    // تصویر بدون خاصیت Colorize
    psdImage.Save(outputSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // تنظیم خاصیت Colorize
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)layer;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // تصویر با خاصیت Colorize
    psdImage.Save(outputColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

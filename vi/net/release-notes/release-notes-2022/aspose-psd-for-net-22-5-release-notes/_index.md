---
title: Aspose.PSD cho .NET 22.5 - Ghi chú phát hành
type: docs
weight: 80
url: /vi/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Thể loại**|
| :- | :- | :- |
|PSDNET-952|Thêm thuộc tính EffectType vào Giao diện ILayerEffect|Tính năng|
|PSDNET-1146|Tối ưu hóa lớp ChannelData|Nâng cấp|
|PSDNET-657|Làm cho thuộc tính độ mờ hoạt động cho DropShadowEffect|Lỗi|
|PSDNET-825|Vẽ không chính xác lớp điều chỉnh qua lớp trong suốt trong một trường hợp cụ thể|Lỗi|
|PSDNET-1168|Cải thiện phương thức Colorize. Màu xám + đặt màu chính xác khi độ bão hòa không phải 100|Lỗi|
|Bài viết|[Cách chạy Aspose.PSD trong Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Tài liệu|


## **Thay đổi API công khai**
# **API đã thêm:**
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


# **API đã loại bỏ:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Ví dụ sử dụng:**

**PSDNET-657. Làm cho thuộc tính độ mờ hoạt động cho DropShadowEffect**

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

    // Ví dụ với Độ mờ = 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(outputImage20, new PngOptions());

    // Ví dụ với Độ mờ = 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(outputImage200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Vẽ không chính xác lớp điều chỉnh qua lớp trong suốt trong một trường hợp cụ thể**

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

**PSDNET-952. Thêm thuộc tính EffectType vào Giao diện ILayerEffect**

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
            // Nó đã bắt được
            psdImage.Save(outputWith, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Cải thiện phương thức Colorize. Màu xám + đặt màu chính xác khi độ bão hòa không phải 100**

{{< highlight csharp >}}
string srcFile = "Colorize.psd";            
string outputSimple = "output_simple.png";
string outputColorize = "output_colorize.png";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    // Hình ảnh không có thuộc tính Colorize
    psdImage.Save(outputSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Đặt thuộc tính Colorize
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)layer;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Hình ảnh có thuộc tính Colorize
    psdImage.Save(outputColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

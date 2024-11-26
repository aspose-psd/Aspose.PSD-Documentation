---
title: Aspose.PSD для .NET 22.5 - Примечания к выпуску
type: docs
weight: 80
url: /ru/net/aspose-psd-for-net-22-5-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-952|Добавление свойства EffectType в интерфейс ILayerEffect|Функция|
|PSDNET-1146|Рефакторинг класса ChannelData|Улучшение|
|PSDNET-657|Сделать работу свойства непрозрачности для DropShadowEffect|Ошибка|
|PSDNET-825|Неверное отображение слоя коррекции через прозрачный слой в конкретном случае|Ошибка|
|PSDNET-1168|Улучшение метода Colorize. Цветовое оттенение серого + установка правильного цвета, когда насыщенность не равна 100|Ошибка|
|Статья|[Как запустить Aspose.PSD в Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Документация|


## **Изменения в публичном API**
# **Добавленные API:**
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


# **Удаленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Примеры использования:**

**PSDNET-657. Сделать работу свойства непрозрачности для DropShadowEffect**

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

    // Пример с непрозрачностью = 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(outputImage20, new PngOptions());

    // Пример с непрозрачностью = 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(outputImage200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Неверное отображение слоя коррекции через прозрачный слой в конкретном случае**

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

**PSDNET-952. Добавление свойства EffectType в интерфейс ILayerEffect**

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
            // это поймано
            psdImage.Save(outputWith, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Улучшение метода Colorize. Цветовое оттенение серого + установка правильного цвета, когда насыщенность не равна 100**

{{< highlight csharp >}}
string srcFile = "Colorize.psd";            
string outputSimple = "output_simple.png";
string outputColorize = "output_colorize.png";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    // Изображение без свойства Colorize
    psdImage.Save(outputSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Установка свойства Colorize
    foreach (Layer layer in psdImage.Layers)
    {
        if (layer is HueSaturationLayer)
        {
            HueSaturationLayer hueSaturationLayer = (HueSaturationLayer)layer;
            hueSaturationLayer.Colorize = true;
            break;
        }
    }
    
    // Изображение со свойством Colorize
    psdImage.Save(outputColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

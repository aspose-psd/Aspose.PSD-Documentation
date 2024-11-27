---
title: Aspose.PSD за .NET 22.2 - Бележки за изданието
type: docs
weight: 110
url: /bg/net/aspose-psd-for-net-22-2-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 22.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1032|Добавяне на поддръжка на .Net 6|Подобрение|
|PSDNET-142|Поддръжка на слоеве за настройка на наситеност|Функционалност|
|PSDNET-396|Поддръжка на vibAResource|Функционалност|
|PSDNET-1057|Създаване на пример за добавяне на персонализирани интелигентни филтри, които не се поддържат в Aspose.PSD|Функционалност|
|PSDNET-642|Изключени равнинни маски на слоевете не се визуализират правилно|Проблем|
|PSDNET-644|Изключение при преоразмеряване на PSD файлове с 16 бита на канал и равнинна маска|Проблем|


## **Промени в публичния API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddVibranceAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer.Vibrance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.VibranceLayer.Saturation
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Vibrance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Saturation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VibAResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.SourceDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.BlendMode
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.Apply(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.ApplyToMask(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.OnLoad
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilter.Clone
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.UnknownSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.Rendering.ISmartFilterRenderer
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.Rendering.ISmartFilterRenderer.Render(Aspose.PSD.PixelsData)
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.IsValidAtPosition
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.IsMaskEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.IsMaskLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.IsMaskExtendWithWhite
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SmartFilters.UpdateResourceValues
- T:Aspose.PSD.PixelsData
- M:Aspose.PSD.PixelsData.#ctor
- M:Aspose.PSD.PixelsData.#ctor(System.Int32[],Aspose.PSD.Rectangle)
- P:Aspose.PSD.PixelsData.Bounds
- P:Aspose.PSD.PixelsData.Pixels


# **Премахнати API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distribution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.AmountNoise
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.IsMonochromatic
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Radius
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Uniform
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussian
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.BlendMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Apply(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.ApplyToMask(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.OnLoad
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Clone
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.sourceDescriptor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsValidAtPosition
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskExtendWithWhite
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.UpdateResourceValues


## **Примери за използване:**

**PSDNET-142. Поддръжка на слоеве за настройка на наситеност**

{{< highlight csharp >}}
string sourceFileName = "WithoutVibrance.psd";
string outputFileNamePsd = "out_VibranceLayer.psd";
string outputFileNamePng = "out_VibranceLayer.png";

using (PsdImage image = (PsdImage) Image.Load(sourceFileName))
{
    // Създаване на нов VibranceLayer
    VibranceLayer vibranceLayer = image.AddVibranceAdjustmentLayer();
    vibranceLayer.Vibrance = 50;
    vibranceLayer.Saturation = 100;

    image.Save(outputFileNamePsd);
    image.Save(outputFileNamePng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-396. Поддръжка на vibAResource**

{{< highlight csharp >}}
// Пример на поддръжка на четене и писане на Ресурс за вибрация по време на изпълнение.
string sourceFileName = "VibranceResource.psd";
string outputFileName = "out_VibranceResource.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        foreach (var resource in layer.Resources)
        {
            if (resource is VibAResource)
            {
                var vibranceResource = (VibAResource)resource;

                int vibranceValue =  vibranceResource.Vibrance;
                int saturationValue = vibranceResource.Saturation;

                vibranceResource.Vibrance = vibranceValue * 2;
                vibranceResource.Saturation = saturationValue * 2;

                break;
            }
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-642. Изключените равнинни маски на слоевете не се визуализират правилно**

{{< highlight csharp >}}
// Пример на изключена равнинна маска на слоя по време на изпълнение.
string sourceFileName = @"RasterMaskDisabled.psd";

string outputMaskOffFileName = @"mask_off.png";
string outputMaskOnFileName  =  "mask_on.png";

using (var im = (PsdImage)Image.Load(sourceFileName))
{
    im.Save(outputMaskOffFileName, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    im.Layers[0].LayerMaskData.Flags = (im.Layers[0].LayerMaskData.Flags & LayerMaskFlags.None);

    im.Save(outputMaskOnFileName, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-644. Изключение при преоразмеряване на PSD файлове с 16 бита на канал и равнинна маска**

{{< highlight csharp >}}
string sourceFile = "GrayscaleWithMask50x30.psd";
string outputPsd = "output_psdnet644.psd";
string outputPng = "output_psdnet644.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Resize(25, 15);

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() {ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}

**PSDNET-1057. Създаване на пример за добавяне на персонализирани интелигентни филтри, които не се поддържат в Aspose.PSD**

{{< highlight csharp >}}
public void CustomSmartFilterExample(string sourceFile = "psdnet1057.psd", string outputPsd = "out_psdnet1057.psd", string outputPng = "out_psdnet1057.png")
{
    // Инициализира неподдържания 'Crystallize' интелигентен филтър във входния масив
    SmartFilter[] InitUnknownSmartFilters(SmartFilter[] smartFilters)
    {
        // ID на 'Crystallize' интелигентния филтър.
        int id =  1131574132;
    
        for (int i = 0; i < smartFilters.Length; i++)
        {
            var smartFilter = smartFilters[i];
            if (smartFilter is UnknownSmartFilter && smartFilter.FilterId == id)
            {
                var customSmartFilterInstance = new CustomSmartFilterWithRenderer();
                customSmartFilterInstance.SourceDescriptor.Structures = smartFilter.SourceDescriptor.Structures;
                smartFilters[i] = customSmartFilterInstance;
            }
        }
    
        return smartFilters;
    }

    using (var image = (PsdImage)Image.Load(sourceFile))
    {
        SmartObjectLayer smartLayer = (SmartObjectLayer)image.Layers[1];
        Layer maskLayer = image.Layers[2];
        Layer regularLayer = image.Layers[3]

smartLayer.SmartFilters.Filters = InitUnknownSmartFilters(smartLayer.SmartFilters.Filters);
        var smartFilter = smartLayer.SmartFilters.Filters[0];

        // Apply filter to SmartObject
        smartLayer.UpdateModifiedContent();
        smartLayer.SmartFilters.UpdateResourceValues();

        // Apply filter to layer mask
        smartFilter.ApplyToMask(maskLayer);

        // Apply filter to layer
        smartFilter.Apply(regularLayer);

        image.Save(outputPsd);
        image.Save(outputPng, new PngOptions());
    }
}

public sealed class CustomSmartFilterWithRenderer : SmartFilter, ISmartFilterRenderer
{
    public override string Name
    {
        get { return "Потребителски 'Crystallize' интелигентен филтър\0"; }
    }

    public override int FilterId
    {
        // ID на 'Crystallize' интелигентния филтър.
        get { return 1131574132; }
    }

    public PixelsData Render(PixelsData pixelsData)
    {
        // Извлечението на структурата на филтъра
        var filterDescriptor = (DescriptorStructure)this.SourceDescriptor.Structures[6];
        // Извличане на стойността на размера на Crystallize
        var valueStructure = (IntegerStructure)filterDescriptor.Structures[0];

        for (int i = 0; i < pixelsData.Pixels.Length; i++)
        {
            if (i % valueStructure.Value == 0)
            {
                pixelsData.Pixels[i] = 0;
            }
        }

        return pixelsData;
    }
}
{{< /highlight >}}
---
title: Using Adjustment Layer for PSD Enhancements
weight: 100
type: docs
description: Examples of using adjustment layers via Aspose.PSD for C#
keywords: [adjustment layer, photo enhance, curves adjustment, levels enhancement, invert, photo filter, psd api, C#, csharp, code sample]
url: net/adjustment-layer-enhancement/
---

## Overview

In this article, we will explore the editing of adjustment layers in Aspose.PSD for C#. Adjustment layers are a powerful feature in image editing that allow you to make non-destructive changes to your images. Aspose.PSD provides a comprehensive set of adjustment layer classes that you can use to modify various aspects of your images.

To demonstrate the editing of adjustment layers, we will use a sample code snippet at the end of the page that loads a PSD image and applies different adjustments to its layers.

In the code snippet below, we start by loading the PSD image using the `PsdImage.Load()` method. We then set up the options for saving the output PNG files. The `PngOptions` class allows us to specify the color type for the output image.

Next, we iterate through each layer in the PSD image and check its type using the `IsAssignable()` method. If the layer is of a specific type, we cast it to that type using the `Cast()` method and apply the desired adjustment. For example, we adjust the brightness and contrast of a `BrightnessContrastLayer`, modify the levels of a `LevelsLayer`, add a curve point to a `CurvesLayer`, and so on.

You can add additional code to apply other adjustments to their respective layers. Aspose.PSD provides a wide range of adjustment layer classes, such as [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), and more.

Finally, we save the modified image using the `Save()` method of the `PsdImage` class.

This code provides a basic overview of how to edit adjustment layers in Aspose.PSD for C#. You can customize the adjustments according to your requirements and explore the various options available in the API documentation.

## Example

Here’s a code sample demonstrating how to use adjustment layers using Aspose.PSD for C#:

```csharp
using Aspose.PSD;
using Aspose.PSD.FileFormats.Png;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers;
using Aspose.PSD.FileFormats.Psd.Layers.LayerResources;
using Aspose.PSD.ImageOptions;

class Program
{
    static void Main()
    {
        string sourcePsd = "AllAdjustments.psd";
        string outputOrigPng = "AllAdjustments_orig.png";
        string outputModPng = "AllAdjustments_mod.png";
        PngOptions pngOpt = new PngOptions();
        pngOpt.ColorType = PngColorType.TruecolorWithAlpha;
        
        using (PsdImage psdImage = (PsdImage)Image.Load(sourcePsd))
        {
            psdImage.Save(outputOrigPng, pngOpt);
            var layers = psdImage.Layers;
        
            foreach (var layer in layers)
            {
                if (layer is BrightnessContrastLayer br)
                {
                    br.Brightness = -br.Brightness;
                    br.Contrast = -br.Contrast;
                }
        
                if (layer is LevelsLayer levels)
                {
                    levels.MasterChannel.OutputShadowLevel = 30;
                    levels.MasterChannel.InputShadowLevel = 5;
                    levels.MasterChannel.InputMidtoneLevel = 2;
                    levels.MasterChannel.OutputHighlightLevel = 213;
                    levels.MasterChannel.InputHighlightLevel = 120;
                }
        
                if (layer is CurvesLayer curves)
                {
                    var manager = curves.GetCurvesManager();
                    var curveManager = (CurvesContinuousManager)manager;
                    curveManager.AddCurvePoint(2, 150, 180);
                }
        
                if (layer is ExposureLayer exp)
                {
                    exp.Exposure += 0.1f;
                }
        
                if (layer is HueSaturationLayer hue)
                {
                    hue.Hue = -15;
                    hue.Saturation = 30;
                }
        
                if (layer is ColorBalanceAdjustmentLayer colorBal)
                {
                    colorBal.MidtonesCyanRedBalance = 30;
                }
        
                if (layer is BlackWhiteAdjustmentLayer bw)
                {
                    bw.Reds = 30;
                    bw.Greens = 25;
                    bw.Blues = 40;
                }
        
                if (layer is PhotoFilterLayer photoFilter)
                {
                    photoFilter.Color = Color.Azure;
                }
        
                if (layer is ChannelMixerLayer channelMixer)
                {
                    var channel = channelMixer.GetChannelByIndex(0);
                    if (channel is RgbMixerChannel rgbChannel)
                    {
                        rgbChannel.Green = 120;
                        rgbChannel.Red = 50;
                        rgbChannel.Blue = 70;
                        rgbChannel.Constant += 10;
                    }
                }
        
                if (layer is InvertAdjustmentLayer)
                {
                    // No actions needed for InvertAdjustmentLayer
                }
        
                if (layer is PosterizeLayer post)
                {
                    post.Levels = 3;
                }
        
                if (layer is ThresholdLayer threshold)
                {
                    threshold.Level = 15;
                }
        
                if (layer is SelectiveColorLayer selectiveColor)
                {
                    var correction = new CmykCorrection
                    {
                        Cyan = 25,
                        Magenta = 10,
                        Yellow = -15,
                        Black = 5
                    };
                    selectiveColor.SetCmykCorrection(SelectiveColorsTypes.Cyans, correction);
                }
            }
        
            psdImage.Save(outputModPng, pngOpt);
        }
    }
}
```

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).


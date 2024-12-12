---
title: Aspose.PSD for Python via .NET 24.11 - Release Notes
type: docs
weight: 10
url: /python-net/aspose-psd-for-python-via-net-24-11-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.11](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**       | **Summary**                                                            | **Category** |
|:--------------|:-----------------------------------------------------------------------|:-------------|
| PSDPYTHON-116 | Implement correct change of FillSettings object                        | Feature      |
| PSDPYTHON-120 | Add support of Artboard layer                                          | Feature      |
| PSDPYTHON-117 | No support of UnitTypes.Millimeters for vector origin bounds           | Bug          |
| PSDPYTHON-118 | [Ai format] Handle the situation when Ai file has no layers (OCG)      | Bug          |
| PSDPYTHON-119 | Rework updating of FillSettings of FillLayer                           | Bug          |

## **Public API Changes**

# **Added APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtBResource.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtBResource.ArtboardBackgroundType
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.BackgroundColor
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Left
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Top
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Right
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Bottom
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.ArtboardLayer.Height

# **Removed APIs:**
- None

## **Usage examples:**

**PSDPYTHON-116. Implement correct change of FillSettings object**
{{< highlight python >}}
        inputFile = "FillLayer_GradientNoise.psd"
        outputFile = "output_FillLayer_GradientNoise.psd"

        with PsdImage.load(inputFile) as img:
            image = cast(PsdImage, img)
            fill_layer = cast(FillLayer, image.layers[1])  # Assuming index of the fill layer is 1

            src_fill_settings = cast(NoiseGradientFillSettings, fill_layer.fill_settings)
            assert src_fill_settings is not None

            new_fill_settings = ColorFillSettings()
            new_fill_settings.color = Color.red

            fill_layer.fill_settings = new_fill_settings
            fill_layer.update()
            image.save(outputFile)

        # Check changed fill settings
        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            fill_layer = cast(FillLayer, image.layers[1])
            dst_fill_settings = as_of(fill_layer.fill_settings, ColorFillSettings)
            assert dst_fill_settings is not None

            # Check that Gradient resource GdFlResource is removed from Resources array of a layer
            assert check_resource_is_removed(fill_layer.resources, GdFlResource)

    def check_resource_is_removed(resources, resource_type_to_remove):
        for resource in resources:
            if isinstance(resource, resource_type_to_remove):
                return False
        return True

    def assert_are_equal(expected, actual, message=None):
        if not expected == actual:
            raise Exception(message or "Objects are not equal.")

    def assert_is_not_null(actual):
        if actual is None:
            raise Exception("Layer is null.")
{{< /highlight >}}

**PSDPYTHON-120. Add support of Artboard layer**
{{< highlight python >}}
        srcFile = "artboard1.psd"

        output = [None] * 4
        references = [None] * 4
        for i in range(0, 4, 1):
            output[i] = "art" + str(i) + ".png"
            references[i] = "art" + str(i) + ".png"

        with PsdImage.load(srcFile) as image:
            psdImage = cast(PsdImage, image)
            art1 = psdImage.layers[4]
            art2 = psdImage.layers[9]
            art3 = psdImage.layers[14]

            pngSaveOptions = PngOptions()
            pngSaveOptions.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
            art1.save(output[1], pngSaveOptions)
            art2.save(output[2], pngSaveOptions)
            art3.save(output[3], pngSaveOptions)

            psdImage.save(output[0], pngSaveOptions)
{{< /highlight >}}

**PSDPYTHON-117. No support of UnitTypes.Millimeters for vector origin bounds**
{{< highlight python >}}
        sourceFile = "30x20.psd"

        with PsdImage.load(sourceFile):
            # Should be no exception
            pass
{{< /highlight >}}

**PSDPYTHON-118. [Ai format] Handle the situation when Ai file has no layers (OCG)**
{{< highlight python >}}
        inputFile = "NoLayers.ai"
        outputFilePng = "output_NoLayers.png"

        with AiImage.load(inputFile) as image:
            image.save(outputFilePng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-119. Rework updating of FillSettings of FillLayer**
{{< highlight python >}}
        inputFile = "FillLayer_UpdateColorFillSettings.psd"

        with PsdImage.load(inputFile) as img:
            image = cast(PsdImage, img)
            fill_layer = cast(FillLayer, image.layers[1])

            before_fill_settings = cast(ColorFillSettings, fill_layer.fill_settings)
            assert Color.from_argb(255, 0, 101, 207), before_fill_settings.color

            soCoResource = cast(SoCoResource, fill_layer.resources[0])
            soCoResource.color = Color.green

            # Emulate change of Resource collection to force update of FillLayer.FillSettings
            fill_layer.resources = fill_layer.resources
            after_fill_settings = cast(ColorFillSettings, fill_layer.fill_settings)

            # Check that fillLayer.FillSettings is updated, not recreated
            assert before_fill_settings, after_fill_settings
            assert Color.green, before_fill_settings.color
{{< /highlight >}}

---
title: Aspose.PSD for Python via .NET 24.9 - Release Notes
type: docs
weight: 10
url: /python-net/aspose-psd-for-python-via-net-24-9-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.9](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**      | **Summary**                                                                                                              | **Category** |
|:-------------|:-------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-95 | [AI Format] Replace standard rendering with APS conversion to reduce file loading speed                                  | Enhancement  |
| PSDPYTHON-96 | Support of artb/artd/abdd/lyvr resources for Artboard                                                                    | Feature      |
| PSDPYTHON-97 | Fix detection of Fill layer                                                                                              | Bug          |
| PSDPYTHON-98 | IndexOutOfRangeException on the updating of TextLayer                                                                    | Bug          |
| PSDPYTHON-99 | Long opening of AI file                                                                                                  | Bug          |
| PSDPYTHON-100| Failed to load FillLayer from Embedded resource stream for Performance report                                            | Bug          |
| PSDPYTHON-101| Exception on reading invalid color value                                                                                 | Bug          |
| PSDPYTHON-104| Starting with Aspose.PSD 24.7.0 issue with the particular document when iterating through Layers: Index was out of range | Bug          |

## **Public API Changes**
# **Added APIs:**

- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BaseArtboardInfoResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AbddResource
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AbddResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AbddResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtBResource
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtBResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtBResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtDResource
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtDResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ArtDResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LyvrResource.Save(Aspose.PSD.StreamContainer,System.Int32)

# **Removed APIs:**
- None

## **Usage examples:**

**PSDPYTHON-95. [AI Format] Replace standard rendering with APS conversion to reduce file loading speed**
{{< highlight python >}}
        sourceFile = "patternstokOnePage.ai"
        start = datetime.now()

        with AiImage.load(sourceFile) as image:
            end = datetime.now()
            if (end - start).seconds > 18:
                raise Exception("The file loading time is too long.")
{{< /highlight >}}

**PSDPYTHON-96. Support of artb/artd/abdd/lyvr resources for Artboard**
{{< highlight python >}}
        srcFile = "artboard1.psd"

        with PsdImage.load(srcFile) as image:
            psdImage = cast(PsdImage, image)
            artDResource = cast(ArtDResource, psdImage.global_layer_resources[2])
            artBResource1 = cast(ArtBResource, psdImage.layers[2].resources[7])
            artBResource2 = cast(ArtBResource, psdImage.layers[5].resources[7])
            lyvrResource1 = cast(LyvrResource, psdImage.layers[2].resources[9])
            lyvrResource2 = cast(LyvrResource, psdImage.layers[5].resources[9])

            countStruct = cast(IntegerStructure, artDResource.items[0])
            assert countStruct.value == 2

            presetNameStruct1 = cast(StringStructure, artBResource1.items[2])
            assert presetNameStruct1.value == "iPhone X\x00"


            presetNameStruct2 = cast(StringStructure, artBResource2.items[2])
            assert presetNameStruct2.value == "iPhone X\x00"

            assert lyvrResource1.version == 160
            assert lyvrResource2.version == 160
{{< /highlight >}}

**PSDPYTHON-97. Fix detection of Fill layer**
{{< highlight python >}}
        inputFile = "FillLayer_ShapeLayer.psd"

        with PsdImage.load(inputFile) as img:
            image = cast(PsdImage, img)
            shapeLayer0 = cast(ShapeLayer, image.layers[0])
            shapeLayer1 = cast(ShapeLayer, image.layers[1])
            shapeLayer2 = cast(ShapeLayer, image.layers[2])
            shapeLayer3 = cast(ShapeLayer, image.layers[3])
            shapeLayer4 = cast(ShapeLayer, image.layers[4])
            shapeLayer8 = cast(ShapeLayer, image.layers[8])
            shapeLayer9 = cast(ShapeLayer, image.layers[9])

            assert shapeLayer0 is not None
            assert shapeLayer1 is not None
            assert shapeLayer2 is not None
            assert shapeLayer3 is not None
            assert shapeLayer4 is not None
            assert shapeLayer8 is not None
            assert shapeLayer9 is not None
{{< /highlight >}}

**PSDPYTHON-98. IndexOutOfRangeException on the updating of TextLayer**
{{< highlight python >}}
       fontsFolder = self.GetFileInBaseFolder("Fonts")

        FontSettings.set_fonts_folders([fontsFolder], True)

        # Inits fonts loading to check if an exception is thrown
        FontSettings.get_adobe_font_name("none")
{{< /highlight >}}

**PSDPYTHON-99. Long opening of AI file**
{{< highlight python >}}
        sourceFile = "choco-kopiya-5_1FfIn55h.ai"

        start = datetime.now()

        with AiImage.load(sourceFile) as image:
            end = datetime.now()
            if (end - start).seconds > 18:
                raise Exception("The file loading time is too long.")
{{< /highlight >}}

**PSDPYTHON-100. Failed to load FillLayer from Embedded resource stream for Performance report**
{{< highlight python >}}
        srcFile = "FillLayersTest.psd"

        with open(srcFile, "rb", buffering=0) as fileStream:
            with Image.load(fileStream) as image:
                # No exception to be thrown here
                pass
{{< /highlight >}}

**PSDPYTHON-101. Exception on reading invalid color value**
{{< highlight python >}}
       srcFile = "Layer123Problem.psd"

        with Image.load(srcFile) as img:
            psdImage = cast(PsdImage, img)
            textLayer = cast(TextLayer, psdImage.layers[0])
            # Here should be no exception
            textData = textLayer.text_data
{{< /highlight >}}

**PSDPYTHON-104. Starting with Aspose.PSD 24.7.0 issue with the particular document when iterating through Layers: Index was out of range**
{{< highlight python >}}
   srcFile = "2176.psd"

        with Image.load(srcFile) as img:
            psdImage = cast(PsdImage, img)
            textLayer = cast(TextLayer, psdImage.layers[100])
            # Here should be no exception
            textData = textLayer.text_data
{{< /highlight >}}
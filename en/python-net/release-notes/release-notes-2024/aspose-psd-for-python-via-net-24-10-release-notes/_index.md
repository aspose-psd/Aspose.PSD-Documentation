---
title: Aspose.PSD for Python via .NET 24.10 - Release Notes
type: docs
weight: 10
url: /python-net/aspose-psd-for-python-via-net-24-10-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.10](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                                                                    | **Category** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-107 | Optimize rendering speed of Gradient Effect                                                                                                    | Enhancement  |
| PSDPYTHON-108 | Fix the issue of updating text with multiple new line symbols                                                                                  | Bug          |
| PSDPYTHON-109 | Open any image file as an embedded smart object in the PSD image doesn't work                                                                  | Bug          |
| PSDPYTHON-110 | Error of processing clipping mask in big image                                                                                                 | Bug          |
| PSDPYTHON-111 | (PSD .NET) UpdateText cutting last letter                                                                                                      | Bug          |
| PSDPYTHON-112 | After saving the PSD file in 3rd party editor, SmartObject.ReplaceContents throws Null Reference but the file still can be opened in Photoshop | Bug          |
| PSDPYTHON-113 | Fix the problem with an exception on the reading of PSD file with Gradient shape                                                               | Bug          |

## **Public API Changes**

# **Added APIs:**
- None

# **Removed APIs:**
- None

## **Usage examples:**

**PSDNET-1308. Fix the issue of updating text with multiple new line symbols**

{{< highlight python >}}
        sourceFile = "TestFileForAsianCharsBig 2.psd"
        testData = "咸咹咺咻咼咽咾咿\r\n哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏"

        with PsdImage.load(sourceFile) as img:
            image = cast(PsdImage, img)
            layer = cast(TextLayer, image.layers[0])
            # Here should be no exception.
            layer.update_text(testData)
{{< /highlight >}}

**PSDNET-1931. Open any image file as an embedded smart object in the PSD image doesn't work**

{{< highlight python >}}
        sourceFile = "smart.psd"
        addFile = "DragonFly.jpeg"
        outputFile = "DragonFly_export.png"
        outputPsd = "DragonFly_export.psd"

        psdOpt = PsdLoadOptions()
        psdOpt.load_effects_resource = True
        with PsdImage.load(sourceFile, psdOpt) as image:
            psdImage = cast(PsdImage, image)
            with open(addFile, "rb", buffering=0) as stream:
                with SmartObjectLayer(stream) as smartLayer:
                    psdImage.add_layer(smartLayer)
                    pngOpt = PngOptions()
                    pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA
                    psdImage.save(outputFile, pngOpt)
                    psdImage.save(outputPsd, PsdOptions())
{{< /highlight >}}

**PSDNET-2060. Optimize rendering speed of Gradient Effect**

{{< highlight python >}}
        inputFile = "PsdDockerExample.psd"
        outputFilePsd = "PsdDockerExample_output.psd"

        psdOpt = PsdLoadOptions()
        psdOpt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(inputFile, psdOpt) as img:
            start = datetime.now()
            img.save(outputFilePsd, pngOpt)
            end = datetime.now()

        if (end - start).seconds > 18:
            raise Exception("Performance problem. Saving should not take more than 10 seconds.")
{{< /highlight >}}

**PSDNET-2084. Error of processing clipping mask in big image**

{{< highlight python >}}
        src = "input.psd"
        output = "out_PSDNET2084.psd"

        with PsdImage.load(src) as image:
            psdImage = cast(PsdImage, image)
            layers = psdImage.layers

            # Select issue layers to speed up processing
            psdImage.layers = [layers[174], layers[175]]

            # Here should be no exception on saving
            psdImage.save(output)
{{< /highlight >}}

**PSDNET-2183. (PSD .NET) UpdateText cutting last letter**

{{< highlight python >}}
        srcFile = "frenteee.psd"
        outFilePng = "out_frenteee.png"

        with PsdImage.load(srcFile) as psdImage:
            psdImage.save(outFilePng, PngOptions())
{{< /highlight >}}

**PSDNET-2184. After saving the PSD file in 3rd party editor, SmartObject.ReplaceContents throws Null Reference but the file still can be opened in Photoshop**

{{< highlight python >}}
        sourceFile = "snapcase.psd"
        changeFile = "snapcase_change.png"

        with PsdImage.load(sourceFile) as image:
            psdImage = cast(PsdImage, image)
            for layer in psdImage.layers:
                if isinstance(layer, SmartObjectLayer) and layer.name == "ARTHERE":
                    smartObjectLayer = SmartObjectLayer(layer)

                    # Exception was here
                    smartObjectLayer.replace_contents(changeFile)
                    smartObjectLayer.embed_linked()

                    break
{{< /highlight >}}

**PSDNET-2192. Fix the problem with an exception on the reading of PSD file with Gradient shape**

{{< highlight python >}}
        # Temporary disabled. Fixed in 24.11
        inputFile = "vectormasks.psd"
        outputFilePsd = "vectormasks_output.psd"
        referenceFilePsd = "vectormasks_output.psd"

        with PsdImage.load(inputFile) as img:
            image = cast(PsdImage, img)
            # Should be no exception

            # Test Gradient parameters
            shapeLayer = cast(ShapeLayer, image.layers[1])
            gradientSettings = cast(NoiseGradientFillSettings, shapeLayer.stroke.fill)

            assert True == gradientSettings.dither
            assert True == gradientSettings.reverse
            assert 90.0 == gradientSettings.angle
            assert 80 == gradientSettings.scale
            assert True == gradientSettings.align_with_layer
            assert GradientType.Radial == gradientSettings.gradient_type
            assert GradientKind.Noise == gradientSettings.gradient_mode
            assert 1837065285 == gradientSettings.rndNumberSeed
            assert False == gradientSettings.show_transparency
            assert False == gradientSettings.use_vector_color
            assert 2048 == gradientSettings.roughness
            assert NoiseColorModel.HSB == gradientSettings.color_model
            assert 0 == gradientSettings.expansion_count

            # Edit
            gradientSettings.dither = False
            gradientSettings.reverse = False
            gradientSettings.angle = 54.0
            gradientSettings.scale = 34
            gradientSettings.align_with_layer = False
            gradientSettings.gradient_type = GradientType.LINEAR
            gradientSettings.show_transparency = True
            gradientSettings.use_vector_color = True
            gradientSettings.roughness = 3072
            gradientSettings.color_model = NoiseColorModel.RGB

            image.save(outputFilePsd)

        with PsdImage.load(outputFilePsd) as img:
            image = cast(PsdImage, img)

            # Should be no exception

            # Test Gradient parameters
            shapeLayer = cast(ShapeLayer, image.layers[1])
            gradientSettings = cast(NoiseGradientFillSettings, shapeLayer.stroke.fill)

            assert False == gradientSettings.dither
            assert False == gradientSettings.reverse
            assert 54.0 == gradientSettings.angle
            assert 34 == gradientSettings.scale
            assert False == gradientSettings.align_with_layer
            assert GradientType.LINEAR == gradientSettings.gradient_type
            assert GradientKind.NOISE == gradientSettings.gradient_mode
            assert 1837065285 == gradientSettings.rndNumberSeed
            assert True == gradientSettings.show_transparency
            assert True == gradientSettings.use_vector_color
            assert 3072 == gradientSettings.roughness
            assert NoiseColorModel.RGB == gradientSettings.color_model
            assert 0 == gradientSettings.expansion_count

            def AssertAreEqual(self, expected, actual, message=None):
                if expected != actual:
                    raise Exception(message or "Objects are not equal.")
{{< /highlight >}}
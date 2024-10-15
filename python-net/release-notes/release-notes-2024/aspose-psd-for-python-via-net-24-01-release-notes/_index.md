---
title: Aspose.PSD for Python via .NET 24.1 - Release Notes
type: docs
weight: 90
url: /net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

This page contains release notes for [Aspose.PSD for Python via .NET 24.1](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Key**     | **Summary**                                                                                                | **Category** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI Format] Add basic handling for multipage AI images                                                    |   Feature   |
|  PSDPYTHON-22 | Warp Text Effect doesn’t apply to text                                                                    |     Bug     |
|  PSDPYTHON-23 | Incorrect rendering of mask in the specific file                                                          |     Bug     |
|  PSDPYTHON-24 | NullReferenceException at Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor            |     Bug     |
|  PSDPYTHON-25 | [AI Format] Fixing the memory usage in AiExporterUtils                                                    |     Bug     |



## **Public API Changes**
# **Added APIs:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Removed APIs:**
- None


## **Usage examples:**

**PSDPYTHON-19. [AI Format] Add basic handling for multipage AI images**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # Load the AI image.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # By default, the ActivePageIndex is 0.
            # So if you save the AI image without changing this property, the first page will be rendered and saved.
            image.save(firstPageOutputPng, PngOptions())

            # Change the active page index to the second page.
            image.active_page_index = 1

            # Save the second page of the AI image as a PNG image.
            image.save(secondPageOutputPng, PngOptions())

            # Change the active page index to the third page.
            image.active_page_index = 2

            # Save the third page of the AI image as a PNG image.
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. Warp Text Effect doesn’t apply to text**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("text_warp.psd")
        outputFile = self.GetFileInOutputFolder("export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True
        opt.allow_warp_repaint = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile, opt) as img:
            img.save(outputFile, pngOpt)
{{< /highlight >}}

**PSDPYTHON-23. Incorrect rendering of mask in the specific file**

{{< highlight python >}}
        sourceFile1 = self.GetFileInBaseFolder("mask_problem.psd")
        sourceFile2 = self.GetFileInBaseFolder("puh_softLight3_1.psd")
        outputFile1 = self.GetFileInOutputFolder("mask_export.png")
        outputFile2 = self.GetFileInOutputFolder("puh_export.png")

        opt = PsdLoadOptions()
        opt.load_effects_resource = True

        pngOpt = PngOptions()
        pngOpt.compression_level = 9
        pngOpt.color_type = PngColorType.TRUECOLOR_WITH_ALPHA

        with PsdImage.load(sourceFile1, opt) as img:
            img.save(outputFile1, pngOpt)

        with PsdImage.load(sourceFile2, opt) as img:
            img.save(outputFile2, pngOpt)
{{< /highlight >}}

**PSDPYTHON-24. NullReferenceException at Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI Format] Fixing the memory usage in AiExporterUtils**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C# Memory usage is 220, but for python we have no direct access to GC activities.
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # Load the AI image.
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # Save the first page of the AI image as a PNG image.
            image.save(firstPageOutputPng, pngOpt)

            # Change the active page index to the second page.
            image.active_page_index = 1

            # Save the second page of the AI image as a PNG image.
            image.save(secondPageOutputPng, pngOpt)

            # Change the active page index to the third page.
            image.active_page_index = 2

            # Save the third page of the AI image as a PNG image.
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("Usage of memory is too big. {} instead of {:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

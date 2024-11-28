---
title: Aspose.PSD for Python via .NET 24.1 - 发行说明
type: docs
weight: 10
url: /zh/net/aspose-psd-for-python-via-net-24-1-release-notes/
---

{{% alert color="primary" %}}

本页面包含[Aspose.PSD for Python via .NET 24.1](https://pypi.org/project/aspose-psd/)的发行说明

{{% /alert %}}

| **关键**     | **摘要**                                                                                                | **类别** |
|:--------------|:----------------------------------------------------------------------------------------------------------|:------------|
|  PSDPYTHON-19 | [AI格式] 添加对多页AI图像的基本处理                                                                             |   功能   |
|  PSDPYTHON-22 | 扭曲文本效果不适用于文本                                                                                    |     错误     |
|  PSDPYTHON-23 | 特定文件中蒙版的渲染不正确                                                                                  |     错误     |
|  PSDPYTHON-24 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor中的NullReferenceException            |     错误     |
|  PSDPYTHON-25 | [AI格式] 修复AiExporterUtils中的内存使用                                                                       |     错误     |



## **公共API更改**

# **已添加的API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **已移除的API:**
- None


## **用法示例:**

**PSDPYTHON-19. [AI格式] 添加对多页AI图像的基本处理**

{{< highlight python >}}
        sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # 加载AI图像。
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)
            # 默认情况下，ActivePageIndex为0。
            # 因此，如果保存AI图像而不更改此属性，则将呈现并保存第一页。
            image.save(firstPageOutputPng, PngOptions())

            # 将活动页索引更改为第二页。
            image.active_page_index = 1

            # 保存AI图像的第二页为PNG图像。
            image.save(secondPageOutputPng, PngOptions())

            # 将活动页索引更改为第三页。
            image.active_page_index = 2

            # 保存AI图像的第三页为PNG图像。
            image.save(thirdPageOutputPng, PngOptions())
{{< /highlight >}}

**PSDPYTHON-22. 扭曲文本效果不适用于文本**

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

**PSDPYTHON-23. 特定文件中蒙版的渲染不正确**

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

**PSDPYTHON-24. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor中的NullReferenceException**

{{< highlight python >}}
        fontsFolder = self.GetFileInBaseFolder("Fonts")
        FontSettings.set_fonts_folders([fontsFolder], True)


        inputFile = self.GetFileInBaseFolder("1.psd")
        outputFile = self.GetFileInOutputFolder("out_1855.png")
        referenceFile = self.GetFileInBaseFolder("out_1855.png")

        with PsdImage.load(inputFile) as psdImage:
            psdImage.save(outputFile, PngOptions())
{{< /highlight >}}

**PSDPYTHON-25. [AI格式] 修复AiExporterUtils中的内存使用**

{{< highlight python >}}
  sourceFile = self.GetFileInBaseFolder("threePages.ai")
        firstPageOutputPng = self.GetFileInOutputFolder("firstPageOutput.png")
        secondPageOutputPng = self.GetFileInOutputFolder("secondPageOutput.png")
        thirdPageOutputPng = self.GetFileInOutputFolder("thirdPageOutput.png")

        # C#的内存使用为220，但对于Python，我们无法直接访问GC活动。
        MemoryLimit = 1500
        process = psutil.Process()
        startMemory = process.memory_info().rss
        pngOpt = PngOptions()
        # 加载AI图像。
        with Image.load(sourceFile) as img:
            image = cast(AiImage, img)

            # 保存AI图像的第一页作为PNG图像。
            image.save(firstPageOutputPng, pngOpt)

            # 将活动页索引更改为第二页。
            image.active_page_index = 1

            # 保存AI图像的第二页作为PNG图像。
            image.save(secondPageOutputPng, pngOpt)

            # 将活动页索引更改为第三页。
            image.active_page_index = 2

            # 保存AI图像的第三页作为PNG图像。
            image.save(thirdPageOutputPng, pngOpt)

        endMemory = process.memory_info().rss

        memoryUsed = (endMemory - startMemory) / 1024 / 1024

        if memoryUsed > MemoryLimit:
            raise Exception("内存使用过大。{}而非{:.1f}".format(memoryUsed, MemoryLimit))
{{< /highlight >}}

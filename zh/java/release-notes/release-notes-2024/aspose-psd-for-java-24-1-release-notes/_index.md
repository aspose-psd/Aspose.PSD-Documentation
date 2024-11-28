---
title: Aspose.PSD的Java 24.1版本发布说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-24-1-release-notes/
---

{{% alert color="primary" %}} 本页面包含[Aspose.PSD的Java 24.1版本](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/)的发布说明 {{% /alert %}}

| **关键字**   | **摘要**                                                                                  | **类别**   |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [AI格式] 添加多页面AI图像的基本处理。                                                          | 功能       |
| PSDJAVA-579 | 文本效果不适用于文字。                                                                      | 故障       |
| PSDJAVA-580 | 特定文件中蒙版的渲染不正确。                                                               | 故障       |
| PSDJAVA-581 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor处的NullReferenceException。| 故障|
| PSDJAVA-582 | [AI格式] 修复AiExporterUtils中的内存使用。                                                   | 故障       |

## **公共API更改**
# **新增API:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
...
...

# **已移除API:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither
...
...

## **用法示例：**

** PSDJAVA-576. [AI格式] 添加多页面AI图像的基本处理**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        String firstPageOutputPng = "src/main/resources/firstPageOutput.png";
        String secondPageOutputPng = "src/main/resources/secondPageOutput.png";
        String thirdPageOutputPng = "src/main/resources/thirdPageOutput.png";

        // Load the AI image.
        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // By default, the ActivePageIndex is 0.
            // So if you save the AI image without changing this property, the first page will be rendered and saved.
            image.save(firstPageOutputPng, new PngOptions());

            // Change the active page index to the second page.
            image.setActivePageIndex(1);

            // Save the second page of the AI image as a PNG image.
            image.save(secondPageOutputPng, new PngOptions());

            // Change the active page index to the third page.
            image.setActivePageIndex(2);

            // Save the third page of the AI image as a PNG image.
            image.save(thirdPageOutputPng, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. 文本效果不适用于文字**

{{< highlight java >}}

        String sourceFile = "src/main/resources/text_warp.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-580. 特定文件中蒙版的渲染不正确**

{{< highlight java >}}

        String sourceFile1 = "src/main/resources/mask_problem.psd";
        String sourceFile2 = "src/main/resources/puh_softLight3_1.psd";
        String outputFile1 = "src/main/resources/mask_export.png";
        String outputFile2 = "src/main/resources/puh_export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile1, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile1, pngOptions);
        }

        try (PsdImage img = (PsdImage) Image.load(sourceFile2, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-581. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor处的NullReferenceException**

{{< highlight java >}}

        String fontsFolder = "src/main/resources/Fonts";
        FontSettings.setFontsFolders(new String[]{fontsFolder}, true);

        String inputFile = "src/main/resources/1.psd";
        String outputFile = "src/main/resources/out_1855.png";
        try (PsdImage psdImage = (PsdImage) Image.load(inputFile)) {
            psdImage.save(outputFile, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [AI格式] 修复AiExporterUtils中的内存使用**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        String firstPageOutputPng = "src/main/resources/firstPageOutput.png";
        String secondPageOutputPng = "src/main/resources/secondPageOutput.png";
        String thirdPageOutputPng = "src/main/resources/thirdPageOutput.png";

        final double MemoryLimit = 700;
        double memoryUsed = Double.MAX_VALUE;

        // Load the AI image.
        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // Save the first page of the AI image as a PNG image.
            image.save(firstPageOutputPng, new PngOptions());

            // Change the active page index to the second page.
            image.setActivePageIndex(1);

            // Save the second page of the AI image as a PNG image.
            image.save(secondPageOutputPng, new PngOptions());

            // Change the active page index to the third page.
            image.setActivePageIndex(2);

            // Save the third page of the AI image as a PNG image.
            image.save(thirdPageOutputPng, new PngOptions());
        }

        System.gc();

        memoryUsed = (double) (Runtime.getRuntime().totalMemory() - Runtime.getRuntime().freeMemory()) / (1024.0 * 1024.0);

        if (memoryUsed > MemoryLimit) {
            throw new RuntimeException("内存使用过大。实际使用量为" + memoryUsed + "，而不是" + String.format("%.1f", MemoryLimit));
        }

{{< /highlight >}}
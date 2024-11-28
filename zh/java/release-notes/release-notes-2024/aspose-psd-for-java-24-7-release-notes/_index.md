---
title: Aspose.PSD for Java 24.7 - 发布说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} 本页包含了 [Aspose.PSD for Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) 的发行说明 {{% /alert %}}

| **关键**     | **摘要**                                                                                      | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | 打开 AI 文档时出现“图像加载失败”异常                                                             | 错误          |
| PSDJAVA-636 | 输出 PDF 文件时文本渲染不正确                                                                     | 错误          |
| PSDJAVA-637 | 在 Linux 上导出失败给定文件时修复 ImageSaveException                                            | 错误          |
| PSDJAVA-638 | 使用 Aspose.Drawing 时修复字体加载                                                               | 错误          |
| PSDJAVA-639 | 使用大型 JPEG 创建智能对象图层时出现“算术运算导致溢出”                                          | 错误          |
| PSDJAVA-640 | 无法将 AI 文件转换为 JPG 文件                                                                    | 错误          |

## **公共 API 更改**
# **新增的 API:**

- 无

# **移除的 API:**

- 无 

## **使用示例:**

**PSDJAVA-635. 打开 AI 文档时出现“图像加载失败”异常**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. 输出 PDF 文件时文本渲染不正确**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. 在 Linux 上导出失败给定文件时修复 ImageSaveException**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. 使用 Aspose.Drawing 时修复字体加载**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- 更新前已安装字体数: " + installedFonts.getFamilies().length);
        System.out.println("- 平台: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- 通过尝试获取‘Arial’的Adobe字体名称来刷新字体缓存: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- 更新后已安装字体数: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 使用大型 JPEG 创建智能对象图层时出现“算术运算导致溢出”**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. 无法将 AI 文件转换为 JPG 文件**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

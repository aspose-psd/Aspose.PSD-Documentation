---
title: Aspose.PSD for Java 23.9 - 发行说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} 本页面包含[Aspose.PSD for Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/)的发行说明 {{% /alert %}}

| **关键字**   | **摘要**                                                                                                                                      | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | 实现为新调整图层创建蒙版                                                                                             |    功能   |
| PSDJAVA-528 | 添加对剪裁图层混合为组合选项的支持                                                                                     |    功能   |
| PSDJAVA-529 | 具有16位颜色模式的PSD文件不适用于调整图层的蒙版                                                                          |      错误     |
| PSDJAVA-530 | 文本图层中括号的渲染不正确                                                                                                |      错误     |
| PSDJAVA-531 | 无法更新文本图层中的样式                                                                                                         |      错误     |
| PSDJAVA-532 | 使用CMYK导出PSD文件后，导出的PSD文件中颜色错误                                                                               |      错误     |
| PSDJAVA-533 | 特定PSB文件引发异常“该矩形没有共同的处理区域”                                                                              |      错误     |
| PSDJAVA-534 | 图像加载失败。OverflowException：算术操作导致溢出。                                                                   |      错误     |

## **公共API更改**
# **新增API:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **移除API:**

- 无

## **用法示例:**

** PSDJAVA-527. 实现为新调整图层创建蒙版**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();
        
        im.save(dstFile);
    }
    
    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];
        
        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "对象不相等。");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. 添加对剪裁图层混合为组合选项的支持**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";
    
    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-529. 具有16位颜色模式的PSD文件不适用于调整图层的蒙版**

{{< highlight java >}}
	String sourceFile = "src/main/resources/source.psd";
    String outputPng = "src/main/resources/current.png";
    
    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-530. 文本图层中括号的渲染不正确**

{{< highlight java >}}
    String file = "src/main/resources/file1.psd";
    String output = "src/main/resources/output_1235.png";
    
    try (PsdImage psdImage = (PsdImage) Image.load(file)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getTextData().updateLayerData();
                
                PsdOptions imageOptions = new PsdOptions(psdImage);
                psdImage.save(output, imageOptions);
            }
        }
    }
{{< /highlight >}}


** PSDJAVA-531. 无法更新文本图层中的样式**

{{< highlight java >}}
    String sourceFile = "src/main/resources/Example_FontSize.psd";
    String outputFile = "src/main/resources/output_Example_FontSize.psd";
    
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        TextLayer l1 = (TextLayer) psdImage.getLayers()[4];
        TextLayer l2 = (TextLayer) psdImage.getLayers()[5];
        
        ITextPortion[] textItems1 = l1.getTextData().producePortions(new String[]{"text1", "text2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());
                
        l1.getTextData().removePortion(0);
        for (ITextPortion item : textItems1) {
            l1.getTextData().addPortion(item);
        }
        
        ITextPortion[] textItems2 = l2.getTextData().producePortions(new String[]{"text layer 1", "text layer 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());
                
        for (ITextPortion item : textItems2) {
            l2.getTextData().addPortion(item);
        }
        
        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();
        
        psdImage.save(outputFile);
    }
{{< /highlight >}}


** PSDJAVA-532. 使用CMYK导出PSD文件后，导出的PSD文件中颜色错误**

{{< highlight java >}}
    String sourceFile = "src/main/resources/canyon.psd";
    String outputFilePng = "src/main/resources/output_canyon.png";
    
    MemoryStream outputStream = new MemoryStream();
    
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        psdImage.save(outputStream.toOutputStream());
    }
    
    outputStream.setPosition(0);
    try (PsdImage psdImage = (PsdImage) Image.load(outputStream.toInputStream())) {
        psdImage.save(outputFilePng, new PngOptions());
    }
    
    outputStream.close();
{{< /highlight >}}


** PSDJAVA-533. 特定PSB文件引发异常“该矩形没有共同的处理区域”**

{{< highlight java >}}
    String input = "src/main/resources/1619_src.psb";
    String output = "src/main/resources/1619_output.png";
    
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage img = (PsdImage) Image.load(input, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        img.save(output, pngOptions);
    }
{{< /highlight >}}


** PSDJAVA-534. 图像加载失败。OverflowException：算术操作导致溢出。**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";
    
    try (PsdImage im = (PsdImage)PsdImage.load(sourceFile))
    {
        Layer layer = im.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)layer.getResources()[0];
        
        assertAreEqual("自定", grdmResource.getGradientName());
    }
    
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "对象不相等。");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

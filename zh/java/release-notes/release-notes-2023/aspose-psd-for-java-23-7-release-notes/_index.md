---
title: Aspose.PSD for Java 23.7 - 发行说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} 本页包含 [Aspose.PSD for Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) 的发行说明 {{% /alert %}}

| **关键**     | **摘要**                                                                                                                                      | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | 添加将 PSD 文件的每个图层导出为动画 GIF 文件的功能                                        | 特性 |
| PSDJAVA-503 | 为 Shape 图层分配来自 vscg 资源的填充属性                                                       | 特性 |
| PSDJAVA-504 | 添加新的扭曲类型 (弧 & 拱)                                                                           | 特性 |
| PSDJAVA-505 | 如果属性 UpdateMetadata 设置为 true，则更改保存 PSD 文件的应用程序为 Aspose.PSD       | 特性 |
| PSDJAVA-510 | 增加变形图像的计算区域                                                                               | 特性 |
| PSDJAVA-511 | 黑白调整图层处理半透明度时错误                                                              | 错误     |
| PSDJAVA-512 | SmartObject ReplaceContents (当 AllowWarpRepaint 选项激活时) 在计算 2 分钟后失败     | 错误     |
| PSDJAVA-513 | 添加获取实际图层组左侧和顶部位置的功能                                                    | 错误     |
| PSDJAVA-514 | 当 psd 文件中有结构为点的 VogkResource 时，图层调整大小错误                               | 错误     |
| PSDJAVA-515 | TextBound 的工作方式不如预期                                            | 错误     |
| PSDJAVA-516 | 使用默认构造函数创建的图层添加到 PSD 图像时不会添加默认资源           | 错误     |
| PSDJAVA-517 | 导出为动画 GIF 时忽略 Timeline.LoopesCount                                  | 错误     |

## **公共 API 更改**
# **已添加的 API:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **已移除的 API:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **使用示例:**

**PSDJAVA-502. 添加将 PSD 文件的每个图层导出为动画 GIF 文件的功能**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // 为每个图层创建帧。
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // 更新当前状态
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. 为 Shape 图层分配来自 vscg 资源的填充属性**

{{< highlight java >}}
        // 实色填充示例
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
...
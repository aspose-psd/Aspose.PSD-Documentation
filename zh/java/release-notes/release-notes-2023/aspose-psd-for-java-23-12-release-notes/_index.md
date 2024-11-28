---
title: Aspose.PSD for Java 23.12发布说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-23-12-release-notes/
---

{{% alert color="primary" %}} 本页面包含 [Aspose.PSD for Java 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) 的发布说明 {{% /alert %}}

| **关键**     | **摘要**                                                                                            | **类别** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [AI格式] 在新版本AI中添加对栅格图像渲染的支持。                                                      | 功能      |
| PSDJAVA-566 | 处理GdflResrource中的渐变类型噪音。                                                                 | 功能      |
| PSDJAVA-567 | 保存文本图层后更新时出现“对象引用未设置为对象的实例”的错误。                                           | 缺陷      |
| PSDJAVA-568 | 修复MacOS上使用System.Drawing.Common和Aspose.Drawing手动加载字体的问题。                                 | 缺陷      |
| PSDJAVA-569 | PsdLoadOptions中的AllowWarpRepaint导致异常。                                                          | 缺陷      |
| PSDJAVA-570 | [AI格式] 实现交叉参考流的处理。                                                                    | 增强功能  |
| PSDJAVA-571 | VectorPathDataResource的许可控制工作不正确。                                                       | 增强功能  |
| PSDJAVA-574 | 在PSD图像中将任何图像文件作为嵌入式智能对象打开。                                                   | 增强功能  |

## **公共API更改**
# **已添加的API:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent1
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent2
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent4 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorSpace 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getFlag 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getKey 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getLength 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getPsdVersion 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getSignature 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent1(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent2(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent3(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent4(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorSpace(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setOpacity(short)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.TypeToolKey 
- T:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.CMYK 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.GrayScale 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.HSB 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.Lab 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getColorModel 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMaximumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMinimumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRndNumberSeed 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRoughness 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getShowTransparency 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setUseVectorColor(boolean)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAlignWithLayer 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientMode 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getScale 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getVerticalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setVerticalOffset(double)

# **已删除的API:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
  M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getScale 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getVerticalOffset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setVerticalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColorPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientName 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getTransparencyPoints 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColorPoints(com.aspose.psd.fileformats.psd.layers.IGradientColorPoint[])
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setTransparencyPoints(com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint[])
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **用法示例：**

** PSDJAVA-565. [AI格式] 在新版本AI中添加对栅格图像渲染的支持 **

{{< highlight java >}}


    String sourceFile = "src/main/resources/raster.ai";
    String outputFile = "src/main/resources/raster_output.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}


** PSDJAVA-566. 处理GdflResrource中的渐变类型噪音 **

{{< highlight java >}}


    String sourceFile = "src/main/resources/Gradient-Fill.psd";
    String destFile = "src/main/resources/Gradient-Fill-out.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile, new PsdLoadOptions())) {
        Layer layer = image.getLayers()[1];

        for (LayerResource resource : layer.getResources()) {
            GdFlResource gdFlResource = (GdFlResource) resource;

            if (gdFlResource != null) {
                gdFlResource.setScale(90);
                gdFlResource.setAngle(30);
                gdFlResource.setDither(false);
                gdFlResource.setAlignWithLayer(true);
                gdFlResource.setReverse(false);

                break;
            }
        }
        image.save(destFile, new PsdOptions());
    }

{{< /highlight >}}


** PSDJAVA-567. 保存文本图层后更新时出现“对象引用未设置为对象的实例”的错误 **

{{< highlight java >}}


    String sourceFile = "src/main/resources/input_1827.psd";
    String outputFile = "src/main/resources/out_1827.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                ((TextLayer) layer).getTextData().updateLayerData();
            }
        }

        // 这里不应该有错误
        psdImage.save(outputFile);
    }

{{< /highlight >}}


** PSDJAVA-569. PsdLoadOptions中的AllowWarpRepaint导致异常 **

{{< highlight java >}}


    String sourceFile = "src/main/resources/SizeChart - 4 Colors.psd";
    String outputFile = "src/main/resources/_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        png
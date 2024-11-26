---
title: Aspose.PSD for Java 20.5 - 发行说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} 本页面包含[Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/)的发行说明 {{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDJAVA-188|支持文档转换进度|特性|
|PSDJAVA-197|支持使用每通道16位的灰度ColorMode PSD图像保存|特性|
|PSDJAVA-198|支持Nvrt资源（反色调整层资源）|特性|
|PSDJAVA-200|支持图层组的图层蒙版|特性|
|PSDJAVA-195|修复将灰度ColorMode 16位每通道PSD图像保存为16位每通道RGB PSD格式时的问题|错误|
|PSDJAVA-196|修复将灰度ColorMode 16位每通道PSD图像保存为8位每通道灰度PSD格式时的问题|错误|
|PSDJAVA-199|通过ITextPortion进行文本对齐不适用于从右到左的语言。输出文件损坏。|错误|
|PSDJAVA-201|尝试打开具有Lab颜色和每通道8位的特定Psd文件时发生异常|错误|
# **公共API更改**
# **添加的API：**
- 无
## **已删除的API：**
- 无
# **用法示例：**

**PSDJAVA-188. 支持文档转换进度**

{{< highlight java >}}

 // 使用进度处理程序进行加载和保存操作的示例。

// 程序使用不同的保存选项触发进度事件。

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// 创建一个将进度信息写入控制台的进度处理程序

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s out of %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- 加载 Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// 将进度处理程序绑定到显示加载进度

loadOptions.setProgressEventHandler(localProgressEventHandler);

// 使用特定的加载选项加载PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- 保存 Apple.psd 为 PNG 格式 ----------");

    PngOptions pngOptions = new PngOptions();

    // 使输出图像有颜色且非透明

    pngOptions.setColorType(PngColorType.Truecolor);

    // 将进度处理程序绑定到显示保存进度

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // 使用特定特性将PSD转换为PNG

    image.save(outputStream, pngOptions);

    System.out.println("---------- 保存 Apple.psd 为 PSD 格式 ----------");

    PsdOptions psdOptions = new PsdOptions();

    // 使输出PSD有颜色

    psdOptions.setColorMode(ColorModes.Rgb);

    // 为每种颜色（红色、绿色和蓝色）加上一个通道，再加上一个复合通道

    psdOptions.setChannelsCount((short)4);

    // 将进度处理程序绑定到显示保存进度

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // 使用特定特性保存带有的PSD 副本

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. 支持使用每通道16位的灰度ColorMode PSD图像保存**

{{< highlight java >}}

 // 应用不同的颜色模式、每通道位数、通道计数和压缩组合的示例。

// 使一个方法能够从本地范围访问

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // 加载预定义的16位灰度PSD

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // 在图层周围绘制灰色内边框

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // 保存带有特定特性的PSD副本

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // 加载保存的PSD

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // 将保存的PSD转换为灰度PNG图片

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // 此处不应有异常

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. 支持Nvrt资源（反色调整层资源）**

{{< highlight java >}}

 // 查找反色调整图层的NvrtResource的示例。

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// 加载包含反色调整图层的预定义PSD

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 尝试查找反色调整图层的资源

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // 找到NvrtResource

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. 支持图层组的图层蒙版**

{{< highlight java >}}

 // 支持图层组的图层蒙版的示例。该程序加载并保存PSD到不同的输出格式，不会抛出异常。

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// 加载包含图层组的图层蒙版的预定义PSD

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // 将加载的PSD转换为PNG

    input.save(outputPng, new PngOptions());

    // 保存PSD的副本

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. 修复将灰度ColorMode 16位每通道PSD图像保存为16位每通道RGB PSD格式时的问题**

{{< highlight java >}}

 // 将16位灰度PSD转换为16位RGB图像，然后再转换为16位灰度像素图像的示例。

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// 加载预定义的16位灰度PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // 在图层周围绘制灰色内边框

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // 将颜色模式改为RGB保存PSD的副本

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 加载保存的PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 将保存的PSD转换为灰度PNG图片

    image1.save(pngExportPath, pngOptions); // 此处不应有异常

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. 修复将灰度ColorMode 16位每通道PSD图像保存为8位每通道灰度PSD格式时的问题**

{{< highlight java >}}

 // 将16位灰度PSD转换为8位灰度图像，然后再转换为8位灰度像素图像的示例。

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// 加载预定义的16位灰度PSD

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // 在图层周围绘制灰色内边框

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // 将通道计数改为8位保存PSD的副本

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// 加载保存的PSD

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // 将保存的PSD转换为灰度PNG图片

    image1.save(pngExportPath, pngOptions); // 此处不应有异常

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. 通过ITextPortion进行文本对齐不适用于从右到左的语言。输出文件损坏。**

{{< highlight java >}}

 // 通过ITextPortion对齐RTL文本图层的示例。程序修改加载的PSD中的现有RTL文本图层，并保存修改后的文档的副本。

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// 加载包含RTL文本图层的预定义PSD

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // 从图层获取文本部分

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // 更改文本对齐方式

    portions[0].getParagraph().setJustification(2);

    // 应用更改到图层

    layer.getTextData().updateLayerData();

    // 保存修改后的PSD副本

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. 尝试打开具有Lab颜色和每通道8位的特定Psd文件时发生异常**

{{< highlight java >}}

 // 支持LAB颜色模式中的8位Photoshop文档的示例。

String srcFile = "Untitled-1.psd";

String outputFilePsd = "output.psd";

// 加载具有LAB颜色模式的预定义8位PSD

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // 保存加载的PSD的副本

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}
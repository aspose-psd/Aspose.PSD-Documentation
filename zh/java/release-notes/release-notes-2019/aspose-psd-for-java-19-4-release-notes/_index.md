---
title: Aspose.PSD for Java 19.4 - 发布说明
type: docs
weight: 20
url: /zh/java/aspose-psd-for-java-19-4-release-notes/
---

{{% alert color="primary" %}}

这个页面包含了Aspose.PSD for Java 19.4的发布说明

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDJAVA-1|添加功能以在不直接加载的情况下将JPEG/PNG等图像文件加载到PsdImage中(不支持Aspose.PSD)|功能|
|PSDJAVA-2|支持具有16位/通道的RGB颜色模式(每种颜色有64位)|功能|
|PSDJAVA-3|支持图层矢量蒙版和文本图层自定义翻转旋转|功能|
|PSDJAVA-4|所有亚洲字符都无法正确呈现|错误|
|PSDJAVA-5|\r\n符号被解释为错误的双行间断|错误|
|PSDJAVA-6|如果使用包含断行的字符串更新TextLayer，则PSD文件将变得无法读取|错误|
|PSDJAVA-7|如果使用包含制表符的字符串更新TextLayer，则处理将失败并显示异常|错误|
# **公共API更改**
# **已添加的API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **已删除的API:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- ...（省略部分内容）
# **用法示例:**

**PSDJAVA-1. 添加加载JPEG/PNG等图像文件到PsdImage的功能，无需直接加载（Aspose.PSD不支持）**

{{< highlight java >}}

 String filePath = "PsdExample.psd";

    String outputFilePath = "PsdResult.psd";

    PsdImage image = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(filePath);

         try 

         {

              Layer layer = null;

              try

              {

                  layer = new Layer((RasterImage)im);

                  image.addLayer(layer);

                  image.save(outputFilePath);

              }

              catch

              {

                  if (layer != null)

                  {

                       layer.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         image.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. 支持具有16位/通道的RGB颜色模式（每种颜色有64位）**

{{< highlight java >}}

  // 支持具有16位/通道的RGB颜色模式（每种颜色有64位）


...

{{< /highlight >}}

**PSDJAVA-3. 支持图层矢量蒙版和文本图层自定义翻转旋转**

{{< highlight java >}}

 // 旋转翻转操作与PSD文件中期望的不符

...

{{< /highlight >}}

**PSDJava-4. 所有亚洲字符都无法正确呈现**

[**请查看附带的示例**](attachments/92602686/92766213.java)

**PSDJAVA-5. \r\n符号被解释为错误的双行间断**

{{< highlight java >}}

...

{{< /highlight >}}

...

**PSDJAVA-6. 如果使用包含断行的字符串更新TextLayer，则PSD文件将变得无法读取**

{{< highlight java >}}

...

{{< /highlight >}}

...

**PSDJAVA-7. 如果使用包含制表符的字符串更新TextLayer，则处理将失败并显示异常**

{{< highlight java >}}

...

{{< /highlight >}}
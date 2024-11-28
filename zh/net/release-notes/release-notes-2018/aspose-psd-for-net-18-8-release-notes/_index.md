---
title: Aspose.PSD for .NET 18.8 - 发行说明
type: docs
weight: 50
url: /zh/net/aspose-psd-for-net-18-8-release-notes/
---

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-68|支持LayerCreationDateTime属性。|特性|
|PSDNET-67|支持SheetColor Highlighting|特性|
|PSDNET-66|能够合并层之间的图层|特性|
|PSDNET-65|部分支持文本图层BoundBox属性|特性|
|PSDNET-64|支持IopaResource|特性|
|PSDNET-56|支持PSD格式的图层效果|特性|
|PSDNET-55|.Net的InterruptMonitor支持|特性|
|PSDNET-50|使图层展平成为可能|特性|
|PSDNET-49|在图层中添加填充不透明度属性的呈现。|特性|
|PSDNET-43|实现曲线调整图层的呈现|特性|
|PSDNET-42|添加对曲线调整图层的支持|特性|
|PSDNET-41|实现级别调整图层的呈现|特性|
|PSDNET-40|添加级别调整图层支持|特性|
|PSDNET-37|添加通道混合器调整图层支持|特性|
|PSDNET-35|添加色相/饱和度调整图层的支持|特性|
|PSDNET-34|为导出实现曝光调整图层呈现。|特性|
|PSDNET-31|添加支持导出渠道Mixer调整图层的呈现|特性|
|PSDNET-26|添加剪贴蒙版支持|特性|
|PSDNET-13|添加图层蒙版支持|特性|
|PSDNET-9|添加照片滤镜调整图层支持|特性|
|PSDNET-8|添加通道混合器调整图层支持|特性|
|PSDNET-7|添加曝光调整图层支持|特性|
|PSDNET-6|添加亮度/对比度调整图层支持|特性|
|PSDNET-5|部分支持调整图层|特性|
|PSDNET-3|添加PSD NoBreak文本选项支持|特性|
|PSDNET-2|运行时添加文本图层的能力|特性|
|PSDNET-62|TIFF编解码器无法保存16位通道图像|增强功能|
|PSDNET-61|保存PSD图像会产生颜色无效的问题|增强功能|
|PSDNET-60|更新时左上角的坐标不正确|增强功能|
|PSDNET-59|更新文本图层时出现异常|增强功能|
|PSDNET-58|将JPEG2000图像的编解码器属性公开|增强功能|
|PSDNET-57|修复导出到BMP的24bpp选项设置|增强功能|
|PSDNET-46|CMYK PSD转换为TIFF或JPG时调整图层被忽略|增强功能|

## **使用示例：**
**PSDNET-68 支持LayerCreationDateTime属性**

{{< highlight java >}}

 // 使用LayerCreationDateTime属性的示例

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // 检查新创建的图层是否更新了创建日期时间

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 支持SheetColor Highlighting**

{{< highlight java >}}

 // 使用SheetColorHighlight属性的示例

string sourceFileName = "SheetColorHighlightExample.psd";

string exportPath = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, layer1.SheetColorHighlight);

    var layer2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, layer2.SheetColorHighlight);

    layer1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-66 能够合并层之间的图层**

{{< highlight java >}}

 // 合并两个图层的示例

var sourceFile1 = "FillOpacitySample.psd";

var sourceFile2 = "ThreeRegularLayersSemiTransparent.psd";

var exportPath = "MergedLayersFromTwoDifferentPsd.psd" 

using (var im1 = (PsdImage)(Image.Load(sourceFile1)))

{

    var layer1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(sourceFile2)))

    {

        var layer2 = im2.Layers[0];

        layer1.MergeLayerTo(layer2);

	im2.Save(exportPath);	

    }

}

{{< /highlight >}}

**PSDNET-65 部分支持文本图层BoundBox属性**

{{< highlight java >}}

 // TextBox示例

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // 图层大小为渲染区域的大小

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox是文本图层的最大尺寸。

    // 在此区域内，PS将尝试适应您的文本

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 对IopaResource的支持**

{{< highlight java >}}

 // 通过IopaResource更改填充不透明度属性

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    var resources = layer.Resources;

    foreach (var resource in resources)

    {

        if (resource is IopaResource)

        {

            var iopaResource = (IopaResource)resource;

            iopaResource.FillOpacity = 200;

        }

    }

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-56 支持PSD格式的图层效果**

{{< highlight java >}}

 using (

    PsdImage image =

        (PsdImage)

        Aspose.PSD.Image.Load(

            sourceFileName,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                output,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 .Net的InterruptMonitor支持**

{{< highlight java >}}

         public void InterruptMonitorTest(string dir, string ouputDir)

        {

            ImageOptionsBase saveOptions = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dir + "big.psb", dir + "big_out.png", saveOptions, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // 超时时间应小于完整图像转换所需的时间（未中断）。

                System.Threading.Thread.Sleep(3000);

                // 中断过程

                monitor.Interrupt();

                System.Console.WriteLine("中断保存线程 #{0} 在 {1}", thread.ManagedThreadId, System.DateTime.Now);

                // 等待中断...

                thread.Join();

            }

            finally

            {

                // 如果要删除的文件不存在，将不会引发任何异常。

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// 启动图像转换并等待中断。

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// 输入图像的路径。

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// 输出图像的路径。

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// 中断监视器。

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// 保存选项。

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// 初始化 <see cref="SaveImageWorker" /> 类的新实例。

            /// </summary>

            /// <param name="inputPath">输入图像的路径。</param>

            /// <param name="outputPath">输出图像的路径。</param>

            /// <param name="saveOptions">保存选项。</param>

            /// <param name="monitor">中断监视器。</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// 尝试将图像从一种格式转换为另一种。 处理中断。

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("预期中断。");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("保存线程 #{0} 在 {1} 完成", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 使图层展平成为可能**

{{< highlight java >}}

 // 整合整个PSD

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// 将一个图层合并到另一个图层

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // 设置合并后的图层

    im.Layers = new Layer[] { layer2 };

    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 在图层中添加填充不透明度属性的呈现。**

{{< highlight java >}}

 // 更改填充不透明度属性

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 实现曲线调整图层的呈现**

{{< highlight java >}}

 // 曲线层编辑

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

string pngExportPath = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

        foreach (var layer in im.Layers)

	{

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }

    // 保存PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

    // 保存PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 添加对曲线调整图层的支持**

{{< highlight java >}}

 // 曲线层编辑

string sourceFileName = "CurvesAdjustmentLayer";

string psdPathAfterChange = "CurvesAdjustmentLayerChanged";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(sourceFileName + j.ToString() + ".psd"))

    {

         foreach (var layer in im.Layers)

	 {

            if (layer is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)layer;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var manager = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var manager = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      manager.AddCurvePoint(0, 50, 100);

                      manager.AddCurvePoint(0, 150, 130);

                 }

            }

	}

    }

    // 保存PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}

**PSDNET-41 实现级别调整图层的呈现**

{{< highlight java >}}

 // 级别层编辑

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

string pngExportPath = "LevelsAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }

    // 保存PSD

    im.Save(psdPathAfterChange);



    // 保存PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 添加级别调整图层支持**

{{< highlight java >}}

 // 级别层编辑

string sourceFileName = "LevelsAdjustmentLayer.psd";

string psdPathAfterChange = "LevelsAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is LevelsLayer)

        {

            var levelsLayer = (LevelsLayer)layer;

            var channel = levelsLayer.GetChannel(0);

            channel.InputMidtoneLevel = 2.0f;

            channel.InputShadowLevel = 10;

            channel.InputHighlightLevel = 230;

            channel.OutputShadowLevel = 20;

            channel.OutputHighlightLevel = 200;

        }

    }

    // 保存PSD

    im.Save{{< /highlight >}}

**PSDNET-37 添加通道混合器调整图层支持**

{{< highlight java >}}

// RGB通道混合器

string sourceFileName = "ChannelMixerAdjustmentLayerRgb.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerRgbChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is RgbChannelMixerLayer)

        {

            var rgbLayer = (RgbChannelMixerLayer)layer;

            rgbLayer.RedChannel.Blue = 100;

            rgbLayer.BlueChannel.Green = -100;

            rgbLayer.GreenChannel.Constant = 50;

        }

    }

    im.Save(psdPathAfterChange);

}

// CMYK通道混合器

string sourceFileName = "ChannelMixerAdjustmentLayerCmyk.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is CmykChannelMixerLayer)

        {

            var cmykLayer = (CmykChannelMixerLayer)layer;

            cmykLayer.CyanChannel.Black = 20;

            cmykLayer.MagentaChannel.Yellow = 50;

            cmykLayer.YellowChannel.Cyan = -25;

            cmykLayer.BlackChannel.Yellow = 25;

        }

    }

    im.Save(psdPathAfterChange);

}

// 为此示例添加新图层（Cmyk）

string sourceFileName = "CmykWithAlpha.psd";

string psdPathAfterChange = "ChannelMixerAdjustmentLayerCmykChanged.psd";

using (var im = LoadFile(sourceFileName))

{

    var newlayer = im.AddChannelMixerAdjustmentLayer();

    newlayer.GetChannelByIndex(2).Constant = 50;

    newlayer.GetChannelByIndex(0).Constant = 50;

    im.Save(psdPathAfterChange);

}		

{{< /highlight >}}

**PSDNET-35 添加色相/饱和度调整图层的支持**

{{< highlight java >}}

 // 色相/饱和度图层编辑

string sourceFileName = "HueSaturationAdjustmentLayer.psd";

string psdPathAfterChange = "HueSaturationAdjustmentLayerChanged.psd";

using (var im = LoadFile(sourceFileName))

{

     foreach (var layer in im.Layers)

     {

           if (layer is HueSaturationLayer)

           {

                var hueLayer = (HueSaturationLayer)layer;

                hueLayer.Hue = -25;

                hueLayer.Saturation = -12;

                hueLayer.Lightness = 67;

                var colorRange = hueLayer.GetRange(2);

                colorRange.Hue = -40;

                colorRange.Saturation = 50;

                colorRange.Lightness = -20;

                colorRange.MostLeftBorder = 300;

           }

      }

      im.Save(psdPathAfterChange);

}



// 添加色相/饱和度图层

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedHueSaturation.psd";



using (PsdImage im = LoadFile(sourceFileName))

{

     this.SaveForVisualTest(im, this.OutputPath, prefix + file, "before");

     var hueLayer = im.AddHueSaturationAdjustmentLayer();

     hueLayer.Hue = -25;

     hueLayer.Saturation = -12;

     hueLayer.Lightness = 67;

     var colorRange = hueLayer.GetRange(2);

     colorRange.Hue = -160;

     colorRange.Saturation = 100;

     colorRange.Lightness = 20;

     colorRange.MostLeftBorder = 300;



     im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-34 为导出实现曝光调整图层呈现。**

{{< highlight java >}}

 // 曝光图层编辑

string sourceFileName = "ExposureAdjustmentLayer.psd";

string psdPathAfterChange = "ExposureAdjustmentLayerChanged.psd";

string pngExportPath = "ExposureAdjustmentLayerChanged.png";

using (var im = LoadFile(sourceFileName))

{

    foreach (var layer in im.Layers)

    {

        if (layer is ExposureLayer)

        {

        var expLayer = (ExposureLayer)layer;

            expLayer.Exposure = 2;

            expLayer.Offset = -0.25f;

            expLayer.GammaCorrection = 0.5f;

        }

    }

    // 保存PSD

    im.Save(psdPathAfterChange);



    // 保存PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}



// 曝光图层添加

string sourceFileName = "PhotoExample.psd";

string psdPathAfterChange = "PhotoExampleAddedExposure.psd";

string pngExportPath = "PhotoExampleAddedExposure.png";



using (PsdImage im = LoadFile(sourceFileName))

{

    var newlayer = im.AddExposureAdjustmentLayer();

    newlayer.Exposure = 2;

    newlayer.Offset = -0.25f;

    newlayer.GammaCorrection = 2f;



    // 保存PSD

    im.Save(psdPathAfterChange);



    // 保存PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}
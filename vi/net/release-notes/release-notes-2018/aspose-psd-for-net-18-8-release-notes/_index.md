---
title: Aspose.PSD cho .NET 18.8 - Ghi chú phát hành
type: docs
weight: 50
url: /vi/net/aspose-psd-cho-net-18-8-ghi-chu-phat-hanh/
---

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-68|Hỗ trợ thuộc tính LayerCreationDateTime.|Tính năng|
|PSDNET-67|Hỗ trợ SheetColor Highlighting|Tính năng|
|PSDNET-66|Khả năng kết hợp các layer với nhau|Tính năng|
|PSDNET-65|Thêm hỗ trợ một phần cho thuộc tính Text Layer BoundBox|Tính năng|
|PSDNET-64|Thêm hỗ trợ IopaResource|Tính năng|
|PSDNET-56|Hỗ trợ Layer Effects cho định dạng PSD|Tính năng|
|PSDNET-55|Hỗ trợ InterruptMonitor cho .Net|Tính năng|
|PSDNET-50|Tạo khả năng làm phẳng các layer|Tính năng|
|PSDNET-49|Thêm việc hiển thị thuộc tính fill opacity trong các layer.|Tính năng|
|PSDNET-43|Thực hiện khả năng hiển thị Curves Adjustment Layer|Tính năng|
|PSDNET-42|Thêm hỗ trợ Curves Adjustment Layer|Tính năng|
|PSDNET-41|Thực hiện khả năng hiển thị Levels Adjustment Layer|Tính năng|
|PSDNET-40|Thêm hỗ trợ Levels adjustment Layer|Tính năng|
|PSDNET-37|Thêm hỗ trợ Channel Mixer Adjustment Layer|Tính năng|
|PSDNET-35|Thêm hỗ trợ Hue/Saturation Adjustment Layer|Tính năng|
|PSDNET-34|Thực hiện Exposure Adjustment Layer để xuất file.|Tính năng|
|PSDNET-31|Thêm hỗ trợ hiển thị khi xuất Layer Adjustment của ChannelMixer|Tính năng|
|PSDNET-26|Thêm hỗ trợ Clipping mask|Tính năng|
|PSDNET-13|Thêm hỗ trợ layer mask|Tính năng|
|PSDNET-9|Thêm hỗ trợ Photo Filter adjustment layer|Tính năng|
|PSDNET-8|Thêm hỗ trợ Channel mixer adjustment layer|Tính năng|
|PSDNET-7|Thêm hỗ trợ Exposure adjustment layer|Tính năng|
|PSDNET-6|Thêm hỗ trợ Brightness/Contrast adjustment layer|Tính năng|
|PSDNET-5|Thêm hỗ trợ một phần cho các layer điều chỉnh|Tính năng|
|PSDNET-3|Thêm hỗ trợ cho tùy chọn văn bản NoBreak của PSD|Tính năng|
|PSDNET-2|Khả năng thêm Text Layer trong thời gian chạy|Tính năng|
|PSDNET-62|Codec TIFF không thể lưu hình ảnh kênh 16 bit|Cải tiến|
|PSDNET-61|Lưu hình ảnh PSD tạo ra màu không hợp lệ|Cải tiến|
|PSDNET-60|Tọa độ của góc trên trái không chính xác khi cập nhật|Cải tiến|
|PSDNET-59|Ngoại lệ khi cập nhật các layer văn bản|Cải tiến|
|PSDNET-58|Trội ra thuộc tính Codec của hình ảnh JPEG2000 cho người dùng|Cải tiến|
|PSDNET-57|Sửa tùy chọn 24bpp cho xuất sang BMP|Cải tiến|
|PSDNET-46|Layer Adjustment bị bỏ qua khi chuyển đổi PSD CMYK sang TIFF hoặc JPG|Cải tiến|

## **Ví dụ sử dụng:**
**PSDNET-68 Hỗ trợ thuộc tính LayerCreationDateTime**

{{< highlight java >}}

 // Ví dụ về thuộc tính LayerCreationDateTime

string sourceFileName = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[0];

    var creationDateTime = layer.LayerCreationDateTime;

    var expectedDateTime = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(expectedDateTime, creationDateTime);

    var now = DateTime.Now;

    var createdLayer = im.AddLevelsAdjustmentLayer();

    // Check if Creation Date Time Updated on newly created layers

    Assert.True(now <= createdLayer.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 Hỗ trợ SheetColor Highlighting**

{{< highlight java >}}

 // Ví dụ sử dụng của thuộc tính SheetColorHighlight

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

**PSDNET-66 Khả năng kết hợp các layer với nhau**

{{< highlight java >}}

 // Ví dụ gộp hai layer

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

**PSDNET-65 Thêm hỗ trợ một phần cho thuộc tính Text Layer BoundBox**

{{< highlight java >}}

 // Ví dụ về Text BoxBounds

string sourceFileName = "LayerWithText.psd";

var correctOpticalSize = new Size(127, 45);

var correctBoundBox = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var textLayer = (TextLayer)im.Layers[1];

    // Kích thước của layer là kích thước của khu vực hiển thị

    var opticalSize = textLayer.Size;

    Assert.AreEqual(correctOpticalSize, opticalSize);

    // TextBoundBox là kích thước tối đa của layer cho Text Layer. 

    // Trong khu vực này, PS sẽ cố gắng vừa văn bản của bạn

    var boundBox = textLayer.TextBoundBox;

    Assert.AreEqual(correctBoundBox, boundBox);

}

{{< /highlight >}}

**PSDNET-64 Thêm hỗ trợ cho IopaResource**

{{< highlight java >}}

 // Thay đổi thuộc tính Fill Opacity thông qua việc thay đổi IopaResource

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

**PSDNET-56 Hỗ trợ Layer Effects cho định dạng PSD**

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

**PSDNET-55 Hỗ trợ InterruptMonitor cho .Net**

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

                // Thời gian chờ nên nhỏ hơn thời gian cần thiết cho việc chuyển đổi hình ảnh đầy đủ (không bị gián đoạn).

                System.Threading.Thread.Sleep(3000);

                // Gián đoạn không quá trình

                monitor.Interrupt();

                System.Console.WriteLine("Interrupting the save thread #{0} at {1}", thread.ManagedThreadId, System.DateTime.Now);

                // Chờ gián đoạn...

                thread.Join();

            }

            finally

            {

                // Nếu tệp cần xóa không tồn tại, sẽ không có ngoại lệ nào được ném.

                System.IO.File.Delete(dir + "big_out.png");

            }

        }

        /// <summary>

        /// Bắt đầu chuyển đổi hình ảnh và đợi sự gián đoạn của nó.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Đường dẫn đến hình ảnh đầu vào.

            /// </summary>

            private readonly string inputPath;

            /// <summary>

            /// Đường dẫn đến hình ảnh đầu ra.

            /// </summary>

            private readonly string outputPath;

            /// <summary>

            /// Ngăn chặn giám sát.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Các tùy chọn lưu.

            /// </summary>

            private readonly ImageOptionsBase saveOptions;

            /// <summary>

            /// Khởi tạo một trường hợp mới của lớp `SaveImageWorker`.

            /// </summary>

            /// <param name="inputPath">Đường dẫn đến hình ảnh đầu vào.</param>

            /// <param name="outputPath">Đường dẫn đến hình ảnh đầu ra.</param>

            /// <param name="saveOptions">Các tùy chọn lưu.</param>

            /// <param name="monitor">Ngăn chặn giám sát.</param>

            public SaveImageWorker(string inputPath, string outputPath, ImageOptionsBase saveOptions, Multithreading.InterruptMonitor monitor)

            {

                this.inputPath = inputPath;

                this.outputPath = outputPath;

                this.saveOptions = saveOptions;

                this.monitor = monitor;

            }

            /// <summary>

            /// Thử chuyển đổi hình ảnh từ một định dạng sang một định dạng khác. Xử lý gián đoạn. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.inputPath))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.outputPath, this.saveOptions);

                        Assert.Fail("Expected interruption.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("The save thread #{0} finishes at {1}", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

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

**PSDNET-50 Tạo khả năng làm phẳng các layer**

{{< highlight java >}}

 // Làm phẳng toàn bộ PSD

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattened.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    im.FlattenImage();

    im.Save(exportPath);	 

}

// Gộp một layer vào một layer khác

string sourceFileName = "ThreeRegularLayersSemiTransparent.psd";

string exportPath = "ThreeRegularLayersSemiTransparentFlattenedLayerByLayer.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var bottomLayer = im.Layers[0];

    var middleLayer = im.Layers[1];

    var topLayer = im.Layers[2];

    var layer1 = im.MergeLayers(bottomLayer, middleLayer);

    var layer2 = im.MergeLayers(layer1, topLayer);

    // Cài đặt các layers sau khi gộp

    im.Layers = new Layer[] { layer2 };



    im.Save(exportPath);	 

}

{{< /highlight >}}

**PSDNET-49 Thêm việc hiển thị thuộc tính fill opacity trong các layer.**

{{< highlight java >}}

 // Thay đổi thuộc tính Fill Opacity

string sourceFileName = "FillOpacitySample.psd";

string exportPath = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(sourceFileName)))

{

    var layer = im.Layers[2];

    layer.FillOpacity = 5;

    im.Save(exportPath);	

}

{{< /highlight >}}

**PSDNET-43 Thực hiện khả năng hiển thị Curves Adjustment Layer**

{{< highlight java >}}

 // Chỉnh sửa layer Curves

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

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

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



    // Lưu PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");



    // Lưu PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath + j.ToString() + ".png", saveOptions);

}

{{< /highlight >}}

**PSDNET-42 Thêm hỗ trợ Curves Adjustment Layer**

{{< highlight java >}}

 // Chỉnh sửa layer Curves

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

                           manager.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2)));

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



    // Lưu PSD

    im.Save(psdPathAfterChange + j.ToString() + ".psd");

}

{{< /highlight >}}**PSDNET-41 Thực hiện khả năng hiển thị Levels Adjustment Layer**

{{< highlight java >}}

 // Chỉnh sửa layer Levels

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



    // Lưu PSD

    im.Save(psdPathAfterChange);



    // Lưu PNG

    var saveOptions = new PngOptions();

    saveOptions.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngExportPath, saveOptions);

}

{{< /highlight >}}

**PSDNET-40 Thêm hỗ trợ Levels adjustment Layer**

{{< highlight java >}}

 // Chỉnh sửa layer Levels

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



    // Lưu PSD

    im.Save(psdPathAfterChange);

}

{{< /highlight >}}

**PSDNET-37 Thêm hỗ trợ Channel Mixer Adjustment Layer**

{{< highlight java >}}



// Channel Mixer Rgb

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

// Channel Mixer Cmyk

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



// Thêm layer mới (Cmyk trong ví dụ này)

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

**PSDNET-35 Thêm hỗ trợ Hue/Saturation Adjustment Layer**

{{< highlight java >}}

 // Chỉnh sửa layer Hue/Saturation

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



// Thêm layer Hue/Saturation

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
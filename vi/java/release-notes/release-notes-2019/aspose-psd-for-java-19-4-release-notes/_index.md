---
title: Ghi chú phát hành Aspose.PSD cho Java 19.4
type: docs
weight: 20
url: /vi/java/aspose-psd-cho-java-19-4-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú phát hành cho Aspose.PSD cho Java 19.4

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDJAVA-1|Làm tính năng để tải tệp hình ảnh JPEG/PNG/v.v vào PsdImage mà không cần tải trực tiếp (Điều này không được hỗ trợ trong Aspose.PSD)|Tính năng|
|PSDJAVA-2|Hỗ trợ Chế độ màu RGB với 16 bit/kanal (64 bit mỗi màu)|Tính năng|
|PSDJAVA-3|Hỗ trợ Maske Vector Lớp và Lớp Văn bản Tùy chỉnh FlipRotate|Tính năng|
|PSDJAVA-4|Tất cả các ký tự châu Á không được hiển thị đúng cách|Lỗi|
|PSDJAVA-5|Các ký hiệu \r\n được hiểu là xuống dòng kép, điều đó là không đúng|Lỗi|
|PSDJAVA-6|Nếu TextLayer được cập nhật bằng chuỗi chứa các LineBreaks thì File PSD trở thành không đọc được|Lỗi|
|PSDJAVA-7|Nếu TextLayer được cập nhật bằng chuỗi chứa các ký hiệu Tab, quá trình xử lý sẽ thất bại với ngoại lệ|Lỗi|
# **Thay đổi API công cộng**
# **APIs được thêm:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **APIs được loại bỏ:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsPaletteSorted
- P:Aspose.PSD.FileFormats.Gif.GifImage.PaletteColorResolutionBits
- P:Aspose.PSD.FileFormats.Gif.GifImage.Width
- P:Aspose.PSD.FileFormats.Gif.GifImage.Height
- P:Aspose.PSD.FileFormats.Gif.GifImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Gif.GifImage.Blocks
- P:Aspose.PSD.FileFormats.Gif.GifImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.BackgroundColorIndex
- P:Aspose.PSD.FileFormats.Gif.GifImage.PixelAspectRatio
- P:Aspose.PSD.FileFormats.Gif.GifImage.IsCached
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.TransparentColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasBackgroundColor
- P:Aspose.PSD.FileFormats.Gif.GifImage.ImageOpacity
- M:Aspose.PSD.FileFormats.Gif.GifImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.CacheData
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.OrderBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.ClearBlocks
- M:Aspose.PSD.FileFormats.Gif.GifImage.InsertBlock(System.Int32,Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AddBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RemoveBlock(Aspose.PSD.FileFormats.Gif.IGifBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Grayscale
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Gif.GifImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Gif.GifImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Gif.GifImage.ReplaceNonTransparentColors(System.Int32)
- T:Aspose.PSD.FileFormats.Tiff.TiffImage
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.#ctor(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double,System.Int32)
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasAlpha
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HasTransparentColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.FileFormat
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.PremultiplyComponents
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ByteOrder
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.HorizontalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.VerticalResolution
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BackgroundColor
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.BitsPerPixel
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ActiveFrame
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Frames
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Height
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.Width
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.IsCached
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ExifData
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.ImageOpacity
- P:Aspose.PSD.FileFormats.Tiff.TiffImage.XmpData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AlignResolutions
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Dither(Aspose.PSD.DitheringMethod,System.Int32,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.SetResolution(System.Double,System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.CacheData
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlip(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RotateFlipAll(Aspose.PSD.RotateFlipType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Rotate(System.Single,System.Boolean,Aspose.PSD.Color)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Add(Aspose.PSD.FileFormats.Tiff.TiffImage)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AddFrames(Aspose.PSD.FileFormats.Tiff.TiffFrame[])
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.InsertFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.RemoveFrame(Aspose.PSD.FileFormats.Tiff.TiffFrame)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Resize(System.Int32,System.Int32,Aspose.PSD.ImageResizeSettings)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeWidthProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeHeightProportionally(System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ResizeProportional(System.Int32,System.Int32,Aspose.PSD.ResizeType)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Grayscale
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeFixed(System.Byte)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeOtsu
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.BinarizeBradley(System.Double)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Crop(System.Int32,System.Int32,System.Int32,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustBrightness(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustContrast(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single,System.Single,System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.AdjustGamma(System.Single)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.Filter(Aspose.PSD.Rectangle,Aspose.PSD.ImageFilters.FilterOptions.FilterOptionsBase)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceColor(System.Int32,System.Byte,System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceNonTransparentColors(System.Int32)
- M:Aspose.PSD.FileFormats.Tiff.TiffImage.ReplaceFrame(System.Int32,Aspose.PSD.FileFormats.Tiff.TiffFrame)
# **Ví dụ về việc sử dụng:**

**PSDJAVA-1. Tạo tính năng tải tệp hình ảnh JPEG/PNG/v.v vào PsdImage mà không cần tải trực tiếp (Điều này không được hỗ trợ trong Aspose.PSD)**

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

**PSDJAVA-2. Hỗ trợ chế độ màu RGB với 16 bit/kanal (64 bit mỗi màu)**

{{< highlight java >}}

  // Hỗ trợ chế độ màu RGB với 16 bit/kanal (64 bit mỗi màu)

        String sourceFileName = "inRgb16.psd.psd";

        String outputFilePathJpg = "outRgb16.jpg";

        String outputFilePathPsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(sourceFileName, options);

        try

        {

            PsdOptions psdOpt = new PsdOptions(image);

            image.save(outputFilePathPsd, psdOpt);



            JpegOptions jpegOpt = new JpegOptions();

            jpegOpt.setQuality(100);

            image.save(outputFilePathJpg);

        }

        finally 

        {

             image.dispose();

        }

    // Các tệp phải được mở mà không có ngoại lệ và phải đọc được bởi Photoshop    

   image = Image.load(outputFilePathPsd));

   image.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Hỗ trợ của Maske Vector Lớp và Lớp Văn bản Tùy chỉnh FlipRotate**

{{< highlight java >}}

 // Thao tác RotateFlip không hoạt động như mong đợi với PSD

    String sourceFile = "1.psd";

    String pngPath = "RotateFlipTest2617.png";

    String psdPath = "RotateFlipTest2617.psd";

    int flipType = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(sourceFile));



    try

    {

        im.rotateFlip(flipType);

        PngOptions options = new PngOptions();

        options.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(pngPath, options);

        im.save(psdPath);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Tất cả các ký tự châu Á không được hiển thị đúng cách**

[**Vui lòng kiểm tra ví dụ đính kèm**](attachments/92602686/92766213.java)

**PSDJAVA-5. Các ký hiệu \r\n được hiểu là xuống dòng kép, điều đó là không đúng**

{{< highlight java >}}

 // \r\n được hiểu là xuống dòng kép, điều đó không chính xác

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";



            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("Đoạn văn thứ nhất\r\nĐoạn văn thứ hai\rThứ ba\rĐoạn văn thứ tư");

                image.save(exportPath, imageOptions);

                // Hình ảnh tạo ra phải đọc được bởi Aspose.PSD/Aspose.Imaging và bởi Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();

            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Nếu TextLayer được cập nhật bằng chuỗi chứa các LineBreaks thì File PSD trở thành không đọc được**

{{< highlight java >}}

 // Nếu TextLayer được cập nhật bằng chuỗi chứa LineBreaks thì File PSD trở thành không đọc được.

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";



            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("Đoạn văn thứ nhất\r\nĐoạn văn thứ hai\r\nThứ ba\r\nĐoạn văn thứ tư");

                image.save(exportPath, imageOptions);

                // Hình ảnh tạo ra
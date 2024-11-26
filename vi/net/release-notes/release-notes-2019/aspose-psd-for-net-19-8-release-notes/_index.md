---
title: Aspose.PSD cho .NET 19.8 - Ghi chú bản phát hành
type: docs
weight: 50
url: /vi/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho Aspose.PSD cho .NET 19.8

{{% /alert %}} 

|**Key**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-184|Tải các tệp hình ảnh JPEG, PNG và khác vào PsdImage từ luồng|Tính năng|
|PSDNET-134|Triển khai hiển thị Lớp Fill: Điều chuyển màu|Tính năng|
|PSDNET-166|Lưu PSD dưới dạng PDF không cung cấp văn bản có thể chọn|Tính năng|
|PSDNET-158|Hỗ trợ lưu PSB dưới dạng PDF|Tính năng|
|PSDNET-189|Sử dụng bộ nhớ cao khi tải PSD với Chế độ Mở chỉ đọc|Tính năng cải thiện|
|PSDNET-171|Sau khi tạo Lớp Văn bản mới, tệp PSD trở nên không thể đọc được đối với PS|Lỗi|
|PSDNET-156|Ngoại lệ khi tải PSD|Lỗi|

## **Thay đổi API công cộng**
# **API được thêm vào:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **API được loại bỏ:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Ví dụ về cách sử dụng:**
**PSDNET-184. Tải tệp hình ảnh JPEG, PNG và khác vào PsdImage từ luồng**

{{< highlight java >}}

    // Tải các tệp hình ảnh JPEG, PNG và khác vào PsdImage từ luồng

    string outputFilePath = "Kết quả.psd";

    var filesList = new string[]

    {

        "Ví dụ Psd.psd",

        "Ví dụ Bmp.bmp",

        "Ví dụ Gif.gif",

        "Ví dụ Jpeg2000.jpf",

        "Ví dụ Jpeg.jpg",

        "Ví dụ Png.png",

        "Ví dụ Tiff.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Triển khai hiển thị Lớp Fill: Điều chuyển màu**

{{< highlight java >}}

             // Triển khai hiển thị Lớp Fill: Điều chuyển màu

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. Lưu PSD dưới dạng PDF không cung cấp văn bản có thể chọn**

{{< highlight java >}}

  // Lưu PSD dưới dạng PDF không cung cấp văn bản có thể chọn

    string sourceFileName = "văn bản.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "văn bản.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Sau khi tạo Lớp Văn bản mới, tệp PSD trở nên không thể đọc được đối với PS**

{{< highlight java >}}

 // Sau khi tạo Lớp Văn bản mới trên Máy chủ Xây dựng, Tệp PSD trở nên không thể đọc được cho PS

    string sourceFileName = "Một lớp.psd";

    string outFileName = "Một lớp với Văn bản được thêm vào.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Một số văn bản", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Ngoại lệ khi tải PSD**

{{< highlight java >}}

 using (var image = Image.Load("Khác.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Sử dụng bộ nhớ cao khi tải PSD với Chế độ Mở chỉ đọc**

{{< highlight java >}}

 // Sử dụng bộ nhớ cao của Aspose.PSD khi tải PSD với Chế độ Mở chỉ đọc

            string sourceFileName = "Văn bản Hiệu ứng Sáng Chữ 3D.psd";

            string outFileName = "Xuất ra.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Sử dụng bộ nhớ phải nhỏ hơn 100 MB cho các ví dụ này

            if (memoryUsed > 100)

            {

                throw new Exception("Sử dụng bộ nhớ quá lớn");

            }

{{< /highlight >}}

**PSDNET-158. Hỗ trợ lưu PSB dưới dạng PDF**

{{< highlight java >}}

 // Hỗ trợ lưu PSB dưới dạng PDF

    string sourceFileName = "mẫu.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "mẫu.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

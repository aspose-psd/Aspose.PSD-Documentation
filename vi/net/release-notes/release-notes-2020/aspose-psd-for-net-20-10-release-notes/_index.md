---
title: Ghi chú phát hành Aspose.PSD cho .NET 20.10
type: tài_liệu
weight: 30
url: /vi/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-565|Ngoại lệ khi lưu tệp PSD cụ thể với lớp văn bản|Lỗi|
|PSDNET-680|Mất font sau các lượt với Aspose.PSD|Lỗi|
|PSDNET-704|Hiển thị lớp Đối tượng Thông minh|Tính năng|
|PSDNET-707|Hỗ trợ biến đổi phi hủy Đối tượng Thông minh|Tính năng|
|PSDNET-711|Lớp Văn bản bị di chuyển sau khi lưu mà không thay đổi gì|Lỗi|
|PSDNET-720|Aspose.PSD 20.8: Ngoại lệ chuyển đổi Psd sang Tiff|Lỗi|

## **Thay đổi API công khai**
# **API được thêm:**
- Không có
# **API bị xóa:**
- Không có

## **Ví dụ sử dụng:**
**PSDNET-565. Ngoại lệ khi lưu tệp PSD cụ thể với lớp văn bản**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-680. Mất font sau các lượt với Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("Các giá trị không bằng nhau.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-704. Hiển thị lớp Đối tượng Thông minh**
{{< highlight csharp >}}
            // Ví dụ này mô tả cách thay thế nội dung của lớp đối tượng thông minh Adobe® Photoshop® và hiển thị chính xác nó.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Ví dụ này mô tả cách cập nhật bộ đệm hình ảnh của các lớp đối tượng thông minh Adobe® Photoshop® và hiển thị chính xác chúng.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}

**PSDNET-707. Hỗ trợ biến đổi phi hủy Đối tượng Thông minh**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Những ví dụ này mô tả các biến đổi không phá hoại của tập tin PSD với SmartObjectLayer.
            // Chúng ta có thể thay đổi tỉ lệ, xoay, bẻ cong, biến đổi góc nhìn, hoặc uốn cong một lớp mà không
            // mất dữ liệu hoặc chất lượng ảnh gốc vì các biến đổi không ảnh hưởng đến dữ liệu gốc.

            // Ví dụ này mô tả cách thay đổi kích thước ảnh Adobe® Photoshop® với các lớp đối tượng thông minh:
            ExampleOfSmartObjectImageResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectImageResizeSupport("picture-frame-4-linked3");
            ExampleOfSmartObjectImageResizeSupport("gorilla");

            // Ví dụ này mô tả cách thay đổi kích thước tệp PSD với các lớp đối tượng thông minh.
            void ExampleOfSmartObjectImageResizeSupport(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Ví dụ này mô tả cách thay đổi kích thước lớp đối tượng thông minh của Adobe® Photoshop®.
            ExampleOfSmartObjectLayerResizeSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerResizeSupport("gorilla");

            // Ví dụ này mô tả cách thay đổi kích thước lớp đối tượng thông minh trong tệp PSD.
            void ExampleOfSmartObjectLayerResizeSupport(string fileName)
            {
                const double scale = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int newWidth = (int)(smartObjectLayer.Width * scale);
                    int newHeight = (int)(smartObjectLayer.Height * scale);
                    smartObjectLayer.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Ví dụ này mô tả cách cắt lớp đối tượng thông minh của Adobe® Photoshop®.
            ExampleOfSmartObjectLayerCropSupport("new_panama-papers-8-trans4-linked");
            ExampleOfSmartObjectLayerCropSupport("gorilla");

            // Ví dụ này mô tả cách cắt một lớp đối tượng thông minh trong tệp PSD.
            void ExampleOfSmartObjectLayerCropSupport(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CropLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "CropLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            ...

{{< /highlight >}}

**PSDNET-711. Lớp Văn bản bị di chuyển sau khi lưu mà không thay đổi gì**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("Các giá trị bằng nhau.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual(txtLayer.Top, txtLayer.TransformMatrix[5]);
            }
{{< /highlight >}}

**PSDNET-720. Aspose.PSD 20.8: Ngoại lệ chuyển đổi Psd sang Tiff**
{{< highlight csharp >}}
            using (var psdImage = (PsdImage)Image.Load("sarbarg.fin12.psd"))
            {
                psdImage.Save("result.tiff", new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
            }
{{< /highlight >}}
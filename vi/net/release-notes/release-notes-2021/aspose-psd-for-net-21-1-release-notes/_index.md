---
title: Aspose.PSD cho .NET 21.1 - Ghi chú phát hành
type: docs
weight: 120
url: /vi/net/aspose-psd-cho-net-21-1-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Thể loại**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Ngoại lệ khi cố gắng chuyển đổi tệp Psd cụ thể thành png|Lỗi|
|PSDNET-792|Ngoại lệ khi lưu PSD chứa đối tượng thông minh sang PNG|Lỗi|

## **Thay đổi API công cộng**
# **API được thêm vào:**
- Không có

# **API bị loại bỏ:**
- Không có

## **Ví dụ về việc sử dụng:**
**PSDNET-766. Aspose.PSD 20.10: Ngoại lệ khi cố gắng chuyển đổi tệp Psd cụ thể thành png**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Ngoại lệ khi lưu PSD chứa đối tượng thông minh sang PNG**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // Tìm Đối tượng Thông minh
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // Chúng ta đang tải Lớp Đối tượng Thông minh từ Memory Stream,
                        // Nhưng chúng ta có thể sử dụng smart.ExportContents(somePath) để xuất đối tượng thông minh ra tệp
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)
                                {
                                    // Tìm Lớp Văn bản
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        // Chúng ta có thể sử dụng cập nhật văn bản đơn giản, nhưng cách này giúp chúng tôi có khả năng chỉnh sửa văn bản theo từng phần
                                        // Tạo các lớp văn bản nhiều dòng và các tính năng định dạng văn bản và đoạn văn khác
                                        // Xin hãy cẩn thận. Nếu Nội dung Đối tượng Thông minh không phải là PSD, bạn không thể sử dụng cách này để chỉnh sửa văn bản
                                        // Trong trường hợp đó, bạn nên sử dụng API Đồ họa: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "Tốt nhất";

                                        // Bạn nên thay đổi kích thước của văn bản nếu muốn hình ảnh trở nên tốt hơn.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // Tốt hơn nếu sử dụng ReplaceContents. Nó sẽ tự động vẽ lại Đối tượng Thông minh
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // Theo cách này, chúng ta đang lưu Tệp PSD đã thay đổi
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

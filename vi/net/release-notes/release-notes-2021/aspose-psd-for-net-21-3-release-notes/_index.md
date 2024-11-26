---
title: Aspose.PSD cho .NET 21.3 - Ghi chú bản phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-cho-net-21-3-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú bản phát hành cho [Aspose.PSD cho .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-823|Thêm SectionDividerLayer để cải thiện trải nghiệm với các nhóm lớp|Nâng cấp|
|PSDNET-694|Khi đọc PattResource, chiều rộng và chiều cao đã được hoán đổi|Lỗi|
|PSDNET-789|Hợp nhất không chính xác của nhiều Layer Effect|Lỗi|
|PSDNET-805|Thứ tự và logic Hợp nhất không chính xác khi có nhiều Layer Effect|Lỗi|
|PSDNET-842|Các thuộc tính hiệu ứng Stroke không được lưu vào tệp PSD|Lỗi|

## **Thay đổi API công khai**
# **API Thêm vào:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **API Đã xóa:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-694. Khi đọc PattResource, chiều rộng và chiều cao đã được hoán đổi**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // kích hoạt vẽ mẫu

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Hợp nhất không chính xác của nhiều Layer Effect**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // Tìm lớp Văn bản
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Tốt nhất";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // Như vậy, chúng ta đang lưu Tệp PSD đã được thay đổi
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. Thứ tự và logic Hợp nhất không chính xác khi có nhiều Layer Effect**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // Như vậy, chúng ta đang lưu Tệp PSD đã được thay đổi
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. Thêm SectionDividerLayer để cải thiện trải nghiệm với các nhóm lớp**

{{< highlight csharp >}}
            // Mã sau mô tả các lớp SectionDividerLayer và cách lấy LayerGroup liên quan đến nó.

            // Cấu trúc lớp
            //    [0]: '</Layer group>' SectionDividerLayer cho Nhóm 1
            //    [1]: 'Layer 1' Lớp thông thường
            //    [2]: '</Layer group>' SectionDividerLayer cho Nhóm 2
            //    [3]: '</Layer group>' SectionDividerLayer cho Nhóm 3
            //    [4]: 'Nhóm 3' Nhóm lớp
            //    [5]: 'Nhóm 2' Nhóm lớp
            //    [6]: 'Nhóm 1' Nhóm lớp

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Các đối tượng không bằng nhau.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Tạo cấu trúc lớp
                // Thêm LayerGroup 'Nhóm 1'
                LayerGroup group1 = image.AddLayerGroup("Nhóm 1", 0, true);
                // Thêm lớp thông thường
                Layer layer1 = new Layer();
                layer1.DisplayName = "Layer 1";
                group1.AddLayer(layer1);
                // Thêm LayerGroup 'Nhóm 2'
                LayerGroup group2 = group1.AddLayerGroup("Nhóm 2", 1);
                // Thêm LayerGroup 'Nhóm 3'
                LayerGroup group3 = group2.AddLayerGroup("Nhóm 3", 0);

                // Lấy các SectionDividerLayer
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // Sử dụng phương thức SectionDividerLayer.GetRelatedLayerGroup(), lấy mẫu LayerGroup liên quan.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // cùng một LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // cùng một LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // cùng một LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // 'Nhóm 1' chứa 5 lớp
            }
{{< /highlight >}}

**PSDNET-842. Các thuộc tính hiệu ứng Stroke không được lưu vào tệp PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Các đối tượng không bằng nhau.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // Sẽ không ném ArgumentNullException

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // Kiểm tra các giá trị đã lưu
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

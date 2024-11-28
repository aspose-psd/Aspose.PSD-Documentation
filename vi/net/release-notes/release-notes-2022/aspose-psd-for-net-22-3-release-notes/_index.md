---
title: Aspose.PSD cho .NET 22.3 - Ghi chú phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-cho-net-22-3-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-210|Thêm thuộc tính IsOpen cho Nhóm Lớp|Tính năng|
|PSDNET-643|Ảnh PSD với các mặt nạ lớp raster loại bỏ mặt nạ khi lưu vào ảnh PSD 16 bit|Lỗi|
|PSDNET-899|Chế độ pha trộn Dissolve không áp dụng cho thư mục có mặt nạ|Lỗi|
|PSDNET-1047|Tệp cụ thể không thể được mở bởi Photoshop sau khi lưu trong Aspose.PSD 21.11|Lỗi|
|PSDNET-1068|Hiển thị không chính xác của lớp với chế độ pha trộn Linear Dodge (Add)|Lỗi|
|PSDNET-1069|Lớp Fill Pattern ném ngoại lệ khi cập nhật sau khi tải|Lỗi|


## **Thay đổi API Công khai**
# **API Thêm vào:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **API Loại bỏ:**
- Không có


## **Ví dụ sử dụng:**

**PSDNET-210. Thêm thuộc tính IsOpen cho Nhóm Lớp**

{{< highlight csharp >}}
// Ví dụ về đọc và ghi thuộc tính IsOpen khi chạy.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. Ảnh PSD với các mặt nạ lớp raster loại bỏ mặt nạ khi lưu vào ảnh PSD 16 bit**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Chế độ pha trộn Dissolve không áp dụng cho thư mục có mặt nạ**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Tệp cụ thể không thể được mở bởi Photoshop sau khi lưu trong Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Cần mở tệp PSD đầu ra bằng Photoshop thủ công.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // không có ngoại lệ.
            }
{{< /highlight >}}

**PSDNET-1068. Hiển thị không chính xác của lớp với chế độ pha trộn Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Lớp Fill Pattern ném ngoại lệ khi cập nhật sau khi tải**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}

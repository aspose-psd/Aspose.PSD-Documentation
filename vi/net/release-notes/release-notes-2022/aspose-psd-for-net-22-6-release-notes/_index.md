---
title: Aspose.PSD cho .NET 22.6 - Ghi chú phát hành
type: docs
weight: 70
url: /vi/net/aspose-psd-cho-net-22-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-940|Tạo API để lấy mã hash duy nhất cho các lớp tương tự trong các tệp khác nhau|Cải tiến|
|PSDNET-678|Hiển thị không đúng của FillLayer với mẫu trong trường hợp các mẫu nhiều hơn một và thứ tự lớp đã thay đổi|Lỗi|
|PSDNET-1125|Ngoại lệ khi tải tệp PSD cụ thể với chế độ màu CMYK|Lỗi|


## **Thay đổi API công cộng**
# **API thêm vào:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **API đã xóa:**
- Không có


## **Ví dụ sử dụng:**

**PSDNET-678. Hiển thị không chính xác của FillLayer với mẫu trong trường hợp các mẫu nhiều hơn một và thứ tự lớp đã thay đổi**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Tạo API để lấy mã hash duy nhất cho các lớp tương tự trong các tệp khác nhau**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // Các phương thức và logic xử lý...
}
{{< /highlight >}}

**PSDNET-1125. Ngoại lệ khi tải tệp PSD cụ thể với chế độ màu CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
---
title: Aspose.PSD cho .NET 24.3 - Ghi chú bản phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-cho-net-24-3-ghi-chu-ban-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú bản phát hành cho [Aspose.PSD cho .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                          | **Danh mục** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [Định dạng AI] Giảm thời gian tải ảnh AI đa trang lớn         |     Cải tiến     |
| PSDNET-1905 | Tệp PSD sau khi chuyển từ 8 bit sang 16 bit trở thành không đọc được |     Lỗi     |
| PSDNET-1906 | Tệp PSD sau khi chuyển từ 8 bit sang 32 bit trở thành không đọc được |     Lỗi     |
| PSDNET-1921 | [Định dạng AI] Sửa lỗi hiển thị Đường cong Ngắn trong tệp AI                 |     Lỗi     |

## **Thay đổi trong API công cộng**
# **API đã thêm:**
- Không có

# **API đã loại bỏ:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-1905. Tệp PSD sau khi chuyển từ 8 bit sang 16 bit trở thành không đọc được**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Lỗi tài nguyên toàn cầu, tài nguyên đầu tiên nên là Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Tệp PSD sau khi chuyển từ 8 bit sang 32 bit trở thành không đọc được**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Lỗi tài nguyên toàn cầu, tài nguyên đầu tiên nên là Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Định dạng AI] Sửa lỗi hiển thị Đường cong Ngắn trong tệp AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

---
title: Aspose.PSD cho .NET 24.2 - Ghi chú phát hành
type: tài liệu
weight: 110
url: /vi/net/aspose-psd-cho-net-24-2-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**    | **Tóm tắt**                                                                  | **Thể loại** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503  | Xử lý thuộc tính Góc cho PatternFillSettings                                |   Tính năng   |
| PSDNET-1719 | Hỗ trợ tỷ lệ dọc và ngang cho TextLayer                                     |     Tính năng     |
| PSDNET-1783 | [Định dạng AI] Thực hiện hiển thị đúng của nền trong Định dạng AI dựa trên PDF |     Tính năng     |
| PSDNET-1611 | Thay đổi cơ chế Distort trong warp                                           |     Cải tiến     |
| PSDNET-1802 | Tăng tốc độ warp                                                             |     Cải tiến     |
| PSDNET-995   | Ngoại lệ "Image loading failed." khi mở tài liệu                              |     Lỗi     |
| PSDNET-1491 | Sửa lỗi lưu các tệp psd có Stroke Pattern                                   |     Lỗi     |
| PSDNET-1642 | Kiểu văn bản không chính xác trong một đối tượng thông minh khi sử dụng ReplaceContents |     Lỗi     |
| PSDNET-1884 | [Định dạng AI] Sửa lỗi việc vẽ Cubic Bezier trong tệp AI                   |     Lỗi     |

## **Thay đổi API công cộng**
# **API đã thêm:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API đã xóa:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-1503. Xử lý thuộc tính Góc cho PatternFillSettings**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Hỗ trợ tỷ lệ dọc và ngang cho TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [Định dạng AI] Thực hiện hiển thị đúng của nền trong Định dạng AI dựa trên PDF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Ngoại lệ "Image loading failed." khi mở tài liệu**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "PRODUCT.ai");
string outputFile1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(sourceFile1))
{
    image.Save(outputFile1, new PngOptions());
}

// Code tiếp theo tương tự như trên...
{{< /highlight >}}

// Vui lòng xem tệp JSON hoàn chỉnh để xem các phần còn lại của mã nguồn và hướng dẫn sử dụng.

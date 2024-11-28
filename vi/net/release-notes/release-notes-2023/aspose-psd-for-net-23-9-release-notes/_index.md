---
title: Aspose.PSD cho .NET 23.9 - Ghi chú phát hành
type: docs
weight: 40
url: /vi/net/aspose-psd-cho-net-23-9-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                                                | **Danh mục** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Thực hiện tạo mặt nạ cho các lớp điều chỉnh mới         | Tính năng |
| PSDNET-1654 | Thêm hỗ trợ của các lớp Blend Clipped làm tùy chọn nhóm blending | Tính năng |
| PSDNET-1194 | Tệp PSD với chế độ màu 16 bit không áp dụng mặt nạ cho các lớp điều chỉnh| Lỗi     |
| PSDNET-1235 | Hiển thị không chính xác dấu ngoặc trong lớp văn bản | Lỗi     |
| PSDNET-1559 | Không thể cập nhật kiểu trong các lớp văn bản            | Lỗi     |
| PSDNET-1583 | Sau khi xuất tệp PSD với CMYK làm hỏng màu sắc trong PSD đã xuất | Lỗi     |
| PSDNET-1619 | Tệp PSB cụ thể gây ra ngoại lệ "Hình chữ nhật không có khu vực xử lý chung" | Lỗi     |
| PSDNET-1648 | Tải hình ảnh thất bại. OverflowException: Phép tính số học dẫn đến tràn | Lỗi     |


## **Thay Đổi API Công Cộng**
# **APIs Đã Thêm:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **APIs Đã Xóa:**
- Không có


## **Ví dụ Sử Dụng:**

**PSDNET-1638. Thực hiện tạo mặt nạ cho các lớp điều chỉnh mới**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Thêm hỗ trợ của các lớp Blend Clipped làm tùy chọn nhóm blending**

{{< highlight csharp >}}
string sourceFile = "example_source.psd";
string outputPsd = "example_output.psd";
string outputPng = "example_output.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. Tệp PSD với chế độ màu 16 bit không áp dụng mặt nạ cho các lớp điều chỉnh**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string outputPng = "current.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Hiển thị không chính xác dấu ngoặc trong lớp văn bản**

{{< highlight csharp >}}
string file = "file1.psd";
string output = "output_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Không thể cập nhật kiểu trong các lớp văn bản**

{{< highlight csharp >}}
string sourceFile = "Example_FontSize.psd";
string outputFile = "output_Example_FontSize.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "text1", "text2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "text layer 1", "text layer 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. Sau khi xuất tệp PSD với CMYK làm hỏng màu sắc trong PSD đã xuất**

{{< highlight csharp >}}
string sourceFile = "canyon.psd";
string outputFilePng = "output_canyon.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(sourceFile))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(outputFilePng, new PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Tệp PSB cụ thể gây ra ngoại lệ "Hình chữ nhật không có khu vực xử lý chung"**

{{< highlight csharp >}}
var input = "1619_src.psb";
var output = "1619_output.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Tải hình ảnh thất bại. OverflowException: Phép tính số học dẫn đến tràn**

{{< highlight csharp >}}
string sourceFile = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

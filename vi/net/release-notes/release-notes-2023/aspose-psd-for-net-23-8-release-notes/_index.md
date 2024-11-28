---
title: Aspose.PSD cho .NET 23.8 - Ghi chú phiên bản
type: docs
weight: 50
url: /vi/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú cho [Aspose.PSD cho .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Tóm tắt**                                                                                                  | **Danh mục** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Thêm loại định dạng mới (Cờ) | Tính năng |
| PSDNET-1621 | Thêm loại định dạng mới: cung lên, cung xuống, cầu | Tính năng |
| PSDNET-1682 | Thực hiện phương thức mới PsdImage.AddPosterizeAdjustmentLayer để thêm lớp Posterize mới | Tính năng |
| PSDNET-913  | Thông tin PSD bị mất chỉ khi mở và lưu | Lỗi     |
| PSDNET-1352 | Tải hình ảnh thất bại | Lỗi     |
| PSDNET-1553 | Tải hình ảnh thất bại: Không thể chuyển đổi đối tượng từ loại UnknownStructure sang loại DescriptorStructure | Lỗi     |
| PSDNET-1631 | Tệp bị thay đổi trong thư viện bên thứ ba làm hỏng tệp PSD nhưng có thể mở trong Photoshop | Lỗi     |


## **Thay đổi API Công khai**
# **API Đã Thêm:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **API Đã Xóa:**
- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-913. Thông tin PSD bị mất chỉ khi mở và lưu**

{{< highlight csharp >}}
string src = "File gốc.psd";
string outputPsd = "out_File gốc.psd";
string outputPng = "out_File gốc.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Tải hình ảnh thất bại**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Tải hình ảnh thất bại: Không thể chuyển đổi đối tượng từ loại UnknownStructure sang loại DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Nên tải đúng
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Tệp bị thay đổi trong thư viện bên thứ ba làm hỏng tệp PSD nhưng có thể mở trong Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Thêm loại định dạng mới (Cờ)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Thêm loại định dạng mới: cung lên, cung xuống, cầu**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Thực hiện phương thức mới PsdImage.AddPosterizeAdjustmentLayer để thêm lớp Posterize mới**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Kiểm tra các thay đổi đã lưu
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

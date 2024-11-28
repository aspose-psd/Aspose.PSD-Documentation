---
title: Ghi chú phát hành Aspose.PSD cho .NET 24.7
type: docs
weight: 60
url: /vi/net/aspose-psd-cho-net-24-7-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 24,7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Tóm tắt**                                       | **Danh mục** |
|:------------|:--------------------------------------------------|:-------------|
| PSDNET-1029 | Ngoại lệ "Image loading failed." khi mở tài liệu AI | Lỗi      |
| PSDNET-2022 | Văn bản hiển thị không chính xác trong tệp PDF đầu ra | Lỗi      |
| PSDNET-2061 | Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp đã cho trên Linux | Lỗi      |
| PSDNET-2080 | Sửa lỗi tải font khi sử dụng Aspose.Drawing        | Lỗi      |
| PSDNET-2085 | 'Phép toán số học đã dẫn đến tràn' khi tạo lớp đối tượng thông minh sử dụng ảnh JPEG lớn | Lỗi      |
| PSDNET-2100 | Tệp AI không thể chuyển đổi thành tệp JPG          | Lỗi      |

## **Thay đổi API công cộng**
# **API Thêm vào:**
- Không có

# **API Xóa bỏ:**
- Không có

## **Ví dụ sử dụng:**

**PSDNET-1029. Ngoại lệ "Image loading failed." khi mở tài liệu AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Văn bản hiển thị không chính xác trong tệp PDF đầu ra**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Sửa lỗi ImageSaveException: Xuất hình ảnh thất bại cho tệp đã cho trên Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Sửa lỗi tải font khi sử dụng Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Trước khi cập nhật. Số lượng font đã cài đặt: " + installedFonts.Families.Length);
    Console.WriteLine("- Nền tảng: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Làm mới bộ nhớ cache font bằng cách thử lấy tên font Adobe cho 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Sau khi cập nhật. Số lượng font đã cài đặt: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Phép toán số học đã dẫn đến tràn' khi tạo lớp đối tượng thông minh sử dụng ảnh JPEG lớn**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Tệp AI không thể chuyển đổi thành tệp JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

---
title: Aspose.PSD cho .NET 22.12 - Ghi chú phát hành
type: docs
weight: 10
url: /vi/net/aspose-psd-cho-net-22-12-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD for .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- Trong bản phát hành này, đã sửa lỗi hồi phục với việc xuất 16 bit.

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Thể loại**|
| :- | :- | :- |
|PSDNET-1336|Thêm thuộc tính TextOrientation có thể chỉnh sửa vào giao diện IText|Tính năng|
|PSDNET-725|Thay đổi kích thước tệp PSD chỉ định với mặt nạ lớp sản xuất mặt nạ không chính xác|Lỗi|
|PSDNET-1277|Thêm khả năng lưu và tải một mặt nạ cho 16 hình ảnh|Lỗi|
|PSDNET-1281|Độ trong suốt không chính xác khi lưu hình ảnh 16 bit thành hình ảnh 16 hoặc 8 bit|Lỗi|
|PSDNET-1375|Sửa CMYK trong màu 16 bit|Lỗi|


## **Thay Đổi API Công Cộng**
# **API Thêm:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **API Đã Xóa:**
- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-725. Thay đổi kích thước tệp PSD chỉ định với mặt nạ lớp sản xuất mặt nạ không chính xác**

{{< highlight csharp >}}
string tệpNguồn = "source.psd";
string đườngDẫnXuấtPsd = "output.psd";
string đườngDẫnXuấtPng = "output.png";

// Mở tệp PSD nguồn
using (PsdImage hìnhẢnh = (PsdImage)Image.Load(tệpNguồn))
{
    const int TỉLệ = 4;

    int chiềuRộngMới = hìnhẢnh.Width * TỉLệ;
    int chiềuCaoMới = hìnhẢnh.Height * TỉLệ;

    // Thực hiện thay đổi kích thước
    hìnhẢnh.Resize(chiềuRộngMới, chiềuCaoMới);
    hìnhẢnh.Save(đườngDẫnXuấtPsd, new PsdOptions(hìnhẢnh));
}

// Mở tệp PSD có kích thước thay đổi
using (PsdImage hìnhẢnh = (PsdImage)Image.Load(đườngDẫnXuấtPsd))
{
    // Render sang PNG
    hìnhẢnh.Save(đườngDẫnXuấtPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Thêm khả năng lưu và tải một mặt nạ cho 16 hình ảnh**

{{< highlight csharp >}}
string tệpPsd8BitNguồn = @"input_8bitColor.psd";
string tệpPsd16BitXuất = @"output_16bitColor.psd";

using (var hìnhẢnh = (PsdImage)Image.Load(tệpPsd8BitNguồn))
{
    // Tùy chọn cho phép lưu màu 16 bit
    PsdOptions tùyChọn16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Tệp PSD sẽ được lưu với độ trong suốt
    hìnhẢnh.Save(tệpPsd16BitXuất, tùyChọn16);
}
{{< /highlight >}}

**PSDNET-1281. Độ trong suốt không chính xác khi lưu hình ảnh 16 bit thành hình ảnh 16 hoặc 8 bit**

{{< highlight csharp >}}
string tệpNguồn = @"Example_16bit.psd";
string tệpLưuLại = @"Resave_16bit.psd";
string tệpHìnhẢnh = @"TotalImage_16bit.png";

// Mở tệp psd màu 16 bit (với độ trong suốt) và lưu sang màu 16 bit
using (var hìnhẢnh = (PsdImage)Image.Load(tệpNguồn))
{
    PsdOptions tùyChọn16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    hìnhẢnh.Save(tệpLưuLại, tùyChọn16);
}

// Tệp psd màu 16 bit đã lưu sẽ được chuyển đổi sang tệp png với độ trong suốt
using (var hìnhẢnh = (PsdImage)Image.Load(tệpLưuLại))
{
    hìnhẢnh.Save(tệpHìnhẢnh, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Thêm thuộc tính TextOrientation có thể chỉnh sửa vào giao diện IText**

{{< highlight csharp >}}
// Mã dưới đây thể hiện khả năng chỉnh sửa thuộc tính TextOrientation mới.
// Điều này không ảnh hưởng đến việc hiển thị lúc này, mà chỉ cho phép bạn chỉnh sửa giá trị thuộc tính.

string nguồn = "1336test.psd";
string xuất = "out_1336test.psd";

using (var hìnhẢnh = (PsdImage)Image.Load(nguồn))
{
    var lớpVănBản = hìnhẢnh.Layers[1] as TextLayer;
    if (lớpVănBản.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Đọc đúng
    }
    else
    {
        throw new Exception("Đọc giá trị thuộc tính TextOrientation không chính xác");
    }

    lớpVănBản.TextData.TextOrientation = TextOrientation.Horizontal;
    lớpVănBản.TextData.UpdateLayerData();

    hìnhẢnh.Save(xuất);
}

using (var hìnhẢnh = (PsdImage)Image.Load(xuất))
{
    var lớpVănBản = hìnhẢnh.Layers[1] as TextLayer;
    if (lớpVănBản.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Đọc đúng
    }
    else
    {
        throw new Exception("Đọc giá trị thuộc tính TextOrientation không chính xác");
    }
}
{{< /highlight >}}

**PSDNET-1375. Sửa CMYK trong màu 16 bit**

{{< highlight csharp >}}
string tệpNguồn = @"ClippingMaskRegular.psd";
string đườngDẫnXuất = @"export.psd";
string đườngDẫnXuấtPng = @"export.png";

// Thiết lập tùy chọn chuyển đổi
PsdOptions tùyChọnPsd = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Chuyển đổi và lưu
using (var hìnhẢnh = (PsdImage)Image.Load(tệpNguồn))
{
    hìnhẢnh.Convert(tùyChọnPsd);
    hìnhẢnh.Save(đườngDẫnXuất);
}

// Mở tệp chuyển đổi và render ra PNG
using (var hìnhẢnh = (PsdImage)Image.Load(đườngDẫnXuất))
{
    hìnhẢnh.Save(đườngDẫnXuấtPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

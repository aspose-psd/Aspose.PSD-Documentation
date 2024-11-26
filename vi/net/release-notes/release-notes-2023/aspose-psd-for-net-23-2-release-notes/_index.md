---
title: Aspose.PSD cho .NET 23.2 - Ghi chú phát hành
type: docs
weight: 110
url: /vi/net/aspose-psd-cho-net-23-2-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1359|Tái cấu trúc k rende văn bản để cải thiện vị trí văn bản, kết xuất và hỗ trợ|Cải tiến|
|PSDNET-1270|Thêm khả năng xử lý Hiệu ứng uốn cong qua API công cộng|Tính năng|
|PSDNET-1391|Thêm hỗ trợ chế độ dẫn dưới cùng và đầu trên cùng từ cài đặt đoạn văn|Tính năng|
|PSDNET-912|Thay đổi Phông chữ và Màu sắc cho TextLayer PSD|Lỗi|
|PSDNET-1022|Xuất sai văn bản ở bài kiểm tra TextUpdateTests, thiếu văn bản|Lỗi|
|PSDNET-1221|Văn bản cỡ rất nhỏ mất sau khi thay đổi kích thước ảnh PSD lớn hơn|Lỗi|
|PSDNET-1301|Aspose.Psd cho .NET textLayer.UpdateText() in ấn '-' (gạch ngang) như gạch dưới theo cách ngẫu nhiên cho các bộ dữ liệu khác nhau|Lỗi|
|PSDNET-1379|Cài đặt Độ phân giải không áp dụng cho việc xuất từ PSD sang PDF|Lỗi|


## **Thay đổi API công cộng**
# **Các API được thêm vào:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop


# **Các API bị xóa bỏ:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual


## **Ví dụ về việc sử dụng:**

**PSDNET-912. Thay đổi Phông chữ và Màu sắc cho TextLayer PSD**

{{< highlight csharp >}}
string thuMucPhong = "Fonts";
string fileNguon = "M1PDTT26052021001.psd";
string psdKetQua = "ketqua.psd";
string pngKetQua = "ketqua.png";

FontSettings.SetFontsFolder(thuMucPhong);

using (var hinhAnh = (PsdImage)Image.Load(fileNguon))
{
    TextLayer tenLop = (TextLayer)hinhAnh.Layers[9];
    var phanVanBan = tenLop.TextData.Items[0];

    phanVanBan.Text = "MODESTO SR";
    phanVanBan.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    phanVanBan.Style.FillColor = Color.Red;

    tenLop.TextData.UpdateLayerData();

    hinhAnh.Save(psdKetQua);
    hinhAnh.Save(pngKetQua, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. Xuất sai văn bản ở bài kiểm tra TextUpdateTests, thiếu văn bản**

{{< highlight csharp >}}
string fileNguon = "ComplexKerningExample.psd";
string psdKetQua = "TextUpdateComplexKerningExample_.psd";
string pngKetQua = "TextUpdateComplexKerningExample_.png";

using (var hinhAnh = (PsdImage)Image.Load(fileNguon))
{
    for (int i = 0; i < hinhAnh.Layers.Length; i++)
    {
        var lop = hinhAnh.Layers[i] as TextLayer;

        if (lop != null)
        {
            lop.UpdateText("Văn bản đã được cập nhật");
        }
    }

    hinhAnh.Save(psdKetQua);
    hinhAnh.Save(pngKetQua, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. Văn bản cỡ rất nhỏ mất sau khi thay đổi kích thước ảnh PSD lớn hơn**

{{< highlight csharp >}}
string nguon = "textTest.psd";
string ketQua = "ketqua.png";

using (var hinhPsd = (PsdImage)Image.Load(nguon))
{
    hinhPsd.Resize(30, 30);

    hinhPsd.Save(ketQua, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. Thêm khả năng xử lý Hiệu ứng uốn cong qua API công cộng**

{{< highlight csharp >}}
string fileNguon = "source.psd";
string pngUon = "warped.png";
string psdUon = "warpFile.psd";

var cacTuChonTaiLoadUon = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var hinhAnh = (PsdImage)Image.Load(fileNguon, cacTuChonTaiLoadUon))
{
    hinhAnh.Save(pngUon, new PngOptions());
    hinhAnh.Save(psdUon, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd cho .NET textLayer.UpdateText() in ấn '-' (gạng) như gạch dưới theo cách ngẫu nhiên cho các bộ dữ liệu khác nhau**

{{< highlight csharp >}}
string nguon = "TEST_PSD_FILE.PSD";
string ketQua = "OUTPUTIMAGE.jpg";

using (PsdImage hinhPsd = (PsdImage)Image.Load(nguon))
{
    foreach (var lop in hinhPsd.Layers.Where(x => x.IsVisible))
    {
        if (lop is TextLayer)
        {
            TextLayer textLayer = lop as TextLayer;
            switch (lop.Name.Trim().ToUpper())
            {
                case "TÊN":
                    textLayer.UpdateText("ANH. NGUYỄN PHÚC VINH");
                    break;
                case "SỐ ID":
                    textLayer.UpdateText("OFF-022/NHÓM - 016");
                    break;
                case "CHỨC DANH":
                    textLayer.UpdateText("NHÂN VIÊN-001");
                    break;
                case "NHÓM MÁU":
                    textLayer.UpdateText("AB-");
                    break;
                case "ĐỊA CHỈ":
                    textLayer.UpdateText("KHỐI-A, ĐƯỜNG-7, CĂN HỘ SỐ - 047, KHU VỰC-024");
                    break;
                case "ĐỊA CHỈ THƯỜNG TRÚ":
                    textLayer.UpdateText("NHÀ SỐ - 42, NGỎ -025, CĂN HỘ VIEW CÂY LÁ, KHU VỰC - 45");
                    break;
            }
        }
    }

    hinhPsd.Save(ketQua, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. Cài đặt Độ phân giải không áp dụng cho việc xuất từ PSD sang PDF**

{{< highlight csharp >}}
string nhap = "Datensatz 1.psd";
string ketQua = "Datensatz 1.pdf";

using (var hinhAnh = Image.Load(nhap, new PsdLoadOptions()))
{
    ResolutionSetting caiDatDoPhanGiai = new ResolutionSetting(300, 300);

    hinhAnh.Save(ketQua, new PdfOptions()
    {
        ResolutionSettings = caiDatDoPhanGiai
    });
}
{{< /highlight >}}

**PSDNET-1391. Thêm hỗ trợ chế độ dẫn dưới cùng và đầu trên cùng từ cài đặt đoạn văn**

{{< highlight csharp >}}
string nhap = "leadingMode.psd";
string ketQua = "output_leadingMode.png";

using (var hinhPsd = (PsdImage)Image.Load(nhap, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)hinhPsd.Layers[1]).TextData;
    foreach (var phanVanBan in text1.Items)
    {
        phanVanBan.Paragraph.LeadingType = LeadingType.TopToTop; // Thay đổi giá trị LeadingType   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)hinhPsd.Layers[2]).TextData;
    foreach (var phanVanBan in text2.Items)
    {
        phanVanBan.Paragraph.LeadingType = LeadingType.BottomToBottom; // Thay đổi giá trị LeadingType   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    hinhPsd.Save(ketQua, new PngOptions());
}
{{< /highlight >}}

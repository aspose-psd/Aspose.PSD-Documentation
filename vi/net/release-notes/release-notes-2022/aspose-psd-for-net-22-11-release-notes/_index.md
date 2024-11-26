---
title: Aspose.PSD cho .NET 22.11 - Ghi chú phát hành
type: docs
weight: 20
url: /vi/net/aspose-psd-cho-net-22-11-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú phát hành cho [Aspose.PSD cho .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Bản phát hành này có một rủi ro trong trường hợp xuất tệp 16-bit, vì vậy chúng tôi khuyến nghị cẩn thận khi sử dụng tính năng này trong bản phát hành này.
Vui lòng không cập nhật Aspose.PSD lên phiên bản 22.9-22.11 nếu xử lý hình ảnh 16-bit là chức năng chính của bạn.

Chúng tôi đang làm việc để tìm giải pháp cho các vấn đề này.

{{% /alert %}}

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-1320|Không thể xuất tệp PSB cực lớn|Cải tiến|
|PSDNET-659|Làm cho trung tâm của đối tượng đồng tâm có thể di chuyển được|Tính năng|
|PSDNET-1330|Phương pháp nén ZipWithoutPrediction không được hỗ trợ cho các tệp cụ thể|Tính năng|
|PSDNET-735|Sau khi sử dụng một phương pháp biến đổi cho một lớp, lớp đã lưu bị sai bounding box|Lỗi|
|PSDNET-1234|Ngoại lệ khi tải hình ảnh PSD có mẫu|Lỗi|
|PSDNET-1244|Xuất hình ảnh thất bại (IndexOutOfRangeException) khi lưu tệp PSD với ký tự Trung Quốc|Lỗi|
|PSDNET-1303|TimeLine ActiveFrame áp dụng không chính xác|Lỗi|
|PSDNET-1307|Regression 22.7: hiển thị văn bản với ký tự Ả Rập không chính xác|Lỗi|
|PSDNET-1321|Vector Mask trên lớp Nhóm hoạt động không đúng. Hình ảnh cuối cùng có lỗ đen nhưng không nên có|Lỗi|


## **Sự thay đổi trong API công cộng**
# **API Thêm vào:**

- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **API Bỏ đi:**

- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-659. Làm cho trung tâm của đối tượng đồng tâm có thể di chuyển được**

{{< highlight csharp >}}
string tệpNguồn = "psdnet659.psd";
string tệpĐầuRa = "output.png";

using (var psdHình = (PsdImage)Image.Load(tệpNguồn))
{
    FillLayer lớpĐồngTâm = (FillLayer)psdHình.Layers[5];
    GradientFillSettings càiĐặt = (GradientFillSettings)lớpĐồngTâm.FillSettings;

    // Cập nhật điểm bù
    càiĐặt.HorizontalOffset = 10;
    càiĐặt.VerticalOffset = -25;

    psdHình.Save(tệpĐầuRa, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Sau khi sử dụng phương pháp biến đổi cho một lớp, lớp đã lưu bị sai bounding box**

{{< highlight csharp >}}
string tênTệpNguồn = @"TextLayer.psd";
string tệpĐầuRa = "TextLayerResized_output.psd";

using (PsdImage hình = (PsdImage)Image.Load(tênTệpNguồn, new PsdLoadOptions()))
{
    TextLayer lớpVănBản = (TextLayer)hình.Layers[1];

    // Đặt kích thước mới cho lớp văn bản
    const int ChiềuRộngMới = 250;
    const int ChiềuCaoMới = 250;

    // Đặt cơ chế cho việc hàm thay đổi kích thước sẽ thay đổi lớp (giá trị mặc định)
    ResizeType loạiThayĐổiKíchThước = ResizeType.NearestNeighbourResample;

    // Cơ chế mới thay đổi kích thước cho lớp văn bản ở đây
    // Không chỉ lớp mà còn ma trận biến đổi của lớp văn bản sẽ thay đổi
    lớpVănBản.Resize(ChiềuRộngMới, ChiềuCaoMới, loạiThayĐổiKíchThước);

    hình.Save(tệpĐầuRa, new PsdOptions(hình));
}

using (PsdImage hình = (PsdImage)Image.Load(tệpĐầuRa, new PsdLoadOptions()))
{
    TextLayer lớpVănBản = (TextLayer)hình.Layers[1];

    // Lý do vị trí sai là do phông chữ mặc định khác
    if (lớpVănBản.TransformMatrix[4] >= 65 
        && lớpVănBản.TransformMatrix[4] <= 67
        && lớpVănBản.TransformMatrix[5] >= 234
        && lớpVănBản.TransformMatrix[5] <= 237)
    {
        // Mọi thứ đều ổn
    }
    else
    {
        throw new Exception("Điểm đặt sai");
    }
}
{{< /highlight >}}

**PSDNET-1234. Ngoại lệ khi tải hình ảnh PSD có mẫu**

{{< highlight csharp >}}
string tệpSrc = "test.psd";
string đầuRa = "output1234.png";

using (PsdImage hìnhPSD = (PsdImage)PsdImage.Load(tệpSrc,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions tùyChọnPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    hìnhPSD.Save(đầuRa, tùyChọnPng);
}
{{< /highlight >}}

**PSDNET-1244. Xuất hình ảnh thất bại (IndexOutOfRangeException) khi lưu tệp PSD với ký tự Trung Quốc**

{{< highlight csharp >}}
string tệpNguồn = "input.psd";
string đườngDẫnĐầuRa = "output.psd";

var tùyChọnTải = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var hình = (PsdImage)Image.Load(tệpNguồn, tùyChọnTải))
{
    foreach (var lớp in hình.Layers)
    {
        if (lớp.Name == "1")
        {
            var lớpVănBản = (TextLayer)lớp;

            lớpVănBản.UpdateText("测试测试");
        }
    }

    // Ở đây không nên có ngoại lệ.
    hình.Save(đườngDẫnĐầuRa, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame áp dụng không chính xác**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string đầuRa = "out_timeline.psd";

using (var hìnhPSD = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(hìnhPSD);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(hìnhPSD);

    hìnhPSD.Save(đầuRa);
}
{{< /highlight >}}

**PSDNET-1307. Regression 22.7: hiển thị văn bản với ký tự Ả Rập không chính xác**

{{< highlight csharp >}}
string thưMụcPhôngChữThửNghiệm = "Fonts";
FontSettings.SetFontsFolder(thưMụcPhôngChữThửNghiệm);
FontSettings.UpdateFonts();

string đườngDẫnNguồn = "sarbarg.fin12.psd";
string đườngDẫnĐầuRa = "result.tiff";

using (var hìnhPSD = (PsdImage)Image.Load(đườngDẫnNguồn))
{
    hìnhPSD.Save(đườngDẫnĐầuRa, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Không thể xuất tệp PSB cực lớn**

{{< highlight csharp >}}
string tệpNguồn = "hf-mim-liman-han-guc-art-kuvvet.psb";
string đườngDẫnXuấtPSD = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var hình = (PsdImage)Image.Load(tệpNguồn, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    hình.Save(đườngDẫnXuấtPSD, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Vector Mask trên lớp Nhóm hoạt động không đúng. Hình ảnh cuối cùng có lỗ đen nhưng không nên có**

{{< highlight csharp >}}
string tệpNguồn = "demo.psd";
string đầuRa = "demo_net.png";

using (PsdImage hình = (PsdImage)PsdImage.Load(tệpNguồn))
{
    PngOptions tùyChọnPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    hình.Save(đầuRa, tùyChọnPng);
}
{{< /highlight >}}

**PSDNET-1330. Phương pháp nén ZipWithoutPrediction không được hỗ trợ cho các tệp cụ thể**

{{< highlight csharp >}}
string tệpNguồn = "20221017_220706_0000.psd";
string đầuRa = "20221017_220706_0000.jpg";

using (var hình = (PsdImage)Image.Load(tệpNguồn, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase tùyChọnHình = new JpegOptions() { Quality = 80 };
    hình.Save(đầuRa, tùyChọnHình);
}
{{< /highlight >}}

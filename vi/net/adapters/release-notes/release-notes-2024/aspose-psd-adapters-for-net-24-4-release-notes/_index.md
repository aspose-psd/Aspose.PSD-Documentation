---
title: Aspose.PSD Bộ chuyển đổi cho .NET 24.4 - Ghi chú Phát hành
type: docs
weight: 100
url: /vi/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD Bộ chuyển đổi cho .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                          | **Danh mục** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Xuất bản ban đầu Aspose.PSD.Adapters.Imaging đến Nuget            | Nâng cấp |


## **Sự thay đổi trong API Công khai**
# **API Thêm vào:**
- Không có

# **API Bị xóa:**
- Không có

## **Ví dụ Sử dụng:**

Vui lòng kiểm tra [trang tài liệu Aspose.PSD.Adapters](/vi/psd/net/adapters)

**PSDNET-1985. Ví dụ hoàn chỉnh nhất về việc sử dụng Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Thêm việc kích hoạt các bộ chuyển đổi trong cấu hình khởi tạo của bạn 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// bổ sung việc kích hoạt Exporters
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Để làm việc với bộ chuyển đổi, bạn cần cả Giấy phép Aspose.PSD và adaptee
// Đây là cách áp dụng Giấy phép Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Đây là ví dụ về cách áp dụng Giấy phép Adaptee cho Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Sau đó, bạn có thể chạy bất kỳ mã nào của adapters hoặc thư viện PSD hoặc Imaging

// Sau đó, tất cả các tệp này có thể được mở bởi Aspose.PSD mà không cần bất kỳ mã bổ sung nào chỉ cần sử dụng
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Sau khi thực thi mã này, bạn sẽ nhận được Tệp PSD được tạo ra từ WEBP và có thể áp dụng bất kỳ Bộ lọc, Lớp và Điều chỉnh Aspose.PSD nào bao gồm biến đổi Warp.
}

// Bạn có thể thêm vào việc Tạo Hình ảnh Adaptees xuất sang Định dạng PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Sử dụng API Aspose.Imaging để Chỉnh sửa tệp WEBP với các tính năng cụ thể của Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Sau đó chỉ cần sử dụng phương thức ToPsdImage() và chỉnh sửa tệp như PSD với các tính năng giống Photoshop bao gồm lớp, bộ lọc thông minh và đối tượng thông minh.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Lưu tệp PSD cuối cùng bằng cách sử dụng Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Nếu bạn không cần sử dụng Loaders hoặc Exporters được cung cấp bởi Bộ chuyển đổi chỉ cần vô hiệu hóa chúng
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}

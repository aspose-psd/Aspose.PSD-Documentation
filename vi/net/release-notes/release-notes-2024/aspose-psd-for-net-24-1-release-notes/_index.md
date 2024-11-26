---
title: Aspose.PSD cho .NET 24.1 - Ghi chú về bản phát hành
type: docs
weight: 120
url: /vi/net/aspose-psd-cho-net-24-1-ghi-chu-phien-ban/
---

{{% alert color="primary" %}}
 
Trang này chứa các ghi chú về [Aspose.PSD cho .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                       | **Thể loại** |
|:-------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835  | [Định dạng AI] Thêm xử lý cơ bản cho hình ảnh AI đa trang                                         |   Tính năng  |
| PSDNET-718   | Hiệu ứng Biến dạng Văn bản không áp dụng vào văn bản                                             |     Lỗi      |
| PSDNET-1620  | Hiển thị không chính xác của mặt nạ trong tệp cụ thể                                              |     Lỗi      |
| PSDNET-1855  | NullReferenceException tại Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor   |     Lỗi      |
| PSDNET-1883  | [Định dạng AI] Sửa lỗi việc sử dụng bộ nhớ trong AiExporterUtils                                  |     Lỗi      |



## **Sự thay đổi trong API công cộng**
# **API Đã Thêm:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API Đã Xoá:**
- Không có


## **Ví dụ về cách sử dụng:**

**PSDNET-718. Hiệu ứng Biến dạng Văn bản không áp dụng vào văn bản**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Hiển thị không chính xác của mặt nạ trong tệp cụ thể**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Định dạng AI] Thêm xử lý cơ bản cho hình ảnh AI đa trang**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Tải hình ảnh AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Mặc định, ActivePageIndex là 0.
    // Vì vậy, nếu bạn lưu hình ảnh AI mà không thay đổi thuộc tính này, trang đầu tiên sẽ được hiển thị và lưu.
    image.Save(firstPageOutputPng, new PngOptions());

    // Thay đổi chỉ số trang hoạt động sang trang thứ hai.
    image.ActivePageIndex = 1;

    // Lưu trang thứ hai của hình ảnh AI dưới dạng hình ảnh PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Thay đổi chỉ số trang hoạt động sang trang thứ ba.
    image.ActivePageIndex = 2;

    // Lưu trang thứ ba của hình ảnh AI dưới dạng hình ảnh PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException tại Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Định dạng AI] Sửa lỗi việc sử dụng bộ nhớ trong AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Load hình ảnh AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Lưu trang đầu tiên của hình ảnh AI dưới dạng hình ảnh PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Thay đổi chỉ số trang hoạt động sang trang thứ hai.
    image.ActivePageIndex = 1;

    // Lưu trang thứ hai của hình ảnh AI dưới dạng hình ảnh PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Thay đổi chỉ số trang hoạt động sang trang thứ ba.
    image.ActivePageIndex = 2;

    // Lưu trang thứ ba của hình ảnh AI dưới dạng hình ảnh PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Việc sử dụng bộ nhớ quá lớn. " + memoryUsed + " thay vì " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}

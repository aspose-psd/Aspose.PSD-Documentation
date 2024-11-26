---
title: Aspose.PSD cho .NET 24.6 - Ghi chú Phát hành
type: docs
weight: 70
url: /vi/net/aspose-psd-cho-net-24-6-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**    | **Tóm tắt**                                                                           | **Loại**  |
|:------------|:---------------------------------------------------------------------------------------|:---------|
| PSDNET-1450 | Triển khai hỗ trợ cho lớp sắc độ Gradient map                                             | Tính năng|
| PSDNET-1670 | [Định dạng AI] Thêm hỗ trợ Metadata XPacket vào Định dạng AI                           | Tính năng|
| PSDNET-1831 | Triển khai các kiểu uốn khác nhau: Inflate, Squeeze và Twist                             | Tính năng|
| PSDNET-1653 | Chế độ Rgb và Lab không thể chứa ít hơn 3 kênh và nhiều hơn 4 kênh trong tệp có Lớp ArtBoard | Lỗi  |
| PSDNET-1775 | Vùng xử lý phía trên phải là số dương. (Tham số 'areaToProcess') khi xử lý tệp cụ thể     | Lỗi  |
| PSDNET-2052 | Hình ảnh bị mở rộng ra ngoài bảng được cắt sau khi lưu. Dữ liệu bị mất, nhưng xem trước đúng | Lỗi  |

## **Thay đổi trong API Công khai**
# **API Thêm vào:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API Loại bỏ:**
- Không có

## **Ví dụ về cách sử dụng:**

**PSDNET-1450. Triển khai hỗ trợ cho lớp sắc độ Gradient map**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // Thêm lớp điều chỉnh Gradient map.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// Kiểm tra các thay đổi đã được lưu
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Định dạng AI] Thêm hỗ trợ Metadata XPacket vào Định dạng AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Các đối tượng không bằng nhau.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Đối tượng kiểm tra là null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Metadata Xmp đã được thêm vào.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Bây giờ chúng ta có thể truy cập vào Gói Xmp của các tệp AI.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // Và chúng tôi có thể truy cập nội dung của các gói này.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. Triển khai các kiểu uốn khác nhau: Inflate, Squeeze và Twist**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Chế độ Rgb và Lab không thể chứa ít hơn 3 kênh và nhiều hơn 4 kênh trong tệp có Lớp ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // Ở đây không nên có ngoại lệ
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. Vùng xử lý phía trên phải là số dương. (Tham số 'areaToProcess') khi xử lý tệp cụ thể**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // Không nên có ngoại lệ
}
{{< /highlight >}}

**PSDNET-2052. Hình ảnh bị mở rộng ra ngoài bảng được cắt sau khi lưu. Dữ liệu bị mất, nhưng xem trước đúng**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Không nên có lỗi ở đây
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Không nên có lỗi ở đây
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

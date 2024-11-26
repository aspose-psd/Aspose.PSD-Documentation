---
title: Aspose.PSD cho .NET 23.10 - Ghi chú phát hành
type: docs
weight: 30
url: /vi/net/aspose-psd-cho-net-23-10-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**   | **Tóm tắt**                                                                                                            | **Danh mục** |
|:------------|:-------------------------------------------|:--------|
| PSDNET-692 | Hỗ trợ hướng văn bản dọc | Tính năng |
| PSDNET-1402 | Sử dụng cài đặt Stroke từ tài nguyên vstk trong việc vẽ gạch đường hình dạng | Tính năng |
| PSDNET-1607 | Triển khai vùng bên trong của các hình dạng Stroke | Tính năng |
| PSDNET-1644 | Không vẽ lại lớp hình dạng nếu nó không thay đổi | Tính năng |
| PSDNET-1696 | [Định dạng AI] Thêm hỗ trợ đọc Header từ Tệp AI dựa trên PDF | Tính năng |
| PSDNET-1560 | Nhiều cách để thiết lập Độ phân giải Tệp Psd không hoạt động | Lỗi |
| PSDNET-1728 | FontSettings.SetFontsFolders không hoạt động hoặc Aspose.PSD sử dụng font không chính xác | Lỗi |
| PSDNET-1739 | Để ngược. Sửa lỗi ngoại lệ tham chiếu Null khi lưu PsdImage khi có lớp Shape | Lỗi |

## **Thay đổi API công khai**
# **API đã thêm:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **API đã xóa:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Ví dụ sử dụng:**

**PSDNET-692. Hỗ trợ hướng văn bản dọc**

{{< highlight csharp >}}
string sourceFile = "692_lt1.psd";
string outputFile = "692_output.png";
string fontsFolder = "692_Fonts";

var fontFolders = new List<string>(FontSettings.GetFontsFolders());
fontFolders.Add(fontsFolder);
FontSettings.SetFontsFolders(fontFolders.ToArray(), true);

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    psdImage.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Sử dụng cài đặt Stroke từ tài nguyên vstk trong việc vẽ gạch đường hình dạng**

{{< highlight csharp >}}
string sourceFile = "StrokeShapeTest.psd";
string outputFilePsd = "StrokeShapeTest.out.psd";
string outputFilePng = "StrokeShapeTest.out.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    Layer layer = image.Layers[1];
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.GreenYellow;
    shapeLayer.Update();

    ShapeLayer shapeLayer2 = (ShapeLayer)image.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)shapeLayer2.Fill;
    gradientSettings.Dither = true;
    gradientSettings.Reverse = true;
    gradientSettings.AlignWithLayer = false;
    gradientSettings.Angle = 20;
    gradientSettings.Scale = 50;
    gradientSettings.ColorPoints[0].Location = 100;
    gradientSettings.ColorPoints[1].Location = 4000;
    gradientSettings.TransparencyPoints[0].Location = 200;
    gradientSettings.TransparencyPoints[1].Location = 3800;
    gradientSettings.TransparencyPoints[0].Opacity = 90;
    gradientSettings.TransparencyPoints[1].Opacity = 10;
    shapeLayer2.Update();

    ShapeLayer shapeLayer3 = (ShapeLayer)image.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)shapeLayer3.Stroke;
    strokeSettings.Size = 15;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    strokeFillSettings.Color = Color.GreenYellow;
    shapeLayer3.Update();

    image.Save(outputFilePsd);
    image.Save(outputFilePng, new PngOptions());
}

// Kiểm tra dữ liệu đã thay đổi.
using (PsdImage image = (PsdImage)Image.Load(outputFilePsd))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    AssertAreEqual(Color.GreenYellow, fillSettings.Color);

    ShapeLayer shapeLayer2 = (ShapeLayer)image.Layers[3];
    GradientFillSettings gradientSettings = (GradientFillSettings)shapeLayer2.Fill;
    AssertAreEqual(true, gradientSettings.Dither);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(20.0, gradientSettings.Angle);
    AssertAreEqual(50, gradientSettings.Scale);
    AssertAreEqual(100, gradientSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, gradientSettings.ColorPoints[1].Location);
    AssertAreEqual(200, gradientSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, gradientSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, gradientSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, gradientSettings.TransparencyPoints[1].Opacity);

    ShapeLayer shapeLayer3 = (ShapeLayer)image.Layers[5];
    StrokeSettings strokeSettings = (StrokeSettings)shapeLayer3.Stroke;
    ColorFillSettings strokeFillSettings = (ColorFillSettings)strokeSettings.Fill;
    AssertAreEqual(15.0, strokeSettings.Size);
    AssertAreEqual(Color.GreenYellow, strokeFillSettings.Color);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1607. Triển khai vùng bên trong của các hình dạng Stroke**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalGradient.psd";
string outputFile = "ShapeInternalGradient.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)shapeLayer.Fill;
    fillSettings.Dither = true;
    fillSettings.Reverse = true;
    fillSettings.AlignWithLayer = false;
    fillSettings.Angle = 20.0;
    fillSettings.Scale = 50;
    fillSettings.ColorPoints[0].Location = 100;
    fillSettings.ColorPoints[1].Location = 4000;
    fillSettings.TransparencyPoints[0].Location = 200;
    fillSettings.TransparencyPoints[1].Location = 3800;
    fillSettings.TransparencyPoints[0].Opacity = 90.0;
    fillSettings.TransparencyPoints[1].Opacity = 10.0;

    shapeLayer.Update();

    image.Save(outputFile);
}

// Kiểm tra dữ liệu đã thay đổi.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    GradientFillSettings fillSettings = (GradientFillSettings)shapeLayer.Fill;

    AssertAreEqual(true, fillSettings.Dither);
    AssertAreEqual(true, fillSettings.Reverse);
    AssertAreEqual(false, fillSettings.AlignWithLayer);
    AssertAreEqual(20.0, fillSettings.Angle);
    AssertAreEqual(50, fillSettings.Scale);
    AssertAreEqual(100, fillSettings.ColorPoints[0].Location);
    AssertAreEqual(4000, fillSettings.ColorPoints[1].Location);
    AssertAreEqual(200, fillSettings.TransparencyPoints[0].Location);
    AssertAreEqual(3800, fillSettings.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, fillSettings.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, fillSettings.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1644. Không vẽ lại lớp hình dạng nếu nó không thay đổi**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";
string outputFile = "ShapeInternalSolid.out.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    // Không sử dụng cập nhật của lớp Shape trước khi lưu

    image.Save(outputFile);

    // Kiểm tra việc vẽ file đã lưu
}

// Kiểm tra rằng dữ liệu lớp hình dạng vẫn không thay đổi.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), fillSettings.Color);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1696. [Định dạng AI] Thêm hỗ trợ đọc Header từ Tệp AI dựa trên PDF**

{{< highlight csharp >}}
string sourceFile = "ai_source.ai";

void AssertIsNotNull(object expected)
{
    if (expected == null)
    {
        throw new Exception("Đối tượng là null.");
    }
}

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    AssertIsNotNull(image);
    AssertIsNotNull(image.Header);
    AssertIsNotNull(image.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. Nhiều cách để thiết lập Độ phân giải Tệp Psd không hoạt động**

{{< highlight csharp >}}
string output1 = "1560_1_output.psd";
string output2 = "1560_2_output.psd";
string output3 = "1560_3_output.psd";

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    newPsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    newPsd.VerticalResolution = 100;
    newPsd.HorizontalResolution = 100;
    newPsd.Save(output1);
}

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    newPsd.SetResolution(200, 200);
    newPsd.Save(output2);
}

using (PsdImage newPsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions psdOptions = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    newPsd.Save(output3, psdOptions);
}

using (var psdImage1 = (PsdImage)Image.Load(output1))
{
    var resResource = psdImage1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(100, resResource.VDpi.Integer);
    AreEqual(100, resResource.HDpi.Integer);
}

using (var psdImage2 = (PsdImage)Image.Load(output2))
{
    var resResource = psdImage2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(200, resResource.VDpi.Integer);
    AreEqual(200, resResource.HDpi.Integer);
}

using (var psdImage3 = (PsdImage)Image.Load(output3))
{
    var resResource = psdImage3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(resResource);
    AreEqual(300, resResource.VDpi.Integer);
    AreEqual(300, resResource.HDpi.Integer);
}

void IsNotNull(object obj)
{
    if (obj == null)
    {
        throw new NullReferenceException();
    }
}

void AreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1728. FontSettings.SetFontsFolders không hoạt động hoặc Aspose.PSD sử dụng font không chính xác**

{{< highlight csharp >}}
string src = "1728_Untitled-1.psd";
string fontsDir = "Fonts";
string outputPng = "1728_output.png";

FontSettings.SetFontsFolders(new string[] { fontsDir }, true);
using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            var textData = textLayer.TextData;
            textData.UpdateLayerData();
        }
    }

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1739. Để ngược. Sửa lỗi ngoại lệ tham chiếu Null khi lưu PsdImage khi có lớp Shape**

{{< highlight csharp >}}
string sourceFile = "ShapeInternalSolid.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    // Nên tải mà không có ngoại lệ

    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[1];

    if (shapeLayer.RawDataSettings == null)
    {
        throw new Exception("RawDataSettings không nên là null.");
    }
}
{{< /highlight >}}
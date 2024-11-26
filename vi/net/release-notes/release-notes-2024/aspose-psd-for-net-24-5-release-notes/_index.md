---
title: Aspose.PSD cho .NET 24.5 - Ghi chú phát hành
type: docs
weight: 80
url: /vi/net/aspose-psd-cho-net-24-5-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                         | **Danh mục** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [AI Format] Thêm hỗ trợ xử lý tập tin AI với tiêu đề EPSF                      | Tính năng      |
| PSDNET-1755 | Mặt nửa trong suốt được xử lý sai trong xem trước tập tin psd                        | Sửa lỗi      |
| PSDNET-1942 | Hiển thị Lớp Hình dạng một phần không chính xác                                        | Sửa lỗi      |
| PSDNET-1957 | Ngoại lệ mỗi khi lưu các tập tin PSD với kích thước lớn hơn 200 MB và kích thước lớn | Sửa lỗi      |
| PSDNET-1998 | Ngoại lệ khi lưu hình ảnh thất bại khi lưu thành tập tin PDF sau cập nhật từ 23.7 lên 24.3     | Sửa lỗi      |
| PSDNET-2033 | Sửa lỗi trong phương pháp GetFontInfoRecords cho các Phông chữ Trung Quốc                    | Sửa lỗi      |

## **Thay đổi API công khai**
# **API Thêm vào:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **API Đã xóa:**
- Không có

## **Các ví dụ về việc sử dụng:**

**PSDNET-1755. Mặt nửa trong suốt được xử lý sai trong xem trước tập tin psd**

{{< highlight csharp >}}
// Mặt nửa trong suốt được xử lý sai trong xem trước tập tin psd.
// BackgroundContents được gán thành Màu Trắng. Các vùng trong suốt nên có màu trắng.

string sourceFile = Path.Combine(baseFolder, "frog_nosymb.psd");
string outputFile = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(sourceFile))
{
    RawColor backgroundColor = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    backgroundColor.SetAsInt(argbValue); // Trắng

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = backgroundColor,
    };

    psdImage.Save(outputFile, psdOptions);
}
{{< /highlight >}}

**PSDNET-1897. [AI Format] Thêm hỗ trợ xử lý tập tin AI với tiêu đề EPSF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "example.ai");
string outputFilePath = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Các đối tượng không bằng nhau.");
    }
}

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    AssertAreEqual(image.Layers.Length, 2);
    AssertAreEqual(image.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[0].ColorIndex, -1);
    AssertAreEqual(image.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[1].ColorIndex, -1);

    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. Hiển thị Lớp Hình dạng một phần không chính xác**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ShapeLayerTest.psd");
string outputFile = Path.Combine(outputFolder, "ShapeLayerTest_output.psd");
const int ImgToPsdRatio = 256 * 65535;

using (var im = (PsdImage)Image.Load(sourceFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[2];
    IPath path = shapeLayer.Path;
    IPathShape[] pathShapes = path.GetItems();
    List<BezierKnotRecord> knotsList = new List<BezierKnotRecord>();
    foreach (IPathShape pathShape in pathShapes)
    {
        BezierKnotRecord[] knots = pathShape.GetItems();
        knotsList.AddRange(knots);
    }

    // Thay đổi thuộc tính của lớp
    var newShape = new PathShape();

    BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    shapeLayer.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(50, 490),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 490),
                    shapeLayer.Container.Size), // Điểm neo
                PointFToResourcePoint(
                    new PointF(150, 490),
                    shapeLayer.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(490, 150),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 50),
                    shapeLayer.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 20),
                    shapeLayer.Container.Size),
            },
        },
    };

    newShape.SetItems(bezierKnots);

    List<IPathShape> newShapes = new List<IPathShape>(pathShapes);
    newShapes.Add(newShape);

    IPathShape[] pathShapeNew = newShapes.ToArray();
    path.SetItems(pathShapeNew);

    shapeLayer.Update();

    im.Save(outputFile, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(outputFile))
{
    ShapeLayer shapeLayer = (ShapeLayer)im.Layers[2];
    IPath path = shapeLayer.Path;
    IPathShape[] pathShapes = path.GetItems();
    List<BezierKnotRecord> knotsList = new List<BezierKnotRecord>();
    foreach (IPathShape pathShape in pathShapes)
    {
        BezierKnotRecord[] knots = pathShape.GetItems();
        knotsList.AddRange(knots);
    }

    AssertAreEqual(3, pathShapes.Length);
    AssertAreEqual(42, shapeLayer.Left);
    AssertAreEqual(14, shapeLayer.Top);
    AssertAreEqual(1600, shapeLayer.Bounds.Width);
    AssertAreEqual(1086, shapeLayer.Bounds.Height);
}

Point PointFToResourcePoint(PointF point, Size imageSize)
{
    return new Point(
        (int)Math.Round(point.Y * (ImgToPsdRatio / imageSize.Height)),
        (int)Math.Round(point.X * (ImgToPsdRatio / imageSize.Width)));
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1957. Ngoại lệ mỗi khi lưu các tập tin PSD với kích thước lớn hơn 200 MB và kích thước lớn**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");
string outputFile = Path.Combine(outputFolder, "output_raw.psd");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Không nên xảy ra lỗi ở đây
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. Ngoại lệ khi lưu hình ảnh thất bại khi lưu thành tập tin PDF sau cập nhật từ 23.7 lên 24.3**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "CVFlor.psd");
string outputFile = Path.Combine(outputFolder, "_export.pdf");

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2033. Sửa lỗi trong phương pháp GetFontInfoRecords cho các Phông chữ Trung Quốc**

{{< highlight csharp >}}
var fontFolder = Path.Combine(baseFolder, "Font");
string sourceFile = Path.Combine(baseFolder, "bd-worlds-best-pink.psd");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { fontFolder }, true);
    FontSettings.UpdateFonts();

    using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
    {
        foreach (var layer in image.Layers)
        {
            var textLayer = layer as TextLayer;

            if (textLayer != null)
            {
                if (textLayer.Text == "best")
                {
                    // Không có sửa lỗi ở đây sẽ có ngoại lệ do phông chữ Tiếng Trung.
                    textLayer.UpdateText("THÀNH CÔNG");
                }
            }
        }
    }
}
finally
{
    FontSettings.Reset();
    FontSettings.UpdateFonts();
}
{{< /highlight >}}

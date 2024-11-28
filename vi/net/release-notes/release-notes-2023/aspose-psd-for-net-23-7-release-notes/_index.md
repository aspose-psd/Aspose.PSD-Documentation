---
title: Ghi chú bản phát hành Aspose.PSD cho .NET 23.7
type: tài-lieu
weight: 60
url: /vi/net/aspose-psd-cho-net-23-7-ghi-chu-ban-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa ghi chú bản phát hành cho [Aspose.PSD cho .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Khóa**     | **Tóm tắt**                                                                                                  | **Danh mục** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Thêm khả năng xuất mỗi lớp của Tệp PSD thành Tệp Gif Động                                        | Tính năng |
| PSDNET-1441 | Gán thuộc tính Fill của lớp Hình dạng từ tài nguyên vscg                                                       | Tính năng |
| PSDNET-1534 | Thêm các loại warp mới (cung & vòm)                                                                           | Tính năng |
| PSDNET-1543 | Thay đổi ứng dụng lưu Tệp PSD thành Aspose.PSD nếu thuộc tính UpdateMetadata được đặt thành true       | Tính năng |
| PSDNET-1567 | Tăng diện tích tính toán của hình warp                                                              | Tính năng |
| PSDNET-1471 | Lớp điều chỉnh Đen và Trắng xử lý độ trong suốt sai lầm                                           | Lỗi     |
| PSDNET-1505 | Thay Thành phần Nội dung SmartObject (khi tùy chọn AllowWarpRepaint được kích hoạt) rơi sau 2 phút tính toán | Lỗi     |
| PSDNET-1585 | Thêm khả năng lấy vị trí Thật sự Bên trái và Bên trên của Nhóm Lớp                                      | Lỗi     |
| PSDNET-1589 | Thay đổi kích thước của lớp không hoạt động đúng khi tệp psd có VogkResource với cấu trúc trong điểm | Lỗi     |
| PSDNET-1608 | TextBound không hoạt động như mong đợi                                                                         | Lỗi     |
| PSDNET-1612 | Thêm một lớp được tạo với hàm tạo mặc định vào hình ảnh PSD không thêm tài nguyên mặc định vào nó             | Lỗi     |
| PSDNET-1623 | Timeline.LoopesCount bị bỏ qua khi xuất thành GIF động                                               | Lỗi     |


## **Thay đổi API công cộng**
# **APIs Thêm:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **APIs Bị Xóa:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Ví dụ Sử dụng:**

**PSDNET-802. Thêm khả năng xuất mỗi lớp của Tệp PSD thành Tệp Gif Động**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Tạo khung cho mỗi lớp.
    int framesCount = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[framesCount];
    for (int i = 0; i < framesCount; i++)
    {
        frames[i] = new Frame();
        LayerState[] layerStates = new LayerState[framesCount];

        for (int j = 0; j < framesCount; j++)
        {
            layerStates[j] = new LayerState();
            layerStates[j].Enabled = i == j;
        }

        frames[i].LayerStates = layerStates;
    }

    timeline.Frames = frames;

    // Cập nhật trạng thái hiện tại
    Layer[] layers = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < framesCount; i++)
    {
        layers[i].IsVisible = states[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Gán thuộc tính Fill của lớp Hình dạng từ tài nguyên vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;
    fillSettings.Color = Color.Red;

    shapeLayer.Update();

    image.Save(outFile);
}

// Kiểm tra các thay đổi đã lưu
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    ColorFillSettings fillSettings = (ColorFillSettings)shapeLayer.Fill;

    AssertAreEqual(Color.Red, fillSettings.Color);

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Lớp điều chỉnh Đen và Trắng xử lý độ trong suốt sai lầm**

{{< highlight csharp >}}
string srcFile = "frog_nosymb.psd";
string outFile = "frog_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Kiểm tra các thay đổi đã lưu
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (blackWhiteAdjustmentLayer == null)
    {
        throw new Exception("Lớp 2 nên là BlackWhiteAdjustmentLayer");
    }

    image.Save(outFile);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1505. Thay Thành phần Nội dung SmartObject (khi tùy chọn AllowWarpRepaint được kích hoạt) rơi sau 2 phút tính toán**

{{< highlight csharp >}}
string sourceFile = "mug 4.psd";
string changeFile = "artwork for replace.png";
string outputFile = "export.png";

int newHeight = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer smartObjectLayer = (SmartObjectLayer)psdImage.Layers[3];

    var scale = (double)newHeight / smartObjectLayer.Height;
    var newWidth = (int)Math.Round(smartObjectLayer.Width * scale);

    PsdImage innerImage = new PsdImage(newWidth, newHeight);
    innerImage.SetResolution(72, 72);

    Stream innerStream = new FileStream(changeFile, FileMode.Open);
    Layer layer = new Layer(innerStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        innerImage.AddLayer(layer);

        smartObjectLayer.ReplaceContents(innerImage);
        smartObjectLayer.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        innerImage.Dispose();
        innerStream.Dispose();
        layer.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Thêm các loại warp mới (cung & vòm)**

{{< highlight csharp >}}
string sourceArcFile = "arc_warp.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_warp.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Thay đổi ứng dụng lưu Tệp PSD thành Aspose.PSD nếu thuộc tính UpdateMetadata được đặt thành true**

{{< highlight csharp >}}
string path = "output.psd";
using (var image = new PsdImage(100, 100))
{
    // Nếu bạn muốn công cụ tạo thay đổi, đảm bảo rằng thuộc tính "UpdateMetadata" được đặt thành true. Nó đã được đặt thành true theo mặc định.
    var psdOptions = new PsdOptions();
    psdOptions.UpdateMetadata = true;

    // Lưu hình ảnh
    image.Save(path, psdOptions);

    // Checking creator tool in code.
    var xmpData = image.XmpData;
    var basicPackage = image.XmpData.GetPackage(Namespaces.XmpBasic);

    // Ở đây sẽ là thông tin công cụ tạo đã được cập nhật.
    var currentCreatorTool = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Tăng diện tích tính toán của hình warp**

{{< highlight csharp >}}
string sourceFile = "mug4_warp.psd";
string outputFile = "mug4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Thêm khả năng lấy vị trí Thật sự Bên trái và Bên trên của Nhóm Lớp**

{{< highlight csharp >}}
string sourceFile = "layerGroupFigures.psd";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Các đối tượng không bằng nhau.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    var layers = image.Layers;

    for (int i = 0; i < layers.Length; i++)
    {
        var layer = layers[i];

        if (layer is LayerGroup)
        {
            // Lấy LayerGroup.
            var group = (LayerGroup)layer;

            var expectedLeft = int.MaxValue;
            var expectedTop = int.MaxValue;
            var expectedRight = 0;
            var expectedBottom = 0;

            // Tính toán vị trí Thật sự Bên trái, Bên trên, Bên phải và Bên dưới.
            foreach (var innerLayer in group.Layers)
            {
                if (innerLayer is AdjustmentLayer || innerLayer.Bounds.IsEmpty)
                {
                    continue;
                }

                expectedLeft = Math.Min(expectedLeft, innerLayer.Left);
                expectedTop = Math.Min(expectedTop, innerLayer.Top);
                expectedRight = Math.Max((expectedLeft + group.Width), (innerLayer.Left + innerLayer.Width));
                expectedBottom = Math.Max((expectedTop + group.Height), (innerLayer.Top + innerLayer.Height));
            }

            // LayerGroup Left, Top, Right, and Bottom positions are calculated properly now.
            AssertAreEqual(group.Left, expectedLeft);
            AssertAreEqual(group.Top, expectedTop);
            AssertAreEqual(group.Right, expectedRight);
            AssertAreEqual(group.Bottom, expectedBottom);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Thay Đổi kích thước của lớp không hoạt động đúng khi tệp psd có VogkResource với cấu trúc trong điểm**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer layer = image.Layers[0];

        layer.Resize(50, 50);

        AssertAreEqual(layer.Height, 50);
        AssertAreEqual(layer.Width, 50);
    }
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Các đối tượng không bằng nhau.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound is not working as expected**

{{< highlight csharp >}}
string sourceFile = "input_Test_forTicket.psd";
string outFile = "out_1608.psd";

Size newTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //Step: Replace text
    TextLayer textLayer = (TextLayer)psdImage.Layers[3];
    textLayer.TextData.Items[0].Text = "Text test replaced";

    //Step: Update TextBoundBox
    textLayer.TextData.UpdateLayerData();
    newTextBox = new Size((int)Math.Ceiling(textLayer.TextBoundBox.Width), textLayer.Height);

    textLayer.TextBoundBox = new Aspose.PSD.RectangleF(PointF.Empty, newTextBox);
    textLayer.TextData.UpdateLayerData();

    psdImage.Save(outFile);
}

// Check changes
using (var psdImage = (PsdImage)Image.Load(outFile))
{
    Txt2Resource txt2Resource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    string textData = Encoding.GetEncoding("Windows-1251").GetString(txt2Resource.Data);

    string search = "<< /0 << /1 << /0 ["; // specific character set to find textBox value in this file.

    int startIndex = textData.IndexOf(search) + search.Length;
    int endIndex = textData.IndexOf("]", startIndex);
    string boxItems = textData.Substring(startIndex, endIndex - startIndex);

    string height = newTextBox.Height.ToString("0.0####").Replace(",", ".");
    string width = newTextBox.Width.ToString("0.0####").Replace(",", ".");

    if (!boxItems.Contains(height) || !boxItems.Contains(width))
    {
        throw new Exception("TextBox not updated.");
    }
}
{{< /highlight >}}

**PSDNET-1612. Adding a layer created with default constructor to PSD image does not add default resources to it**

{{< highlight csharp >}}
string output = "newLayer.psd";

using (var psdImage = new PsdImage(500, 500))
{
    var layer = new Layer();
    psdImage.AddLayer(layer);

    LyidResource lyidResource = (LyidResource)FindResource(LyidResource.TypeToolKey, layer.Resources);

    int layerId = lyidResource.Value; // Was NullReferenceException

    psdImage.Save(output);
}
    
LayerResource FindResource(int resType, LayerResource[] resources)
{
    if (resources != null)
    {
        foreach (var layerResource in resources)
        {
            if (layerResource.Key == resType)
            {
                return layerResource;
            }
        }
    }

    return null;
}
{{< /highlight >}}

**PSDNET-1623. Timeline.LoopesCount is ignored when exporting to animated GIF**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputGif = "out_4_animated.psd.gif";

using (var psdImage = (Psd
---
title: Aspose.PSD cho .NET 20.3 - Các ghi chú phát hành
type: docs
weight: 100
url: /vi/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú phát hành cho [Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-188|Hỗ trợ của .Net Core|Tính năng|
|PSDNET-523|Chuyển đổi tập tin Adobe Illustrator thành PDF|Tính năng|
|PSDNET-212|Thêm khả năng hiển thị các kiểu khác nhau trong một lớp văn bản|Tính năng|
|PSDNET-144|Hỗ trợ của Black and White Adjustment Layer|Tính năng|
|PSDNET-233|Thêm hỗ trợ xuất định dạng AI (Phiên bản 8) sang các định dạng khác|Tính năng|
|PSDNET-540|Hỗ trợ xử lý chế độ trộn PassThrough (Chỉ dành cho Nhóm Lớp)|Tính năng|
|PSDNET-539|Ngoại lệ: Không thể tải hình ảnh khi tải hình ảnh có Tên Unicode Alpha Rỗng|Lỗi|
|PSDNET-541|Đầu ra không chính xác sau khi thay đổi tính hiển thị của một Nhóm Lớp|Lỗi|
|PSDNET-516|Ngoại lệ khi tải hình ảnh PSD: Phần màu (Tài nguyên Đổ Bóng) phải chứa 3 thành phần màu cho RGB hoặc 4 thành phần màu cho CMYK|Lỗi|
|PSDNET-536|Ngoại lệ nếu cố vẽ trên lớp mới tạo nếu phiên bản Đơn giản của Constructor được sử dụng|Lỗi|

## **Thay đổi API công cộng**
# **API được thêm vào:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **API bị Loại bỏ:**
- None

## **Ví dụ về cách sử dụng:**
**PSDNET-523. Chuyển đổi tập tin Adobe Illustrator thành PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Thêm khả năng hiển thị các kiểu khác nhau trong một lớp văn bản**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // chỉnh sửa kiểu văn bản "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // chỉnh sửa kiểu văn bản "2\r"

    newPortions[2].Style.FauxBold = true; // chỉnh sửa kiểu văn bản "Bold"

    newPortions[3].Style.FauxItalic = true; // chỉnh sửa kiểu văn bản "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // chỉnh sửa kiểu văn bản "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // chỉnh sửa kiểu văn bản "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Thêm hỗ trợ xuất định dạng AI (Phiên bản 8) sang các định dạng khác**

{{< highlight java >}}

 // Ví dụ về việc xuất tệp AI sang định dạng PSD và PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Hỗ trợ xử lý chế độ trộn PassThrough (Chỉ dành cho Nhóm Lớp)**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Không có lớp thứ 23.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "Lớp thứ 23 không phải là nhóm lớp.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Tên lớp thứ 23 không phải là 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Lớp AdjustmentGroup phải có chế độ trộn 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Cập nhật văn bản lớp văn bản gây ra ngoại lệ**

{{< highlight java >}}

 // Cập nhật văn bản lớp văn bản gây ra ngoại lệ

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Kiểm tra";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Lưu hình ảnh PSD sau khi thực hiện thao tác RotateFlip tạo tập tin bị hỏng không thể mở được.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Nên được thực thi mà không có ngoại lệ

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Không làm gì

}

{{< /highlight >}}

**PSDNET-539. Ngoại lệ: Load hình ảnh thất bại khi tải hình ảnh có Tài nguyên Tên Unicode Rỗng**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Ở đây chúng ta không nên có ngoại lệ

{

    // không làm gì

}

{{< /highlight >}}

**PSDNET-541. Đầu ra không chính xác sau khi thay đổi tính hiển thị của một Nhóm Lớp**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// thực hiện thay đổi trong tên lớp và lưu nó

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Tắt tất cả mọi thứ bên trong một nhóm

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Ngoại lệ khi tải hình ảnh PSD: Phần màu (Tài nguyên Đổ Bóng) phải chứa 3 thành phần màu cho RGB hoặc 4 thành phần màu cho CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Ở đây chúng ta không nên có ngoại lệ

{

    // không làm gì

}

{{< /highlight >}}

**PSDNET-536. Ngoại lệ nếu cố vẽ trên lớp mới tạo nếu phiên bản Đơn giản của Constructor được sử dụng**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // vẽ hình chữ nhật với công cụ Pen

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // vẽ hình chữ nhật khác với Solid Brush trong màu Xanh

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

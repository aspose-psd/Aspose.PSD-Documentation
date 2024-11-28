---
title: Aspose.PSD cho Java 20.3 - Ghi chú phát hành
type: docs
weight: 10
url: /vi/java/aspose-psd-cho-java-20-3-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Thể loại**|
| :- | :- | :- |
|PSDJAVA-133|Chuyển đổi tệp Adobe Illustrator thành PDF|Tính năng|
|PSDJAVA-134|Thêm khả năng vẽ các kiểu khác nhau trong một lớp văn bản|Tính năng|
|PSDJAVA-135|Hỗ trợ Layer Điều chỉnh Đen và Trắng|Tính năng|
|PSDJAVA-137|Thêm hỗ trợ xuất định dạng AI (Phiên bản 8) sang các định dạng khác|Tính năng|
|PSDJAVA-138|Hỗ trợ xử lý Chế độ Trộn Luôn Giữ (Chỉ sử dụng cho Nhóm Lớp)|Tính năng|
|PSDJAVA-136|Ngoại lệ: Lỗi tải hình ảnh khi tải hình ảnh với Tên Alpha Unicode trống|Lỗi|
|PSDJAVA-139|Đầu ra không chính xác sau khi thay đổi tính hiển thị của một Nhóm Lớp|Lỗi|
|PSDJAVA-140|Ngoại lệ khi tải hình ảnh PSD: Mục màu (Tài nguyên DropShadow) phải chứa 3 thành phần màu cho RGB hoặc 4 thành phần màu cho CMYK|Lỗi|
|PSDJAVA-141|Ngoại lệ nếu cố vẽ trên lớp mới tạo nếu phiên bản đơn giản của Constructor được sử dụng|Lỗi|
# **Thay đổi API công cộng**
# **API Đã Thêm:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **API Đã Xóa:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Ví dụ về cách sử dụng:**
**PSDJAVA-133. Chuyển đổi tệp Adobe Illustrator thành PDF**

{{< highlight java >}}

 String inFile = "rect2_color.ai";

String outFile = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(inFile);

try

{

    aiImage.save(outFile, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Thêm khả năng vẽ các kiểu khác nhau trong một lớp văn bản**

{{< highlight java >}}

 String inFilePath = "text212.psd";

String outFilePath = "Output_text212.psd";

PsdImage image = (PsdImage)Image.load(inFilePath);

try

{

    TextLayer textLayer = (TextLayer)image.getLayers()[1];

    IText textData = textLayer.getTextData();

    ITextStyle defaultStyle = textData.producePortion().getStyle();

    ITextParagraph defaultParagraph = textData.producePortion().getParagraph();

    defaultStyle.setFillColor(Color.getDimGray());

    defaultStyle.setFontSize(51);

    textData.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // chỉnh sửa kiểu văn bản "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // chỉnh sửa kiểu văn bản "2\r"

    newPortions[2].getStyle().setFauxBold(true); // chỉnh sửa kiểu văn bản "Bold"

    newPortions[3].getStyle().setFauxItalic(true); // chỉnh sửa kiểu văn bản "Italic\r"

    newPortions[3].getStyle().setBaselineShift(-25); // chỉnh sửa kiểu văn bản "Italic\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // chỉnh sửa kiểu văn bản "Lowercasetext"

    for (ITextPortion newPortion : newPortions)

    {

        textData.addPortion(newPortion);

    }

    textData.updateLayerData();

    image.save(outFilePath);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Hỗ trợ Layer Điều chỉnh Đen và Trắng**

{{< highlight java >}}

 // Ví dụ về việc hỗ trợ thêm lớp điều chỉnh đen và trắng trong quá trình chạy.

String inFileName = "Stripes.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("BlackWhiteAdjustmentLayer");

    newLayer.setReds(22);

    newLayer.setYellows(92);

    newLayer.setGreens(70);

    newLayer.setCyans(79);

    newLayer.setBlues(7);

    newLayer.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Ví dụ về hỗ trợ lớp điều chỉnh đen và trắng.

inFileName = "BlackWhiteAdjustmentLayerStripesMask.psd";

outFileName = "Output" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer blwhLayer = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    blwhLayer.setReds(15);

    blwhLayer.setYellows(25);

    blwhLayer.setGreens(35);

    blwhLayer.setCyans(10);

    blwhLayer.setBlues(50);

    blwhLayer.setMagentas(105);

    blwhLayer.setUseTint(true);

    blwhLayer.setBwPresetKind(4);

    blwhLayer.setBlackAndWhitePresetFileName("bwPresetFileName");

    blwhLayer.setTintColorRed(60);

    blwhLayer.setTintColorGreen(80);

    blwhLayer.setTintColorBlue(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Thêm hỗ trợ xuất định dạng AI (Phiên bản 8) sang các định dạng khác**

{{< highlight java >}}

 // Ví dụ về việc xuất tệp AI sang định dạng PSD và PNG

String inFileName = "form_8.ai";

String outFileNamePrefix = "form_8_export";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefix + ".psd", new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefix + ".png", pngOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Hỗ trợ xử lý Chế độ Trộn Luôn Giữ (Chỉ sử dụng cho Nhóm Lớp)**

{{< highlight java >}}

 class LocalScope

{

    void assertIsTrue(boolean condition, String message)

    {

        if (!condition)

        {

            throw new FormatException(message);

        }

    }

}

LocalScope localScope = new LocalScope();

String inFileName = "Apple.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    localScope.assertIsTrue(image.getLayers().length >= 23, "Không có lớp thứ 23.");

    LayerGroup layer = (LayerGroup)image.getLayers()[23];

    localScope.assertIsTrue(layer != null, "Lớp thứ 23 không phải là lớp nhóm.");

    localScope.assertIsTrue(layer.getName().equals("AdjustmentGroup"), "Tên lớp thứ 23 không phải là 'AdjustmentGroup'.");

    localScope.assertIsTrue(layer.getBlendModeKey() == BlendMode.PassThrough, "Lớp Nhóm Điều chỉnh phải có chế độ trộn 'pass through'.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("OutputApple.png", pngOptions);

    layer.setBlendModeKey(BlendMode.Normal);

    image.save("Normal" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormalOutputApple.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Ngoại lệ: Lỗi tải hình ảnh khi tải hình ảnh với Tên Alpha Unicode trống**

{{< highlight java >}}

 String inFilePath = "apple.psd";

PsdImage psdImage = null;

try

{

    // Ở đây chúng ta không nên có ngoại lệ

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Đầu ra không chính xác sau khi thay đổi tính hiển thị của một Nhóm Lớp**

{{< highlight java >}}

 String inFileName = "input.psd";

String outFileName = "output.psd";

// Thực hiện thay đổi tên các lớp và lưu tệp

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer layer = image.getLayers()[i];

        // Tắt tất cả mọi thứ bên trong một nhóm

        if (layer instanceof LayerGroup)

        {

            layer.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Ngoại lệ khi tải hình ảnh PSD: Mục màu (Tài nguyên DropShadow) phải chứa 3 thành phần màu cho RGB hoặc 4 thành phần màu cho CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

PsdImage image = null;

try

{

    image = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (image != null) image.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Ngoại lệ nếu cố vẽ trên lớp mới tạo nếu phiên bản đơn giản của Constructor được sử dụng**

{{< highlight java >}}

 String outputFile = "output.psd";

int width = 100;

int height = 100;

PsdImage image = new PsdImage(width, height);

try

{

    Layer layer = new Layer();

    layer.setBottom(height);

    layer.setRight(width);

    image.addLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.clear(Color.getYellow());

    // vẽ một hình chữ nhật với công cụ Pen

    graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // vẽ một hình chữ nhật khác với Solid Brush màu Xanh

    graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}
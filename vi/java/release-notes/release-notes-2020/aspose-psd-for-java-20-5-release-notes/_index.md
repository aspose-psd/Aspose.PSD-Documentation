---
title: Aspose.PSD cho Java 20.5 - Ghi chú phát hành
type: docs
weight: 40
url: /vi/java/aspose-psd-cho-java-20-5-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}} Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-cho-java-20.5/) {{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDJAVA-188|Hỗ trợ tiến trình chuyển đổi tài liệu|Tính năng|
|PSDJAVA-197|Hỗ trợ Lưu hình ảnh PSD Chế độ màu Xám với 16 bít mỗi kênh|Tính năng|
|PSDJAVA-198|Hỗ trợ Tài nguyên Nvrt (Tài nguyên Lớp Điều chỉnh Đảo Ngược)|Tính năng|
|PSDJAVA-200|Hỗ trợ Mặt nạ Lớp cho Nhóm Lớp|Tính năng|
|PSDJAVA-195|Khắc phục lỗi lưu hình ảnh PSD với Chế độ màu Xám 16 bít mỗi kênh sang định dạng PSD RGB 16 bit mỗi kênh|Lỗi|
|PSDJAVA-196|Khắc phục lỗi lưu hình ảnh PSD với Chế độ màu Xám 16 bít mỗi kênh sang định dạng PSD Xám 8 bit mỗi kênh|Lỗi|
|PSDJAVA-199|Căn chỉnh Văn bản thông qua ITextPortion không hoạt động cho ngôn ngữ từ phải qua trái. Tệp đầu ra bị hỏng.|Lỗi|
|PSDJAVA-201|Ngoại lệ khi cố gắng mở tệp Psd cụ thể với Màu LAB và 8 bit/kênh|Lỗi|
# **Thay Đổi Công cộng API**
# **API Đã Thêm:**
- Không có
## **API Đã Xoá:**
- Không có
# **Ví dụ về cách sử dụng:**

**PSDJAVA-188. Hỗ trợ tiến trình chuyển đổi tài liệu**

{{< highlight java >}}

 // Một ví dụ về việc sử dụng trình xử lý tiến trình cho các hoạt động tải và lưu.

// Chương trình sử dụng các tùy chọn lưu khác nhau để kích hoạt sự kiện tiến trình.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Tạo trình xử lý tiến trình ghi thông tin tiến trình ra bảng điều khiển

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s trên tổng số %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Đang tải Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Liên kết trình xử lý tiến trình để hiển thị tiến trình tải

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Tải PSD bằng các tùy chọn tải cụ thể

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Đang lưu Apple.psd sang định dạng PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Làm cho hình ảnh đầu ra có màu sắc và không trong suốt

    pngOptions.setColorType(PngColorType.Truecolor);

    // Liên kết trình xử lý tiến trình để hiển thị tiến trình lưu

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Chuyển đổi PSD sang PNG với các đặc điểm cụ thể

    image.save(outputStream, pngOptions);

    System.out.println("---------- Đang lưu Apple.psd sang định dạng PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Làm cho hình ảnh PSD đầu ra có màu sắc

    psdOptions.setColorMode(ColorModes.Rgb);

    // Đặt một channel cho mỗi màu (đỏ, xanh lá cây và xanh da trời) cùng một channel hợp thành

    psdOptions.setChannelsCount((short)4);

    // Liên kết trình xử lý tiến trình để hiển thị tiến trình lưu

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Lưu bản sao của PSD với các đặc điểm cụ thể

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Hỗ trợ Lưu hình ảnh PSD Chế độ màu Xám với 16 bít mỗi kênh**

{{< highlight java >}}

 // Một ví dụ về việc áp dụng các kết hợp khác nhau của chế độ màu, số bit mỗi kênh, số kênh

// đếm và nén cho các lớp cụ thể.

// Làm cho một phương thức có thể truy cập từ phạm vi cục bộ

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Tải một PSD xám 16-bit đã được xác định trước

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Vẽ viền xám bên trong xung quanh lớp

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Lưu bản sao của PSD với các đặc điểm cụ thể

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Tải PSD được lưu

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Chuyển đổi PSD đã lưu thành một hình ảnh PNG xám

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // Không nên có ngoại lệ ở đây

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Hỗ trợ Tài nguyên Nvrt (Tài nguyên Lớp Điều chỉnh Đảo Ngược)**

{{< highlight java >}}

 // Một ví dụ về việc tìm NvrtResource của một lớp điều chỉnh đảo ngược.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Tải một PSD đã được xác định trước chứa một lớp điều chỉnh đảo ngược

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Thử tìm tài nguyên của lớp điều chỉnh đảo ngược

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Tìm thấy NvrtResource

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Hỗ trợ Mặt nạ Lớp cho Nhóm Lớp**

{{< highlight java >}}

 // Một ví dụ về hỗ trợ mặt nạ lớp cho nhóm lớp. Chương trình tải và lưu PSD

// sang các định dạng đầu ra khác nhau mà không ném ra ngoại lệ.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Tải một PSD đã được xác định trước chứa mặt nạ lớp cho nhóm lớp

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Chuyển PSD đã tải sang PNG

    input.save(outputPng, new PngOptions());

    // Lưu một bản sao của PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Khắc phục lỗi lưu hình ảnh PSD với Chế độ màu Xám 16 bít mỗi kênh sang định dạng PSD RGB 16 bit mỗi kênh**

{{< highlight java >}}

 // Một ví dụ về chuyển đổi một PSD xám 16 bit sang một PSD RGB 16 bit và sau đó trở lại

// 16 bit xám nhưng là một hình ảnh raster.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Tải một PSD xám 16 bit đã được xác định trước

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Vẽ viền xám bên trong xung quanh lớp

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Lưu bản sao của PSD với chế độ màu được thay đổi thành RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Tải PSD đã lưu

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Chuyển đổi PSD đã lưu thành một hình ảnh PNG xám

    image1.save(pngExportPath, pngOptions); // Không nên có ngoại lệ ở đây

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Khắc phục lỗi lưu hình ảnh PSD với Chế độ màu Xám 16 bít mỗi kênh sang định dạng PSD Xám 8 bit mỗi kênh**

{{< highlight java >}}

 // Một ví dụ về chuyển đổi một PSD xám 16 bit sang một PSD xám 8 bit và sau đó thành

// một hình ảnh raster xám 8 bit.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Tải một PSD xám 16 bit đã được xác định trước

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Vẽ viền xám bên trong xung quanh lớp

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Lưu bản sao của PSD với số kênh được thay đổi thành 8 bit

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Tải PSD đã lưu

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Chuyển đổi PSD đã lưu thành một hình ảnh PNG xám

    image1.save(pngExportPath, pngOptions); // Không nên có ngoại lệ ở đây

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Căn chỉnh Văn bản thông qua ITextPortion không hoạt động cho ngôn ngữ từ phải qua trái. Tệp đầu ra bị hỏng.**

{{< highlight java >}}

 // Một ví dụ về việc căn chỉnh lớp văn bản RTL thông qua ITextPortion. Chương trình sửa đổi

// một lớp văn bản RTL hiện có trong PSD đã tải và lưu một bản sao của tài
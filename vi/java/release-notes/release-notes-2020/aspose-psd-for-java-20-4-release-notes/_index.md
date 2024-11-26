---
title: Ghi chú về Aspose.PSD cho Java 20.4
type: docs
weight: 30
url: /zh/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}}Trang này chứa ghi chú về [Aspose.PSD cho Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/){{% /alert %}}

| **Khóa** | **Tóm tắt** | **Danh mục** |
| :- | :- | :- |
| PSDJAVA-156 | Hỗ trợ của tài nguyên 'Vector Origination Data' | Tính năng |
| PSDJAVA-171 | Hỗ trợ của lclrResource (Thiết lập màu Bảng) | Tính năng |
| PSDJAVA-157 | Hỗ trợ các thuộc tính từ dữ liệu LengthRecord. (Các thao tác đường dân (các thao tác logic), chỉ số của hình dạng trong lớp, số lượng hồ nơi bézier) | Tính năng |
| PSDJAVA-158 | Hỗ trợ Mảng Mục tiêu Hình ảnh #1010 Màu nền | Tính năng |
| PSDJAVA-161 | Thêm các Lớp Đổ bó màu khi chạy | Tính năng |
| PSDJAVA-168 | Hỗ trợ Mảng Mục tiêu Hình ảnh #1009 Thông tin biên | Tính năng |
| PSDJAVA-169 | Hỗ trợ các Lớp trong Các Tệp Định dạng AI | Tính năng |
| PSDJAVA-163 | Hỗ trợ Đọc và Chỉnh sửa Hiệu ứng Lớp Đè Lên đồng màu Gradient | Tính năng |
| PSDJAVA-164 | Kết xuất Hiệu ứng Lớp Đè Lên đồng màu Gradient | Tính năng |
| PSDJAVA-149 | Aspose.PSD cho lỗi java khi lấy thuộc tính textData.items của lớp văn bản | Sửa lỗi |
| PSDJAVA-166 | Sửa lỗi lưu hình ảnh PSD với Chế độ Màu Xám và 16 bit mỗi kênh sang định dạng PSD xám | Sửa lỗi |
| PSDJAVA-167 | Sửa lỗi lưu hình ảnh PSD với Chế độ Màu Xám và 16 bit mỗi kênh sang định dạng PNG | Sửa lỗi |
| PSDJAVA-159 | Các thay đổi thuộc tính GradientOverlayEffect.BlendMode không được hiển thị trong Photoshop. | Sửa lỗi |

## **Thay đổi API công cộng**

### **API đã thêm:**

- M: com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M: com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M: com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float, float)
- T: com.aspose.psd.fileformats.psd.PsdVersion
- F: com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F: com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F: com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M: com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short, byte[], byte[])
- M: com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M: com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k, com.aspose.psd.IColorPalette)
- M: com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M: com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M: com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M: com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[], com.aspose.psd.fileformats.psd.layers.text.ITextStyle, com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M: com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T: com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T: com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M: com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M: com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream, boolean)

## **API đã xóa:**

- M: com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k, com.aspose.psd.IColorPalette)
- M: com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)

# **Ví dụ về cách sử dụng:**

**PSDJAVA-156. Hỗ trợ của tài nguyên 'Vector Origination Data'**

{{< highlight java >}}
/*

Một ví dụ về việc đọc và chỉnh sửa một tài nguyên Nguyên bản Vectơ.

*/

// Giữ các phương pháp trong phạm vi cục bộ cho sự đơn giản

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("Không tìm thấy VogkResource.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Tải một tệp PSD chứa một nguồn nguyên mẫu VOGK đã được xác định trước

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Tìm tài nguyên Vogk đầu tiên trong tài nguyên của lớp đã xác định trước

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Xác minh các thuộc tính nguồn nguyên mẫu

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("Tài nguyên Vogk bị đọc sai.");

    }

    // Chỉnh sửa một số thuộc tính của nguồn nguyên mẫu

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Lưu một bản sao đã chỉnh sửa của tệp PSD đã tải trên đường dẫn

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Hỗ trợ của lclrResource (Thiết lập màu Bảng)**

{{< highlight java >}}
/*

Một ví dụ về việc sử dụng Màu Bảng Lớp để làm nổi bật trực quan các lớp. Ví dụ, bạn có thể

cập nhật một số lớp trong PSD sau đó nổi bật bằng màu lớp mà bạn muốn thu hút

sự chú ý.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // Tài nguyên lclr luôn tồn tại trong danh sách tài nguyên tệp psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Màu Bảng đã được đọc sai");

                }

                // Đảo ngược màu tời trình bày. Thiết lập nền màu lớp

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Trong tệp, màu của các lớp được làm nổi bật theo thứ tự này

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// Tải một tệp PSD chứa một nguồn màu đã xác định trước

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Tải một tệp PSD vừa lưu

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Đảo ngược màu

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Hỗ trợ các thuộc tính từ dữ liệu LengthRecord. (Các thao tác đường dẫn (các thao tác logic), chỉ số của hình dạng trong lớp, số lượng hồ nơi bézier)**

{{< highlight java >}}
/*

Một ví dụ về việc thay đổi các thao tác đường dẫn khi làm việc với hình dạng. Chương trình đọc

một số hồ sơ đường dẫn vectơ đã xác định trước (LengthRecord) và thay đổi các thao tác đường dẫn của họ sau đó lưu

một bản sao đã chỉnh sửa của tài liệu dưới dạng tệp PSD mới.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Tải một tệp PSD chứa một nguồn vsms đã xác định trước

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Tìm VsmsResource đầu tiên trong tài nguyên của lớp đã xác định trước

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Thay đổi cách kết hợp các hình dạng

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Lưu một bản sao đã chỉnh sửa của tệp PSD đã tải trên đường dẫn

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Hỗ trợ Mảng Mục tiêu Hình ảnh #1010 Màu nền**

{{< highlight java >}}
/*

Một ví dụ về việc đọc và chỉnh sửa một tài nguyên màu nền.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Tải một tệp PSD chứa một màu nền đã xác định trước

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Không tìm thấy Tài nguyên Màu Nền");

    }

    // Cập nhật màu của tài nguyên màu nền

    backgroundColorResource.setColor(Color.getDarkRed());

    // Lưu một bản sao đã chỉnh sửa của tệp PSD đã tải trên đường dẫn

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Thêm các Lớp Đổ bó màu khi chạy**
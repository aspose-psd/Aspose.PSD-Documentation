---
title: Aspose.PSD cho Java 20.7 - Ghi chú phát hành
type: docs
weight: 50
url: /vi/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} Trang này chứa ghi chú phát hành cho [Aspose.PSD for Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDJAVA-231|Hỗ trợ thêm Phần hiệu ứng Stroke tại thời gian chạy|Tính năng|
|PSDJAVA-249|Hỗ trợ tài nguyên lnk2 / lnk3 (Tài nguyên của Lớp Đối tượng Thông minh)|Tính năng|
|PSDJAVA-247|Thay đổi thông báo ngoại lệ khi cố gắng mở các định dạng không được hỗ trợ như ảnh|Cải tiến|
|PSDJAVA-235|Nếu chúng tôi lưu tệp PSD sau khi tạo Nhóm Lớp mới, chúng tôi nhận được cảnh báo Photoshop khi mở tệp.|Lỗi|
|PSDJAVA-236|Không thể lưu LayerMask|Lỗi|
|PSDJAVA-237|Clipping mask không áp dụng cho thư mục|Lỗi|
|PSDJAVA-238|Không thể mở tệp với Aspose.PSD cho Java|Lỗi|
|PSDJAVA-239|Ngoại lệ lưu hình ảnh thất bại khi chuyển đổi từ PSD sang PDF|Lỗi|
|PSDJAVA-240|Phép cắt làm cho đường cắt không hợp lệ trong hình ảnh PSD|Lỗi|
|PSDJAVA-241|Ngoại lệ NullReference khi cố gắng lưu Tệp PSD cụ thể với Phần hiệu ứng Bóng đổ|Lỗi|
|PSDJAVA-243|Aspose.PSD trả về true trên Image.CanLoad(pdfStream)|Lỗi|
|PSDJAVA-244|Lớp không render được trong tệp PNG đã tạo|Lỗi|
|PSDJAVA-245|Ngoại lệ khi truy cập TextData|Lỗi|
|PSDJAVA-246|Ngoại lệ ImageSaveException khi lưu PSD|Lỗi|

# **Thay Đổi API Công Khai**
# **API Đã Thêm:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **API Đã Xóa:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **Ví dụ Sử Dụng:**

**PSDJAVA-231. Hỗ trợ thêm Phần hiệu ứng Stroke tại thời gian chạy**
{{< highlight java >}}
// Ví dụ này cho thấy cách thêm phần hiệu ứng Stroke (viền) vào các lớp hiện có của tệp PSD trong Java.
// Có ba loại viền: màu, gradient và hình mẫu. Mỗi loại có
// ba cách (vị trí) mà viền được vẽ: bên trong, ở giữa và bên ngoài.
// Ví dụ này chỉ ra cách sử dụng tất cả các trường hợp này.
 
String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";
 
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;
 
    // 1. Thêm Tô màu, ở vị trí Bên trong
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 2. Thêm Tô màu, ở vị trí Bên ngoài
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 3. Thêm Tô màu, ở vị trí Chính giữa
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 4. Thêm Đổ màu Gradient, ở vị trí Bên trong
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);
 
    // 5. Thêm Đổ màu Gradient, ở vị trí Bên ngoài
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);
 
    // 6. Thêm Đổ màu Gradient, ở vị trí Chính giữa
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);
 
    // 7. Thêm Đổ màu Hình mẫu, ở vị trí Bên trong
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);
 
    // 8. Thêm Đổ màu Hình mẫu, ở vị trí Bên ngoài
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);
 
    // 9. Thêm Đổ màu Hình mẫu, ở vị trí Chính giữa
    strokeEffect = psdImage.getLayers()[9].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Center);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(75);
 
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**PSDJAVA-249. Hỗ trợ tài nguyên lnk2 / lnk3 (Tài nguyên của Lớp Đối tượng Thông minh)**
{{< highlight java >}}
// Ví dụ này demo làm thế nào để làm việc với tài nguyên đối tượng thông minh (cơ bản là Lnk2Resource).
// Chương trình tải và xuất các đối tượng thông minh từ một số tài liệu Photoshop đến
// các định dạng tệp raster. Code cũng demo việc sử dụng các phương thức công cộng của Lnk2Resource.
 
class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("Giá trị thực %s không bằng với kỳ vọng %s.", actual, expected));
        }
    }
 
    // Lưu dữ liệu của một đối tượng thông minh vào tệp PSD
    void saveSmartObjectData(String filePath, byte[] data)
    {
        FileStreamContainer container = FileStreamContainer.createFileStream(filePath, false);
        try
        {
            container.write(data);
        }
        finally
        {
            container.dispose();
        }
    }
 
    // Nạp dữ liệu mới cho đối tượng thông minh từ một tệp
    byte[] loadNewData(String filePath)
    {
        FileStreamContainer container = FileStreamContainer.openFileStream(filePath);
        try
        {
            return container.toBytes();
        }
        finally
        {
            container.dispose();
        }
    }
 
    // Lấy và thiết lập các thuộc tính của Lnk2 / Lnk3 Resource Lnk và các nguồn dữ liệu LiFD trong hình ảnh PSD
    void exampleOfLnk2ResourceSupport(
            String fileName,
            int dataSourceCount,
            int length,
            int newLength,
            Object[] dataSourceExpectedValues)
    {
        String srcPsdPath = fileName;
        String dstPsdPath = "out_" + fileName;
 
        PsdImage image = (PsdImage)Image.load(srcPsdPath);
        try
        {
            // Tìm kiếm cho Lnk2Resource
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;
 
                    // Xác minh thuộc tính của Lnk2Resource
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);
 
                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                                               // Xác minh và thay đổi các thuộc tính của LiFdDataSource
                        LiFdDataSource lifdSource = lnk2Resource.get_Item(i);
                        Object[] expected = (Object[])dataSourceExpectedValues[i];
                        assertAreEqual(LinkDataSourceType.liFD, lifdSource.getType());
                        assertAreEqual(expected[0], lifdSource.getUniqueId().toString());
                        assertAreEqual(expected[1], lifdSource.getOriginalFileName());
                        assertAreEqual(expected[2], lifdSource.getFileType().trim());
                        assertAreEqual(expected[3], lifdSource.getFileCreator().trim());
                        assertAreEqual(expected[4], lifdSource.getData().length);
                        assertAreEqual(expected[5], lifdSource.getAssetModTime());
                        assertAreEqual(expected[6], lifdSource.getChildDocId());
                        assertAreEqual(expected[7], lifdSource.getVersion());
                        assertAreEqual(expected[8], lifdSource.hasFileOpenDescriptor());
                        assertAreEqual(expected[9], lifdSource.getLength());
 
                        if (lifdSource.hasFileOpenDescriptor())
                        {
                            assertAreEqual(-1, lifdSource.getCompId());
                            assertAreEqual(-1, lifdSource.getOriginalCompId());
                            lifdSource.setCompId(Integer.MAX_VALUE);
                        }
 
                        saveSmartObjectData(
                                fileName + "_" + lifdSource.getOriginalFileName(),
                                lifdSource.getData());
                        lifdSource.setData(loadNewData("new_" + lifdSource.getOriginalFileName()));
                        assertAreEqual(expected[10], lifdSource.getLength());
 
                        lifdSource.setChildDocId(UUID.randomUUID().toString());
                        lifdSource.setAssetModTime(Double.MAX_VALUE);
                        lifdSource.setFileType("test");
                        lifdSource.setFileCreator("me");
                    }
 
                    assertAreEqual(newLength, lnk2Resource.getLength());
                    break;
                }
            }
 
            // Đảm bảo rằng đã tìm thấy Lnk2Resource
            assertAreEqual(true, lnk2Resource != null);
 
            // Sao chép hình ảnh PSD đã tải
            if (image.getBitsPerChannel() < 32) // 32 bit mỗi kênh không được hỗ trợ
            {
                image.save(dstPsdPath, new PsdOptions(image));
            }
        }
        finally
        {
            image.dispose();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();
 
 
Object[] Lnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "00af34a0-a90b-674d-a821-73ee508c5479",
                                "rgb8_2x2.png",
                                "png",
                                "",
                                0x53,
                                0d,
                                "",
                                7,
                                true,
                                0x124L,
                                0x74cL
                        }
        };
 
Object[] LayeredLnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "69ac1c0d-1b74-fd49-9c7e-34a7aa6299ef",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
                new Object[]
                        {
                                "5a7d1965-0eae-b24e-a82f-98c7646424c2",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694L,
                                0x10dd4L
                        },
        };
 
Object[] LayeredLnk3ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "2fd7ba52-0221-de4c-bdc4-1210580c6caa",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694l,
                                0x10dd4L
                        },
                new Object[]
                        {
                                "372d52eb-5825-8743-81a7-b6f32d51323d",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
        };
 
// Ví dụ này mô tả cách lấy và đặt các thuộc tính của Lnk2 Resource và nguồn dữ liệu LiFD của nó cho 8 bit mỗi kênh.
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
// Ví dụ này mô tả cách lấy và đặt các thuộc tính của Lnk3 Resource và nguồn dữ liệu LiFD của nó cho 32 bit mỗi kênh.
$.exampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
// Ví dụ này mô tả cách lấy và đặt các thuộc tính của Lnk2 Resource và nguồn dữ liệu LiFD của nó cho 16 bit mỗi kênh.
$.exampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}

**PSDJAVA-247. Thay đổi thông báo ngoại lệ khi cố gắng mở các định dạng không được hỗ trợ như ảnh**
{{< highlight java >}}
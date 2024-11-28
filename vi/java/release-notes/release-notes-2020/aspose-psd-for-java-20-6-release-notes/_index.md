---
title: Aspose.PSD cho Java 20.6 - Ghi chú phát hành
type: docs
weight: 50
url: /vi/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Trang này chứa ghi chú phát hành cho [Aspose.PSD cho Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDJAVA-216|Hỗ trợ LnkEResource (Tài nguyên của Lớp Đối tượng Thông Minh)|Tính năng|
|PSDJAVA-219|Hỗ trợ britResource (Tài nguyên của Lớp Điều chỉnh Độ Sáng/Độ Tương Phản)|Tính năng|
|PSDJAVA-222|Di chuyển thiết lập DefaultReplacementFont vào lớp ImageOptionsBase|Cải tiến|
|PSDJAVA-217|Resize file PSD không hoạt động chính xác nếu có mặt nạ trong lớp điều chỉnh có giới hạn trống|Lỗi|
|PSDJAVA-218|Ảnh Psd với chế độ RGB 16 bit/ kênh chỉ cập nhật lớp trên xem trước|Lỗi|
|PSDJAVA-220|Thay đổi Mặt nạ lớp PSD bị loại bỏ khi lưu|Lỗi|
|PSDJAVA-221|Thứ tự Lớp Không Chính Xác sau khi thêm Nhóm Lớp vào Nhóm Lớp trống|Lỗi|
|PSDJAVA-223|Ngoại lệ khi tải tệp PSD cụ thể với tài nguyên LnkE hợp chất và thuộc tính adobeStockLicenseState|Lỗi|
|PSDJAVA-224|Việc lưu Tệp AI dưới định dạng Jpeg2000 không hoạt động|Lỗi|
|PSDJAVA-225|Nhóm Lớp với Chế Độ Kết hợp Không Được Hiển Thị|Lỗi|
|PSDJAVA-226|Ngoại lệ NullReference khi cố gắng chuyển đổi tệp Psd cụ thể thành hình ảnh|Lỗi|
|PSDJAVA-227|OverflowException khi cố gắng mở tệp Psd cụ thể|Lỗi|
### **Thay đổi API Công khai**
### **API Đã Thêm:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **API Đã Xóa:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Ví Dụ Sử Dụng:**

**PSDJAVA-216: Hỗ trợ LnkEResource (Tài nguyên của Lớp Đối tượng Thông Minh)**

{{< highlight java >}}

 // Một ví dụ về việc liên kết các loại tài sản khác nhau (hình ảnh raster, thư viện CC) với PSD.

// Cũng xem xét API của LnkeResource.

// Một lớp giữ các phương thức trong phạm vi cục bộ

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("Ví dụ về Hỗ trợ LnkEResource không hoạt động chính xác.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Ví dụ này thể hiện cách lấy và đặt các thuộc tính của tài nguyên Photoshop Psd LnkE

    // Resource chứa thông tin về một tệp ngoại e liên kết.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Tải một PSD được xác định trước

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Tìm LnkeResource trong các tài nguyên Lớp toàn cầu

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Xác định lại các thuộc tính của LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Cập nhật các thuộc tính của LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Đảm bảo LnkeResource được hỗ trợ

            assertIsTrue(lnkeResource != null);

            // Lưu một bản sao của PSD đã tải

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Tải bản sao đã lưu

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Chuyển đổi PSD sang định dạng tệp PNG (với kênh alpha cho tính trong suốt)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Ví dụ này thể hiện cách lấy và đặt các thuộc tính của tài nguyên Psd LnkE

// Chứa thông tin về tệp JPEG liên kết bên ngoài.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Ví dụ này thể hiện cách lấy và đặt các thuộc tính của Photoshop Psd LnkE

// Chứa thông tin về tệp PNG bên ngoài liên kết.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Ví dụ này thể hiện cách lấy và đặt các thuộc tính của Photoshop Psd LnkE

// Chứa thông tin về tài sản thư viện CC liên kết bên ngoài.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Tính năng có sẵn trong Photoshop CC 2015)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: Hỗ trợ britResource (Tài nguyên của Lớp Điều chỉnh Độ Sáng/Độ Tương Phản)**

{{< highlight java >}}

 // Ví dụ này thể hiện cách bạn có thể thay đổi chương trình PSD Image

// Brightness/Contrast Layer Resource - BritResource. Đây là một API Aspose.PSD cấp thấp.

// Bạn có thể sử dụng Lớp Điều chỉnh Độ Sáng/Độ Tương Phản thông qua API của nó, điều này sẽ dễ dàng hơn,

// nhưng việc chỉnh sửa trực tiếp tài nguyên hình ảnh PhotoShop sẽ mang lại cho bạn nhiều quyền kiểm soát hơn về nội dung tệp PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Tải tài liệu PhotoShop chứa lớp Điều chỉnh Độ Sáng / Độ Tương Phản

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Tìm BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Xác định các thuộc tính tài nguyên

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource được đọc sai");

                    }

                    // Cập nhật các thuộc tính tài nguyên

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Lưu một bản sao của PSD đã cập nhật

                    psdImage.save(dstPath, new PsdOptions());

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

**PSDJAVA-217: Resize file PSD không hoạt động chính xác nếu có mặt nạ trong lớp điều chỉnh có giới hạn trống**

{{< highlight java >}}

 // Một ví dụ về thay đổi kích thước hình ảnh chứa mặt nạ lớp điều chỉnh với giới hạn trống.

// Chương trình tải một PSD được xác định trước chỉ để kiểm tra xem có ngoại lệ không.

final int scale = 2; // Hệ số tùy ý

String[] names = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmky",

};

for (String name : names)

{

    String srcFilePath = name + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + name + ".png";

    // Tải một PSD chứa mặt nạ lớp điều chỉnh có giới hạn trống

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // Thay đổi kích thước hình ảnh

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // Lưu một bản sao của PSD đã tải

        image.save(dstFilePath, new PsdOptions());

        // Xuất PSD sang định dạng tệp PNG (với kênh alpha cho tính trong suốt)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, pngOptions);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: Ảnh Psd với chế độ RGB 16 bit/ kênh chỉ cập nhật lớp trên xem trước**


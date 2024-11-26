---
title: บันทึกการอัปเดต Aspose.PSD for Java 20.6
type: สารบัญ
weight: 50
url: /th/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

| **คีย์** | **สรุป** | **หมวดหมู่** |
| :- | :- | :- |
|PSDJAVA-216|สนับสนุนของ LnkEResource (Resource of Smart Object Layer)|คุณลักษณะ|
|PSDJAVA-219|สนับสนุน britResource (Resource of Brightness/Contrast Adjustment Layer)|คุณลักษณะ|
|PSDJAVA-222|ย้ายการตั้งค่า DefaultReplacementFont เข้าสู่ ImageOptionsBase class|การปรับปรุง|
|PSDJAVA-217|การเปลี่ยนขนาดไฟล์ PSD ไม่ถูกต้องหากมีมาสค์ในชั้นการปรับที่มีขอบว่างเปล่า|ข้อผิดพลาด|
|PSDJAVA-218|Psd Image โหมด RGB 16 bit/channel มีการอัปเดตชั้นเท่านั้นบนพรีวิว|ข้อผิดพลาด|
|PSDJAVA-220|การเปลี่ยนเปลี่ยนของ PSD Layer Mask ถูกลบขณะบันทึก|ข้อผิดพลาด|
|PSDJAVA-221|ลำดับของเลเยอร์ไม่ถูกต้องหลังจากเพิ่มชั้นเลเยอร์ลูกเข้าไปในชั้นเลเยอร์เปล่า|ข้อผิดพลาด|
|PSDJAVA-223|มีข้อยกเว้นเมื่อโหลดไฟล์ PSD พิเศษที่มีคอมไพล์ LnkE Resource และคุณสมบัติ adobeStockLicenseState|ข้อผิดพลาด|
|PSDJAVA-224|การบันทึกไฟล์ AI เป็นรูปแบบ Jpeg2000 ไม่ทำงาน|ข้อผิดพลาด|
|PSDJAVA-225|Layer Group ที่ไม่ได้ใช้โหมดผสมผสาน ไม่ถูกเรนเดอร์|ข้อผิดพลาด|
|PSDJAVA-226|การเกิด NullReference Exception เมื่อพยายามแปลงไฟล์ Psd บางไฟล์เป็นภาพ|ข้อผิดพลาด|
|PSDJAVA-227|การเกิด OverflowException เมื่อพยายามเปิดไฟล์ Psd บางไฟล์|ข้อผิดพลาด|

# **การเปลี่ยนแปลงใน API สาธารณะ**
# **API ที่เพิ่มเข้ามา:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate (java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize (long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath (java.lang.String)
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState (boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime (double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId (int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor (boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink (boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId (int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName (java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId (java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save (com.aspose.psd.StreamContainer, int)
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

## **API ที่ถูกลบออก:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **ตัวอย่างการใช้:**

**PSDJAVA-216: สนับสนุนของ LnkEResource (Resource of Smart Object Layer)**

{{< highlight java >}}

 // ตัวอย่างของการเชื่อมโยงส่วนประเภทต่าง ๆ (รูปแบบเราส์เตอร์, ไลบรารี CC) ไปยัง PSD

// นอกจากนี้ API ของ LnkeResource ถือว่าจำเป็น

// ระดับคลาสที่เก็บเมธอดในโองการถ์

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport ทำงานผิด.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // ตัวอย่างนี้แสดงให้เห็นว่าต้องว่าจะได้หรือตั้งค่าของ LnkE

    // คุณสมบัติที่มีข้อมูลเกี่ยวกับไฟล์ลิ้งทางภายนอก

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

            longfileSize)

    {

        String outputPath = "out_" + fileName;

        // โหลด PSD ที่กำหนดล่วงหน้า

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // ค้นหา LnkeResource ในระดับโกลบอล

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // ตรวจสอบคุณสมบัติของ LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), fileSize);

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

                    // อัปเดตคุณสมบัติของ LnkeResource

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

            // ตรวจสอบว่า LnkeResource ถูกสนับสนุนหรือไม่

            assertIsTrue(lnkeResource != null);

            // บันทึกสำเนาของ PSD ที่โหลด

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // โหลดสำเนาที่บันทึก

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // แปลง PSD เป็นรูปแบบไฟล์ PNG (พร้อมกับช่องแอลฟาสำหรับความโป่งแสง)

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

// ตัวอย่างนี้แสดงให้เห็นว่าต้องได้หรือตั้งค่าของ Psd LnkE ทราบ

// ข้อมูลเกี่ยวกับไฟล์ลิ้งทางภายนอก JPEG

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

// ตัวอย่างนี้แสดงให้เห็นว่าต้องได้หรือตั้งค่าของ Psd LnkE ทราบ

// ข้อมูลเกี่ยวกับไฟล์ลิ้งทางภายนอก PNG

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

// ตัวอย่างนี้แสดงให้เห็นว่าต้องได้หรือตั้งค่าของ Psd LnkE ทราบ

// ข้อมูลเกี่ยวกับไฟล์ลิ้งทางภายนอก CC ไลบรารี

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Feature is available in Photoshop CC 2015)",

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

**PSDJAVA-219: สนับสนุนของ britResource (Resource of Brightness/Contrast Adjustment Layer)**

{{< highlight java >}}

 // ตัวอย่างของการเปลี่ยนรูปภาพ PSD Brightness/Contrast Layer Resource - BritResource นี้เป็น API ระดับล่างของ Aspose.PSD

// คุณสามารถใช้ Brightness/Contrast Layer ผ่าน API

// ที่ง่ายกว่า แต่การแก้ไขโดยตรงของรีซอร์ส Photoshop จะให้คุณสมบัติ

// มากกว่าสำหรับเนื้อหาของไฟล์ PSD

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// โหลดเอกสาร Photoshop ที่มีชั้นการปรับ Brightness/Contrast

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // ค้นหา BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // ตรวจสอบคุณสมบัติของ resource

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource ถูกอ่านผิด");

                    }

                    // อัปเดตคุณสมบัติของ resource

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // บันทึกสำเนาของ PSD ที่อัปเดต

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

**PSDJAVA-217: การเปลี่ยนขนาดไฟล์ PSD ไม่ถูกต้องหากมีมาสค์ในชั้นการปรับที่มีขอบว่างเปล่า**

{{< highlight java >}}

 // ตัวอย่างของการเปลี่ยนขนาดรูปภาพที่มีมาสค์ในชั้นการปรับที่มีขอบว่างเปล่า

// โปรแกรมโหลด PSD ที่กำหนดล่วงหน้าเพื่อตรวจสอบว่าไม่มีข้อยกเว้น

final int scale = 2; // ค่าคงที่

String[] names = {

    "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

    "LevelsLayerWithLayerMaskRgb",

    "LevelsLayerWithLayerMaskCmyk",

};

for (String name : names)

{

    String srcFilePath = name + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + name + ".png";

    // โหลด PSD ที่กำหนดที่มีมาสค์ในชั้นการปรับที่มีขอบว่างเปล่า

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // เปลี่ยนขนาดรูปภาพ

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // บันทึกสำเนาของ PSD ที่โหลด

        image.save(dstFilePath, new PsdOptions());

        // ส่งออก PSD เป็นไฟล์ PNG (พร้อมกับช่องแอลฟาสำหรับความโป่งแสง)

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

**PSDJAVA-218: Psd Image โหมด RGB 16 bit/channel มีการอัปเดตชั้นเท่านั้นบนพรีวิว**

{{< highlight java >}}

 // ตัวอย่างของการอัปเดตเลเยอร์สำหรับภาพชั้น 16 บิต RGB

// โปรแกรมวาดบางสิ่งบนทุกชั้นเพื่อให้แน่ใจว่าชั้นทั้งหมดได้รับการอัปเดตอย่างถูกต้อง

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

// โหลด PSD ที่กำหนดในโหมด RGB 16 bit

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // วาดชื่อเลเยอร์และเส้นขอบภายใน
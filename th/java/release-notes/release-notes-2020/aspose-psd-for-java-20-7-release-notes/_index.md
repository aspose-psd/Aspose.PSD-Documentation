---
title: บันทึกการเปลี่ยยะ Aspose.PSD สำหรับ Java 20.7
type: docs
weight: 50
url: /th/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการเปลี่ยวสำหรับ [Aspose.PSD สำหรับ Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**คีย์**|**สรุป**|**หมวดหมู่**|
| :- | :- | :- |
|PSDJAVA-231|สนับสนุนการเพิ่ม Stroke Effect ในระหว่างการเรียกใช้งาน|คุณลักษณะ|
|PSDJAVA-249|สนับสนุนการ lnk2 / lnk3 Resources (Resources ของ Smart Object Layer)|คุณลักษณะ|
|PSDJAVA-247|เปลี่ยนข้อความข้อพล้อตเมื่อพยายามเปิดรูปแบบที่ไม่รองรับเป็นรูปภาพ|ปรับปรุง|
|PSDJAVA-235|หากเราบันทึกไฟล์ PSD หลังจากสร้าง Layer Group ใหม่เราจะได้การเตือนจาก Photoshop เมื่อเปิดไฟล์|ข้อบกพร่อง|
|PSDJAVA-236|ล้มเหลวในการบันทึก LayerMask|ข้อบกพร่อง|
|PSDJAVA-237|การ Clipping mask ไม่ได้ปรับใช้กับโฟลเดอร์|ข้อบกพร่อง|
|PSDJAVA-238|ไม่สามารถเปิดไฟล์ด้วย Aspose.PSD for Java|ข้อบกพร่อง|
|PSDJAVA-239|ข้อยกเว้นการบันทึกภาพเมื่อแปลง PSD เป็น PDF|ข้อบกพร่อง|
|PSDJAVA-240|การดำเนินการตัดอาจทำให้เส้น Clipping เป็นค่าไม่ถูกต้องในภาพ PSD|ข้อบกพร่อง|
|PSDJAVA-241|การ NullReference Exception เมื่อพยายามบันทึกไฟล์ PSD ที่ระบุพร้อมกับเอฟเฟกต์เงา|ข้อบกพร่อง|
|PSDJAVA-243|Aspose.PSD ส่งคืน true ใน Image.CanLoad(pdfStream)|ข้อบกพร่อง|
|PSDJAVA-244|เลเยอร์ล้มเหลวในการแสดงใน PNG ที่สร้างขึ้น|ข้อบกพร่อง|
|PSDJAVA-245|ข้อยกเว้นในการเข้าถึง TextData|ข้อบกพร่อง|
|PSDJAVA-246|ImageSaveException เมื่อบันทึกไฟล์ PSD|ข้อบกพร่อง|

# **การเปลี่ยนแปลง API สาธารณะ**
# **API ที่เพิ่ม:**
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
## **API ที่ลบ:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.predicate.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])

# **ตัวอย่างการใช้งาน:**

**PSDJAVA-231. สนับสนุนการเพิ่ม Stroke Effect ในระหว่างการใช้งาน**
{{< highlight java >}}
// ตัวอย่างนี้แสดงถึงการเพิ่ม stroke effect (เส้นขอบ) ไปยังเลเยอร์ที่มีอยู่ในไฟล์ PSD ใน Java
// มี 3 ประเภทของ stroke: สี, ไฟ gradient, และ ลายหรือ pattern. แต่ละประเภทมี
// 3 รูปแบบ (positions) ที่ stroke จะถูก render: ภายใน, กึ่งกลาง, และ ภายนอก
// ตัวอย่างนี้แสดงถึงการใช้งานของทั้งหมดทั้ง 3 กรณีนั้น

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

    // 1. เพิ่ม Color fill, ที่ตำแหน่งภายใน
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 2. เพิ่ม Color fill, ที่ตำแหน่งภายนอก
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 3. เพิ่ม Color fill, ที่ตำแหน่งกลาง
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // 4. เพิ่ม Gradient fill, ที่ตำแหน่งภายใน
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);

    // 5. เพิ่ม Gradient fill, ที่ตำแหน่งภายนอก
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);

    // 6. เพิ่ม Gradient fill, ที่ตำแหน่งกลาง
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);

    // 7. เพิ่ม Pattern fill, ที่ตำแหน่งภายใน
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);

    // 8. เพิ่ม Pattern fill, ที่ตำแหน่งภายนอก
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);

    // 9. เพิ่ม Pattern fill, ที่ตำแหน่งกลาง
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

**PSDJAVA-249. สนับสนุน lnk2 / lnk3 Resources (Resources ของ Smart Object Layer)**
{{< highlight java >}}
// ตัวอย่างนี้แสดงวิธีการทำงานกับ smart object resources (โดยส่วนใหญ่คือ Lnk2Resource)
// โปรแกรมโหลด Photoshop documents หลายรายการและส่งออก smart objects ของพวกเขาไปยัง
// รูปแบบไฟล์ raster. โดยโค้ดยังทราบการใช้งานของเมทอด public ของ Lnk2Resource

class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("ค่าที่เป็นจริง %s ไม่เท่ากับค่าที่คาดหวัง %s", actual, expected));
        }
    }

    // บันทึกข้อมูลของ smart object เข้าไปในไฟล์ PSD
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

    // โหลดข้อมูลใหม่สำหรับ smart object จากไฟล์
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

    // ดึงและตั้งค่าของ PSD Lnk2 / Lnk3 Resource และ LiFD data sources ใน PSD image
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
            // ค้นหา Lnk2Resource
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;

                    // ตรวจสอบคุณสมบัติของ Lnk2Resource
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);

                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // ตรวจสอบและเปลี่ยนค่าของ LiFdDataSource
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

            // ตรวจสอบว่า Lnk2Resource ถูกพบ
            assertAreEqual(true, lnk2Resource != null);

            // สร้างสำเนาของ PSD ที่โหลด
            if (image.getBitsPerChannel() < 32) // การบันทึก 32 bit ต่อช่องยังไม่ได้รับการสนับสนุน
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

// ตัวอย่างนี้แสดงถึงวิธีการดึงและตั้งค่าของ PSD Lnk2 Resource และข้อมูล LiFD sources สำหรับ 8 bit ต่อช่อง
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);

// ตัวอย่างนี้แสดงถึงวิธีการดึงและตั้งค่าของ PSD Lnk3 Resource และข้อมูล LiFD sources สำหรับ 32 bit ต่อช่อง
$.exampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);

// ตัวอย่างนี้แสดงถึงวิธีการดึงและตั้งค่าของ PSD Lnk2 Resource และข้อมูล LiFD sources สำหรับ 16 bit ต่อช่อง
$.exampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}
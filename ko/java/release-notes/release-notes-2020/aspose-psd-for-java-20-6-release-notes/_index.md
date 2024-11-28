---
title: Aspose.PSD for Java 20.6 - 릴리스 노트
type: docs
weight: 50
url: /ko/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) 에 대한 릴리스 노트가 포함되어 있습니다. {{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDJAVA-216|LnkEResource (Smart Object Layer의 리소스) 지원|기능|
|PSDJAVA-219|britResource (명암 조정 레이어의 리소스) 지원|기능|
|PSDJAVA-222|DefaultReplacementFont 설정을 ImageOptionsBase 클래스로 이동|개선|
|PSDJAVA-217|조정 레이어에 있는 마스크가 빈 영역을 가진 경우 PSD 파일 크기 조정이 정상 작동하지 않음|버그|
|PSDJAVA-218|RGB 모드 16비트/채널의 PSD 이미지가 레이어를 미리 보기 상태에서만 업데이트|버그|
|PSDJAVA-220|PSD 레이어 마스크 변경이 저장될 때 무시됨|버그|
|PSDJAVA-221|비어있는 레이어 그룹에 레이어 그룹 추가 후 부정확한 레이어 순서|버그|
|PSDJAVA-223|복합 LnkE 리소스 및 adobeStockLicenseState 속성이 있는 특정 PSD 파일 로드 시 예외 발생|버그|
|PSDJAVA-224|AI 파일을 Jpeg2000 형식으로 저장하는 것이 작동하지 않음|버그|
|PSDJAVA-225|PassThrough Blending Mode가 아닌 레이어 그룹이 렌더링되지 않음|버그|
|PSDJAVA-226|특정 PSD 파일을 이미지로 변환하려고 할 때 NullReference 예외|버그|
|PSDJAVA-227|특정 PSD 파일을 열려고 할 때 OverflowException 예외 발생|버그|

# **공개 API 변경**
# **추가된 API:**
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
## **삭제된 API:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **사용 예시:**

**PSDJAVA-216: LnkEResource (스마트 객체 레이어의 리소스) 지원**

{{< highlight java >}}

 // PSD에 다른 유형의 자산(래스터 이미지, CC 라이브러리)을 링크하는 예제.

// 또한 LnkeResource의 API를 살펴본다.

// 로컬 범위에서 메서드를 보유하는 클래스

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("LnkEResourceSupportExample 작동을 잘못했습니다.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // 이 예제는 Photoshop Psd LnkE에 대한 속성을 가져오고 설정하는 방법을 보여준다.

    // 외부 링크된 파일에 대한 정보가 포함된 LnkeResource에 대한 정보

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

        // 미리 정의된 PSD 로드

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // 전역 리소스 중에서 LnkeResource 찾기

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // LnkeResource 속성 확인

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

                    // LnkeResource 속성 업데이트

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

            // LnkeResource가 지원되는지 확인

            assertIsTrue(lnkeResource != null);

            // 로드된 PSD의 사본 저장

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // 저장된 사본 로드

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // PSD를 PNG 파일 형식으로 변환 (투명도를 위한 알파 채널 포함)

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

// 외부로 연결된 JPEG 파일에 대한 정보를 포함하는 Photoshop Psd LnkE Resource의 속성을 가져오고 설정하는 방법을 보여준다.

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

// 외부로 연결된 PNG 파일에 대한 정보를 포함하는 Photoshop Psd LnkE Resource의 속성을 가져오고 설정하는 방법을 보여준다.

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

// 외부로 연결된 CC Libraries 자산에 대한 정보를 포함하는 Photoshop Psd LnkE Resource의 속성을 가져오고 설정하는 방법을 보여준다.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries 자산 “rgb8_2x2_linked/rgb8_2x2” (Photoshop CC 2015에서 사용 가능한 기능)",

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

**PSDJAVA-219: britResource (명암 조정 레이어의 리소스) 지원**

{{< highlight java >}}

 // 프로그래밍 방식으로 PSD 이미지의 명암/조도 조정 레이어 리소스인 britResource를 변경하는 방법을 보여준다. 이것은 낮은 수준의 Aspose.PSD API이다. 명암/조도 레이어를 사용하여 PSD에서 API를 사용할 수 있으며, 직접적인 PhotoShop 리소스 편집은 PSD 파일 내용에 대한 제어를 더 많이 제공한다.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// 명암/조도 조정 레이어를 포함하는 Photoshop 문서를 로드

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // BritResource를 검색합니다.

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // 리소스 속성 확인

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource를 잘못 읽었습니다.");

                    }

                    // 리소스 속성 업데이트

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // 업데이트된 PSD의 사본 저장

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


**PSDJAVA-217: 조정된 PSD 파일 크기가 조정 레이어에 빈 바운드를 가진 마스크가 있는 경우 잘못 작동함**

{{< highlight java >}}

 // 빈 바운드를 가진 조정 레이어 마스크가 포함된 이미지를 조정하는 예제입니다.

// 프로그램은 예외가 없는지 확인하기 위해 미리 정의된 PSD를 로드합니다.

final int scale = 2; // 임의의 계수

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

    // 빈 바운드를 가진 조정 레이어 마스크를 포함하는 미리 정의된 PSD를 로드합니다.

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // 이미지 크기 조정

        image.resize(image.getWidth() * scale, image.getHeight() * scale);

        // 로드된 PSD의 사본 저장

        image.save(dstFilePath, new PsdOptions());

        // PSD를 PNG 파일 형식으로 내보내기 (투명도를 위한 알파 채널 포함)

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



**PSDJAVA-218: RGB 모드 16비트/채널의 PSD 이미지가 레이어를 미리 보기 상태에서만 업데이트**

{{< highlight java >}}

 // 16비트 RGB 이미지의 일반 레이어를 업데이트하는 예제입니다. 프로그램은 전체 레이어가 올바르게 업데이트되는지 확인하기 위해 각 레이어에 무언가를 그립니다.

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

// 16비트 RGB 모드의 미리 정의된 PSD를 로드합니다

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // 일반 레이어에 레이어 이름과 내부 테두리를 그립니다

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // 로드된 PSD의 사본 저장

    image.save(outputFilePath, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}



**PSDJAVA-220: PSD 레이어 마스크 변경이 저장될 때 무시됨**

{{< highlight java >}}

 // PSD 이미지에서 라스터 마스크를 가져와 파일로 저장하는 클래스

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("예제 작동에 문제가 있습니다.");

        }

    }

    // Big-endian 바이트 순서로 변환된 int 값 가져오기

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Big-endian에서 Int32 값으로 변환하기

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("바이트");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("인덱스", "인덱스가 바이트 배열을 벗어납니다.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // PSD 이미지의 레이어에서 라스터 마스크 가져와 파일에 저장

    void saveRasterMask(String maskFilePath, Layer layer)

    {

        LayerMaskDataShort maskData = (LayerMaskDataShort)layer.getLayerMaskData();

        FileStreamContainer container = FileStreamContainer.createFileStream(maskFilePath, false);

        try

        {

            container.write(getBigEndianBytesInt32(maskData.getTop()));

            container.write(getBigEndianBytesInt32(maskData.getLeft()));

            container.write(getBigEndianBytesInt32(maskData.getBottom()));

            container.write(getBigEndianBytesInt32(maskData.getRight()));

            container.writeByte(maskData.getDefaultColor());

            container.writeByte((byte)maskData.getFlags());

            container.write(getBigEndianBytesInt32(maskData.getImageData().length));

            container.write(maskData.getImageData(), 0, maskData.getImageData().length);

        }

        finally

        {

            container.dispose();

        }

    }

    // 파일에서 레이어에 라스터 마스크 추가하고 PSD 포맷 이미지에 저장

    void addRasterMask(Layer layer, String maskSourcePath)

    {

        LayerMaskDataShort maskData = new LayerMaskDataShort();

        FileStreamContainer container = FileStreamContainer.openFileStream(maskSourcePath);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(container.read(bytes), 22);

            maskData.setTop(fromBigEndianToInt32(bytes, 0));

            maskData.setLeft(fromBigEndianToInt32(bytes, 4));

            maskData.setBottom(fromBigEndianToInt32(bytes, 8));

            maskData.setRight(fromBigEndianToInt32(bytes, 12));

            maskData.setDefaultColor(bytes[16]);

            maskData.setFlags(bytes[17]);

            int imageDataLength = fromBigEndianToInt32(bytes, 18);

            byte[] data = new byte[imageDataLength];

            assertAreEqual(maskData.getMaskRectangle().getWidth() *

                    maskData.getMaskRectangle().getHeight(), imageDataLength);

            assertAreEqual(container.read(data), imageDataLength);

            maskData.setImageData(data);

        }

        finally

        {

            container.dispose();

        }

        // 레이어에만 LayerMaskData를 추가하는 것으로는 올바른 저장이 되지 않아 채널이 업데이트되지 않습니다.

        // layer.setLayerMaskData(mask); // 이렇게 하면 마스크 채널이 추가되지 않습니다.

        // 마스크 추가(또는 업데이트)

        layer.addLayerMask(maskData); // 이렇게 하면 마스크와 채널이 모두 추가 및 업데이트됩니다!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Adobe® Photoshop® PSD 파일에서 라스터 레이어 마스크를 가져와 파일에 저장하는 방법을 보여주는 예제입니다.

PngOptions pngOptions = new PngOptions();

pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

String sourceFilePath = "FourWithMasks.psd";

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    Layer layer = image.getLayers()[2];

    // 레이어에서 라스터 마스크 가져와 파일에 저장

    $.saveRasterMask("FourWithMasks2.msk", layer);

    // 레이어 마스크 변경(반전) 및 이미지 저장

    LayerMaskData mask = layer.getLayerMaskData();

    byte[] maskData = mask.getImageData();

    for (int i = 0; i < maskData.length; i++)

    {

        maskData[i] = (byte)~maskData[i];

    }

    // LayerMaskData를 변경하는 것만으로 렌더링에 영향을 주지만 정확한 저장을 위해 채널이 업데이트되지 않습니다.

    image.save("FourWithMasksUpdated2.png", pngOptions);

    // 그러나 LayerMaskData를 변경하는 것만으로는 정확한 저장을 위해 채널이 업데이트되지 않습니다.

    layer.setLayerMaskData(mask); // 이것도 작동하지 않습니다

    layer.addLayerMask(mask); // 그러나 이것은 마스크와 채널 모두 추가/업데이트합니다!

    image.save("FourWithMasksUpdated2.psd");

    // 레이어에서 라스터 마스크 제거 및 이미지 저장

    layer.setLayerMaskData(null); // LayerMaskData를 제거하는 것만으로 렌더링에 영향을 주지만 PSD 형식으로 저장하는 데는 영향을 주지 않음

    image.save("FourWithMasksRemoved2.png", pngOptions);

    layer.addLayerMask(null); // 이렇게 하면 마스크와 마스크 채널이 모두 제거됩니다!

    image.save("FourWithMasksRemoved2.psd");

    // 파일에서 레이어에 라스터 마스크 추가 및 이미지 저장

    $.addRasterMask(layer, "raster.msk");

    image.save("FourWithMasksAdded2.png", pngOptions);

    image.save("FourWithMasksAdded2.psd");

}

finally

{

    image.dispose();

}

{{< /highlight >}}
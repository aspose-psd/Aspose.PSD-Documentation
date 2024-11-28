---
title: Aspose.PSD for Java 20.7 - 릴리스 노트
type: docs
weight: 50
url: /ko/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDJAVA-231|런타임에서 스트로크 효과 추가 지원|기능|
|PSDJAVA-249|lnk2 / lnk3 리소스 지원 (스마트 오브젝트 레이어의 리소스)|기능|
|PSDJAVA-247|지원하지 않는 형식을 이미지로 열려고 할 때 예외 메시지 변경|개선|
|PSDJAVA-235|새 레이어 그룹 생성 후 PSD 파일 저장 시 Photoshop 경고 발생|버그|
|PSDJAVA-236|레이어 마스크 저장 실패|버그|
|PSDJAVA-237|클리핑 마스크가 폴더에 적용되지 않음|버그|
|PSDJAVA-238|Aspose.PSD for Java로 파일 열기 불가|버그|
|PSDJAVA-239|PSD를 PDF로 변환 시 이미지 저장 실패 예외 발생|버그|
|PSDJAVA-240|크롭 작업으로 PSD 이미지의 클리핑 경로 무효화|버그|
|PSDJAVA-241|그림자 효과가 있는 특정 PSD 파일 저장 시 NullReference 예외 발생|버그|
|PSDJAVA-243|Aspose.PSD가 Image.CanLoad(pdfStream)에 대해 true를 반환|버그|
|PSDJAVA-244|PNG에서 레이어 렌더링 실패|버그|
|PSDJAVA-245|TextData 접근 시 예외 발생|버그|
|PSDJAVA-246|PSD 저장 시 ImageSaveException 발생|버그|

# **공개 API 변경**
# **추가된 API:**
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
## **제거된 API:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **사용 예시:**

**PSDJAVA-231. 런타임에서 스트로크 효과 추가 지원**
{{< highlight java >}}
// 이 예제는 Java에서 PSD 파일의 기존 레이어에 선 효과(테두리)를 추가하는 방법을 보여줍니다.
// 선에는 색상, 그라데이션 및 패턴 등 세 가지 유형이 있습니다. 각 유형마다 내부, 중앙 및 외부에 효과가 렌더링되는 세 가지 방법이 있습니다.
// 이 예제는 모든 경우의 사용법을 보여줍니다.
 
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
 
    // 1. 색상 채우기 추가, 내부 위치
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 2. 색상 채우기 추가, 외부 위치
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 3. 색상 채우기 추가, 중앙 위치
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 나머지 코드는 생략
    // 4. 그라디언트 채우기 추가, 내부 위치
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);
 
    // 나머지 코드는 생략
{{< /highlight >}}
 
**PSDJAVA-249. lnk2 / lnk3 리소스 지원 (스마트 오브젝트 레이어의 리소스)**
{{< highlight java >}}
// 이 예제는 스마트 오브젝트 리소스(기본적으로 Lnk2Resource)와 작업 방법을 보여줍니다.
// 프로그램은 여러 Photoshop 문서를로드하여 스마트 오브젝트를 래스터 파일 형식으로 내보내고
// Lnk2Resource의 public 메서드 사용을 디모합니다.
 
class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("예상 %s가 실제 %s와 동일하지 않습니다.", actual, expected));
        }
    }
 
    // 스마트 오브젝트의 데이터를 PSD 파일에 저장
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
 
    // 파일에서 스마트 오브젝트의 새 데이터 로드
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
 
    // PSD 이미지의 Lnk2 / Lnk3 Resource 및 PSD 이미지의 liFD 데이터 소스의 속성 가져오기 및 설정
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
            // Lnk2Resource 검색
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;
 
                    // Lnk2Resource의 속성 검증
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);
 
                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // LiFdDataSource의 속성 검증 및 변경
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
 
            // Lnk2Resource 확인
            assertAreEqual(true, lnk2Resource != null);
 
            // 로드된 PSD의 사본을 만들기
            if (image.getBitsPerChannel() < 32) // 32 비트 채널 저장이 아직 지원되지 않습니다
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
 
{{< /highlight >}}

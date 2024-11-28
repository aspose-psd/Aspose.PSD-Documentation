---
title: Aspose.PSD for Java 20.4 - 릴리스 노트
type: docs
weight: 30
url: /ko/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDJAVA-156|'벡터 원점 데이터' 리소스 지원|기능|
|PSDJAVA-171|lclrResource (시트 색상 설정) 지원|기능|
|PSDJAVA-157|LengthRecord 데이터의 속성 지원. (경로 작업 (부울 연산), 레이어 내 모양의 인덱스, 베지에 노트 레코드 수)|기능|
|PSDJAVA-158|이미지 섹션 리소스 #1010 배경색 지원|기능|
|PSDJAVA-161|런타임에 채우기 레이어 추가|기능|
|PSDJAVA-168|이미지 섹션 리소스 #1009 테두리 정보 지원|기능|
|PSDJAVA-169|AI 형식 파일에서 레이어 지원|기능|
|PSDJAVA-163|그라데이션 오버레이 레이어 효과 읽기 및 편집 지원|기능|
|PSDJAVA-164|그라데이션 오버레이 레이어 효과 렌더링|기능|
|PSDJAVA-149|텍스트 레이어의 textData.items 속성을 가져올 때 Aspose.PSD for Java 오류|버그|
|PSDJAVA-166|그레이스케일 ColorMode 및 채널 당 16 비트로 PSD 이미지 저장시 그레이스케일 PSD 형식으로 수정|버그|
|PSDJAVA-167|그레이스케일 ColorMode 및 채널 당 16 비트로 PNG 형식으로 PSD 이미지 저장시 수정|버그|
|PSDJAVA-159|GradientOverlayEffect.BlendMode 속성 변경이 Photoshop에 표시되지 않음|버그|
# **공개 API 변경사항**
# **추가된 API:**
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
## **제거된 API:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **사용 예시:**

**PSDJAVA-156. '벡터 원점 데이터' 리소스 지원**

{{< highlight java >}}

 /*

벡터 원점 데이터 리소스를 읽고 수정하는 예제.

*/

// 간단함을 위해 메서드를 로컬 스코프에 유지

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

            throw new Exception("VogkResource를 찾을 수 없습니다.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// 미리 정의된 VOGK 리소스가 포함된 PSD 파일 로드

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 사전 정의된 레이어의 리소스에서 첫 번째 VogkResource를 찾음

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // 사전 정의된 리소스 속성 확인

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource를 잘못 읽음.");

    }

    // 일부 VogkResource 속성 수정

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // 로드된 PSD 파일의 수정된 사본을 경로에 저장

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. lclrResource (시트 색상 설정) 지원**

{{< highlight java >}}

 /*

레이어 시트 색상을 사용하여 레이어를 시각적으로 강조하는 예제. 예를 들어 PSD에서 몇 개의 레이어를 업데이트한 다음 원하는 레이어를 색상으로 강조할 수 있습니다.

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

                // lcrl 리소스는 항상 psd 파일 리소스 목록에 존재함.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("시트 색상이 잘못 읽혔습니다.");

                }

                // 스타일 시트 색상 반전. 레이어 색상 강조 설정

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// 파일의 레이어 색상 강조 순서

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

// 사전 정의된 LclrResource가 포함된 PSD 파일 로드

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

// 방금 저장된 PSD 파일 로드

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // 색상 반전

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. LengthRecord 데이터의 속성 지원. (경로 작업 (부울 연산), 레이어 내 모양의 인덱스, 베지에 노트 레코드 수)**

{{< highlight java >}}

 /*

모양을 다룰 때 경로 작업을 변경하는 예제. 프로그램이 미리 정의된 벡터 경로 레코드(LengthReco rd)를 읽고 경로 작업을 변경한 후 새 PSD 파일로 수정된 사본을 저장.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// vsms 리소스가 포함된 PSD 파일 로드

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // 사전 정의된 레이어의 리소스에서 첫 번째 VsmsResource 찾기

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

    // 모양을 결합하는 방법 변경

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // 로드된 PSD 파일의 수정된 사본을 경로에 저장

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Image Section 리소스 #1010 배경색 지원**

{{< highlight java >}}

 /*

배경색 리소스를 읽고 수정하는 예제.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// 사전 정의된 배경색 리소스 포함 PSD 파일 로드

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

        throw new Exception("배경색 리소스를 찾을 수 없습니다.");

    }

    // 배경색 리소스의 색상 업데이트

    backgroundColorResource.setColor(Color.getDarkRed());

    // 로드된 PSD 파일의 수정된 사본을 경로에 저장

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. 런타임에 채우기 레이어 추가**

{{< highlight java >}}

 /*

다양한 유형의 채우기 레이어를 포함하여 Photoshop 문서에 채우기 레이어를 추가하는 예제.

*/

String outPsdFilePath = "output.psd";

// 빈 캔버스가 있는 Photoshop 문서 생성

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // PSD에 다양한 유형의 채우기 레이어 추가

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Color Fill Layer");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Gradient Fill Layer");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Pattern Fill Layer");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // 로드된 PSD 파일의 수정된 사본을 경로에 저장

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-168. Image Section 리소스 #1009 테두리 정보 지원**

{{< highlight java >}}

 /*

경계 정보 리소스가 포함된 PSD 파일을 읽고 수정하고 저장하는 예제
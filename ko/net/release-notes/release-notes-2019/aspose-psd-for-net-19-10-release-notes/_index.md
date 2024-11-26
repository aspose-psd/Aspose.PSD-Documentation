---
title: Aspose.PSD .NET 19.10 - 릴리스 노트
type: docs
weight: 30
url: /ko/net/aspose-psd-for-net-19-10-release-notes/
---

{{% alert color="primary" %}}

Aspose.PSD .NET 19.10을 위한 릴리스 노트가 포함되어 있는 페이지입니다.

{{% /alert %}}

|**키**|**개요**|**카테고리**|
| :- | :- | :- |
|PSDNET-207|[색상 균형 조정 레이어 지원](/psd/ko/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|기능|
|PSDNET-145|[반전 조정 레이어 지원](/psd/ko/net/modifying-images/#modifyingimages-invertadjustmentlayer)|기능|
|PSDNET-139|[바이큐빅 리샘플러 구현](/psd/ko/net/modifying-images/#modifyingimages-implementbicubicresampling)|기능|
|PSDNET-169|[클리핑 마스크로 PSD 내보내기 지원 추가](/psd/ko/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|기능|
|PSDNET-168|[조정 레이어로 PSD 내보내기 지원 추가](/psd/ko/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|기능|
|PSDNET-179|문제 Get 레이어 DropShadowEffect|향상|
|PSDNET-203|텍스트에 / (슬래시) 문자가 포함된 경우 Photoshop에서 파일을 열 수 없음|버그|
|PSDNET-199|텍스트 레이어에 줄 바꿈만 포함된 PSD 파일을 저장할 수 없음|버그|
|PSDNET-185|잘못된 글꼴 크기 추출|버그|

## **공개 API 변경**

# **추가된 API:**

- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **제거된 API:**

- 없음

## **사용 예시:**

**PSDNET-207. 색상 균형 조정 레이어 지원**

{{< highlight java >}}

var filePath = "ColorBalance.psd";

var outputPath = "ColorBalance_out.psd";

using (var im = (PsdImage)Image.Load(filePath))

{

    foreach (var layer in im.Layers)

    {

        var cbLayer = layer as ColorBalanceAdjustmentLayer;

        if (cbLayer != null)

        {

            cbLayer.ShadowsCyanRedBalance = 30;

            cbLayer.ShadowsMagentaGreenBalance = -15;

            cbLayer.ShadowsYellowBlueBalance = 40;

            cbLayer.MidtonesCyanRedBalance = -90;

            cbLayer.MidtonesMagentaGreenBalance = -25;

            cbLayer.MidtonesYellowBlueBalance = 20;

            cbLayer.HighlightsCyanRedBalance = -30;

            cbLayer.HighlightsMagentaGreenBalance = 67;

            cbLayer.HighlightsYellowBlueBalance = -95;

            cbLayer.PreserveLuminosity = true;

        }

    }

    im.Save(outputPath);

}

{{< /highlight >}}

**PSDNET-145. 반전 조정 레이어 지원**

{{< highlight java >}}

var filePath = "InvertStripes_before.psd";

var outputPath = "InvertStripes_after.psd";

using (var im = (PsdImage)Image.Load(filePath))

{

    im.AddInvertAdjustmentLayer();

    im.Save(outputPath);

}

{{< /highlight >}}

**PSDNET-139. 바이큐빅 리샘플러 구현**

{{< highlight java >}}

string sourceFile = "sample.psd";

string destName = "ResamplerCubicConvolutionStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.CubicConvolution);

    image.Save(destName, new PsdOptions(image));

}


string sourceFile = "sample.psd";

string destName = "ResamplerCatmullRomStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.CatmullRom);

    image.Save(destName, new PsdOptions(image));

}

string sourceFile = "sample.psd";

string destName = "ResamplerMitchellStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.Mitchell);

    image.Save(destName, new PsdOptions(image));

}

string sourceFile = "sample.psd";

string destName = "ResamplerCubicBSplineStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.CubicBSpline);

    image.Save(destName, new PsdOptions(image));

}

string sourceFile = "sample.psd";

string destName = "ResamplerSinCStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.SinC);

    image.Save(destName, new PsdOptions(image));

}

string sourceFile = "sample.psd";

string destName = "ResamplerBellStripes_after.psd";

// 기존 이미지를 로드하여 PsdImage 클래스의 인스턴스로 가져오기

using (PsdImage image = (PsdImage)Image.Load(sourceFile))

{

    image.Resize(300, 300, ResizeType.Bell);

    image.Save(destName, new PsdOptions(image));

}

{{< /highlight >}}

**PSDNET-169. 클리핑 마스크로 PSD 내보내기 지원 추가**

{{< highlight java >}}

using (PsdImage image = (PsdImage)Image.Load("clip.psd"))

{

    image.Save("output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-168. 조정 레이어로 PSD 내보내기 지원 추가**

{{< highlight java >}}

using (PsdImage image = (PsdImage)Image.Load("example.psd"))

{

    image.Save("document.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-203. 텍스트에 / (슬래시) 문자가 포함된 경우 Photoshop에서 파일을 열 수 없음**

{{< highlight java >}}

var psdImage = (PsdImage)image;

var layers = psdImage.Layers;

for (var index = layers.Length - 1; index >= 0; index--)

{

    var layer = layers[index];

    if (!(layer is TextLayer)) continue;

    var textLayer = (TextLayer)layer;

    textLayer.UpdateText("/");

}

var imageOptions = new PsdOptions(psdImage);

var fileName = Path.GetFileName(filePath);

var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

psdImage.Save(outputFilePath, imageOptions);

{{< /highlight >}}

**PSDNET-199. 텍스트 레이어에 줄 바꿈만 포함된 PSD 파일을 저장할 수 없음**

{{< highlight java >}}

string filePath = "testLineBreaks2.psd";

string outputPath = "testLineBreaks2_changed.psd";

var newText = "\r";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-185. 잘못된 글꼴 크기 추출**

{{< highlight java >}}

// 잘못된 글꼴 크기 추출 

string filePath = "直播+电商.psd";

var tolerance = 0.001;

using (var image = Image.Load(filePath))

{

    int layerIndex = 22;

    // 기존 API (첫 번째 단락 글꼴 사용)

    PsdImage psdImage = image as PsdImage;

    double[] matrix = ((TextLayer)psdImage.Layers[layerIndex]).TransformMatrix;

    double baseFontSize = ((TextLayer)psdImage.Layers[layerIndex]).Font.Size;

    double fontSize = matrix[0] * baseFontSize;

    // 기본 글꼴 크기 확인

    if (Math.Abs(100.0 - baseFontSize) > tolerance)

    {

        throw new Exception("글꼴 크기가 잘못 읽혔습니다");

    }

    // 실제 글꼴 크기 확인

    if (Math.Abs(88.425 - fontSize) > tolerance)

    {

        throw new Exception("TransformMatrix가 잘못 읽혔습니다");

    }

    // 새 API (한 텍스트 레이어에 여러 글꼴 크기 포함 가능)

    ITextPortion[] portions = ((TextLayer)psdImage.Layers[layerIndex]).TextData.Items;

    ITextStyle style = portions[0].Style;

    double fontSizeOfPortion = matrix[0] * style.FontSize;

    // 기본 부분 글꼴 크기 확인

    if (Math.Abs(100.0 - style.FontSize) > tolerance)

    {

        throw new Exception("글꼴 크기가 잘못 읽혔습니다");

    }

    // 실제 부분 글꼴 크기 확인

    if (Math.Abs(88.425 - fontSizeOfPortion) > tolerance)

    {

        throw new Exception("TransformMatrix가 잘못 읽혔습니다");

    }

}

{{< /highlight >}}

**PSDNET-179. 문제 Get 레이어 DropShadowEffect**

{{< highlight java >}}

   // DropShadowEffect.UseGlobalLight 속성이 'true'일 때에 DropShadowEffect 객체는 PsdImage.GlobalAngle 속성에서 각도 값을 사용합니다.

    using (PsdImage image = (PsdImage)Image.Load("4.psd"))

    {

        image.GlobalAngle = 30;

        image.Save("output.psd");

    }

{{< /highlight >}}
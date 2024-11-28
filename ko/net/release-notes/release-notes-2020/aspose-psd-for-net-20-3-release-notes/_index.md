---
title: Aspose.PSD for .NET 20.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-188|.Net Core 지원|기능|
|PSDNET-523|Adobe Illustrator 파일을 PDF로 변환|기능|
|PSDNET-212|한 텍스트 레이어에서 다른 스타일 렌더링 기능 추가|기능|
|PSDNET-144|흑백 조정 레이어 지원|기능|
|PSDNET-233|AI 형식(버전 8)을 다른 형식으로 내보내기 지원 추가|기능|
|PSDNET-540|PassThrough 블렌딩 모드 처리 지원 (레이어 그룹 전용)|기능|
|PSDNET-539|빈 Unicode Alpha Names 리소스가 포함된 이미지를로드하면 이미지 로드에 실패하는 예외|버그|
|PSDNET-541|레이어 그룹의 가시성을 변경한 후 부적절한 출력|버그|
|PSDNET-516|PSD 이미지를로드하는 중 예외: RGB의 경우 컬러 섹션 (DropShadow 리소스)은 3 색상 구성 요소를 포함해야하며 CMYK의 경우 4 색상 구성 요소를 포함해야합니다.|버그|
|PSDNET-536|간단한 버전의 생성자를 사용하여 새로 생성된 레이어에 그리려고하면 예외가 발생합니다|버그|

## **공개 API 변경**
# **추가된 API:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **제거된 API:**
- None

## **사용 예시:**
**PSDNET-523. Adobe Illustrator 파일을 PDF로 변환**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. 한 텍스트 레이어에서 다른 스타일 렌더링 기능 추가**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // 텍스트 스타일 "E=mc" 편집

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // 텍스트 스타일 "2\r" 편집

    newPortions[2].Style.FauxBold = true; // 텍스트 스타일 "Bold" 편집

    newPortions[3].Style.FauxItalic = true; // 텍스트 스타일 "Italic\r" 편집

    newPortions[3].Style.BaselineShift = -25; // 텍스트 스타일 "Italic\r" 편집

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // 텍스트 스타일 "Lowercasetext" 편집

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. AI 형식(버전 8)을 다른 형식으로 내보내기 지원 추가**

{{< highlight java >}}

 // AI 파일을 PSD 및 PNG 형식으로 내보내는 예제

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. PassThrough 블렌딩 모드 처리 지원 (레이어 그룹 전용)**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "23번째 레이어가 없습니다.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23번째 레이어가 레이어 그룹이 아닙니다.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "23번째 레이어의 이름이 'AdjustmentGroup'이 아닙니다.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup 레이어는 'pass through' 블렌딩 모드를 가져야합니다.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. 텍스트 레이어 텍스트 업데이트 시 예외 발생**

{{< highlight java >}}

 // 텍스트 레이어 텍스트 업데이트 시 예외 발생

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

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

**PSDNET-182. RotateFlip 작업 후 PSD 이미지 저장 시 손상된 파일이 생성되어 열 수 없는 파일이 생성됨**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// 예외없이 실행되어야 함

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 
{

    // 아무것도 하지 않음

}

{{< /highlight >}}

**PSDNET-539. 빈 Unicode Alpha Names 리소스가 포함된 이미지를로드하면 이미지 로드에 실패하는 예외**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // 여기에서는 예외 없이 실행되어야 합니다

{

    // 아무것도 하지 않음

}

{{< /highlight >}}

**PSDNET-541. 레이어 그룹의 가시성을 변경한 후 부적절한 출력**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// 레이어 이름을 변경하고 저장

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // 그룹 내에서 모든 것을 끕니다

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. PSD 이미지를로드하는 중 예외: 컬러 섹션 (DropShadow 리소스)은 RGB의 경우 3 색상 구성 요소를, CMYK의 경우 4 색상 구성 요소를 포함해야함**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // 여기에서는 예외 없이 실행되어야 함

{

    // 아무것도 하지 않음

}

{{< /highlight >}}

**PSDNET-536. 심플 버전의 생성자를 사용하여 새 레이어에 그리려고하면 예외가 발생함**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // Pen 도구를 사용하여 사각형 그리기

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // 파란색 중첩 브러시로 다른 사각형 그리기

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}


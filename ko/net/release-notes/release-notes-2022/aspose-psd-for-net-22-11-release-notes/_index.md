---
title: Aspose.PSD for .NET 22.11 - 릴리스 노트
type: docs
weight: 20
url: /ko/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

{{% alert color="warning" %}}

- 16비트 내보내기의 경우 이 릴리스에서 회귀가 있어 해당 기능을 사용할 때 주의를 권장합니다.
16비트 이미지 처리가 주요 기능인 경우, Aspose.PSD를 22.9-22.11로 업데이트하지 마십시오.

해당 문제에 대한 해결책을 작업 중에 있습니다.

{{% /alert %}}

|**키**|**개요**|**범주**|
| :- | :- | :- |
|PSDNET-1320|권한부여하려면 매우 큰 PSB 파일을 내보낼 수 없음|개선|
|PSDNET-659|원형 그라데이션의 중심을 이동 가능하게 만듭니다|기능|
|PSDNET-1330|특정 파일에 대한 ZipWithoutPrediction 압축 방식을 지원하지 않음|기능|
|PSDNET-735|레이어에 대해 변형 메서드만 사용한 후에 저장된 레이어의 바운딩 상자가 잘못된 문제|버그|
|PSDNET-1234|패턴이 있는 PSD 이미지를 로드하면 예외 발생|버그|
|PSDNET-1244|중국어 심볼이 있는 PSD 파일 저장 시 이미지 내보내기 실패 (IndexOutOfRangeException)|버그|
|PSDNET-1303|TimeLine ActiveFrame이 부정확하게 적용|버그|
|PSDNET-1307|회귀 22.7: 아랍어 문자가있는 텍스트의 부정확한 렌더링|버그|
|PSDNET-1321|그룹 레이어의 벡터 마스크가 잘못된 작업을 함. 최종 이미지에는 검은 구멍이 있지만 있어서는 안 됨|버그|


## **공개 API 변경 사항**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **제거된 API:**
- 없음


## **사용 예시:**

**PSDNET-659. 원형 그라데이션의 중심을 이동 가능하게 만듭니다**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // 오프셋 지점 업데이트
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. 레이어에 대해 변형 메서드만 사용한 후에 저장된 레이어의 바운딩 상자가 잘못된 문제**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // 텍스트 레이어의 새 크기 설정
    const int NewWidth = 250;
    const int NewHeight = 250;

    // 리사이즈 기능이 레이어를 크기 조정하는 방법 설정 (기본값)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // 여기서 텍스트 레이어의 새로운 리사이징 방법 사용
    // 레이어뿐만 아니라 텍스트 레이어의 변환 행렬도 변경됨
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // 델타의 이유는 기본 글꼴이 다름
    if (txtLayer.TransformMatrix[4] >= 65
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // 모두 정상
    }
    else
    {
        throw new Exception("위치 지점이 잘못되었습니다");
    }
}
{{< /highlight >}}

**PSDNET-1234. 패턴이 있는 PSD 이미지를 로드하면 예외가 발생**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. 중국어 심볼이 있는 PSD 파일 저장 시 이미지 내보내기 실패 (IndexOutOfRangeException)**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // 여기서는 예외가 없어야 합니다.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame이 부정확하게 적용**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. 회귀 22.7: 아랍어 문자가 있는 텍스트의 부정확한 렌더링**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. 매우 큰 PSB 파일을 내보낼 수 없음**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. 그룹 레이어의 벡터 마스크가 잘못된 작업을 함. 최종 이미지에는 검은 구멍이 있지만 있어서는 안 됨**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. 특정 파일에 대한 ZipWithoutPrediction 압축 방식을 지원하지 않음**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}

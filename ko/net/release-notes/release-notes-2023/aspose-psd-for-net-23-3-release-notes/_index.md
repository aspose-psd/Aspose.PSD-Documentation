---
title: Aspose.PSD for .NET 23.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-23-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 23.3](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDNET-146|Posterize 조정 레이어 지원|기능|
|PSDNET-1366|VscgResource 지원 구현|기능|
|PSDNET-1437|Posterize 조정 레이어 데이터를 위한 PostResource 자원 지원 추가|기능|
|PSDNET-931|컬러 모드 CMYK로 조정 및 곡선 조정과 함께 레이어를 PNG로 내보낼 때 부정확함|버그|
|PSDNET-1403|파일 저장 및 PS에 의한 파일 업데이트 후 문단 스타일이 누락됨|버그|
|PSDNET-1453|텍스트의 빛과 그림자 효과가 손상된 렌더링|버그|


## **공용 API 변경점**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.Angle
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.KeyForData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.TypeToolKey


# **제거된 API:**
- 없음


## **사용 예시:**

**PSDNET-146. Posterize Adjustment Layer 지원**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    foreach (Layer layer in image.Layers)
    {
        if (layer is PosterizeLayer)
        {
            ((PosterizeLayer)layer).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-931. CMYK 컬러 모드 및 곡선 조정과 함께 PNG 레이어를 부정확하게 내보내는 오류**

{{< highlight csharp >}}
string srcFile = "input_LevelsLayerWithLayerMaskCmyk.psd";
string outputFile = "output_LevelsLayerWithLayerMaskCmykTest.png";
string outputFilePsd = "output.psd";

var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };
using (PsdImage image = (PsdImage)Image.Load(srcFile, psdLoadOptions))
{
    image.Save(outputFilePsd, new PsdOptions()); // ', new PsdOptions()' 가 버그를 유발합니다.
    image.Save(outputFile, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1366. VscgResource 지원 구현**

{{< highlight csharp >}}
string sourceFile = "StrokeInternalFill_src.psd";
string outputFile = "StrokeInternalFill_res.psd";

void AreEqual(double expected, double current, double tolerance = 0.1)
{
    if (Math.Abs(expected - current) > tolerance)
    {
        throw new Exception(
        $"값이 동일하지 않습니다.\n예상:{expected}\n결과:{current}\n차이:{expected - current}");
    }
}

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(89.8, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(219.6, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(34.2, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);

    ((DoubleStructure)rgbColorStructure.Structures[0]).Value = 255d; // 빨강
    ((DoubleStructure)rgbColorStructure.Structures[1]).Value = 0d; // 녹색
    ((DoubleStructure)rgbColorStructure.Structures[2]).Value = 0d; // 파랑

    image.Save(outputFile);
}

// 변경 사항 확인
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    VscgResource vscgResource = (VscgResource)image.Layers[1].Resources[0];
    DescriptorStructure rgbColorStructure = (DescriptorStructure)vscgResource.Items[0];

    AreEqual(255, ((DoubleStructure)rgbColorStructure.Structures[0]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[1]).Value);
    AreEqual(0, ((DoubleStructure)rgbColorStructure.Structures[2]).Value);
}
{{< /highlight >}}

**PSDNET-1403. 파일 저장 및 PS에 의한 파일 업데이트 후 문단 스타일이 누락됨**

{{< highlight csharp >}}
string sourceFile = "PSDTest3.psd";
string outputFile = "output.psd";

string[] newText = new string[]
{
    "타일 \r",
    "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Qui dicta minus molestiae vel beatae natus"
};

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    TextLayer layer2 = image.AddTextLayer("새 레이어", new Aspose.PSD.Rectangle(117, 150, 350, 100));
    var textDataTL = layer2.TextData;

    ITextStyle defaultStyleTL = textDataTL.ProducePortion().Style;

    ITextParagraph defaultParagraphTL = textDataTL.ProducePortion().Paragraph;
    ITextPortion[] newPortionsTL = textDataTL.ProducePortions(newText, defaultStyleTL, defaultParagraphTL);

    newPortionsTL[0].Style.FontSize = 14;
    newPortionsTL[0].Style.FontName = "TwCenMT-Bold";

    newPortionsTL[1].Style.Leading = 20;
    newPortionsTL[1].Style.FontSize = 10;
    newPortionsTL[1].Style.FontName = "TwCenMT-Bold";

    // 기존 텍스트 제거
    textDataTL.RemovePortion(0);

    // 새 텍스트 부분 추가
    foreach (var newPortion in newPortionsTL)
    {
        textDataTL.AddPortion(newPortion);
    }

    textDataTL.UpdateLayerData();

    image.Save(outputFile);
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(outputFile))
{
    Txt2Resource txt2OutputResource = (Txt2Resource)psdImage.GlobalLayerResources[1];
    byte[] bytes = txt2OutputResource.Data;
    string txt2Data = "";
    for (int i = 18900; i < bytes.Length; i++)
    {
        txt2Data += (char)bytes[i];
    }

    string key0 = @" >> /6 0 >> >> /1 "; // 문단 0의 길이에 대한 접두사
    string key1 = @" >> /6 1 >> >> /1 "; // 문단 1의 길이에 대한 접두사
    int index0 = txt2Data.IndexOf(key0);
    int index1 = txt2Data.IndexOf(key1);

    string lenPar0 = txt2Data.Substring(index0 + key0.Length, 1);
    string lenPar1 = txt2Data.Substring(index1 + key1.Length, 3);

    string expected0 = newText[0].Length.ToString();
    string expected1 = (newText[1].Length + 1).ToString();

    if (lenPar0 != expected0 || lenPar1 != expected1)
    {
        throw new Exception(
            $"문단 길이가 잘못되었습니다.\n예상: {expected0} 및 {expected1}\n결과: {lenPar0} 및 {lenPar1}\n");
    }
}
{{< /highlight >}}

**PSDNET-1437. Posterize Adjustment Layer의 데이터를 위한 PostResource 자원 지원 추가**

{{< highlight csharp >}}
string sourceFile = "zendeya_posterize.psd";
string outputFile = "zendeya_posterize_10.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];

    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is PostResource)
        {
            ((PostResource)resource).Levels = 10;
            image.Save(outputFile);

            break;
        }
    }
}
{{< /highlight >}}

**PSDNET-1453. 텍스트의 빛과 그림자 효과가 손상된 렌더링**

{{< highlight csharp >}}
string outputPsd = "effect_bug.psd";
string outputPng = "effect_bug.png";

using (var psdImage = new PsdImage(500, 500))
{
    // 텍스트 레이어 추가
    Aspose.PSD.Rectangle textArea1 = new Aspose.PSD.Rectangle(50, 0, 400, 100);
    Aspose.PSD.Rectangle textArea2 = new Aspose.PSD.Rectangle(50, 150, 400, 100);
    Aspose.PSD.Rectangle textArea3 = new Aspose.PSD.Rectangle(50, 300, 400, 100);

    TextLayer textLayer1 = psdImage.AddTextLayer("효과 있는 텍스트", textArea1);
    TextLayer textLayer2 = psdImage.AddTextLayer("효과 있는 텍스트", textArea2);
    TextLayer textLayer3 = psdImage.AddTextLayer("효과 있는 텍스트", textArea3);

    // 텍스트 레이어 수정
    textLayer1.TextData.Items[0].Style.FontSize = 150;
    textLayer1.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer1.TextData.UpdateLayerData();

    textLayer2.TextData.Items[0].Style.FontSize = 150;
    textLayer2.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer2.TextData.UpdateLayerData();

    textLayer3.TextData.Items[0].Style.FontSize = 150;
    textLayer3.TextData.Items[0].Style.FillColor = Aspose.PSD.Color.Goldenrod;
    textLayer3.TextData.UpdateLayerData();

    // 효과 추가
    OuterGlowEffect glow = textLayer1.BlendingOptions.AddOuterGlow(); // 중단
    glow.Spread = 15;
    ((ColorFillSettings)glow.FillColor).Color = Color.Red;

    var shadow = textLayer2.BlendingOptions.AddDropShadow(); // 긴 텍스트와 함께 중단
    shadow.Distance = 25;
    shadow.Color = Color.DarkBlue;

    var innerShadow = textLayer3.BlendingOptions.AddInnerShadow(); // 긴 텍스트와 함께 중단
    innerShadow.UseGlobalLight = false;
    innerShadow.Angle = -179;
    innerShadow.Distance = 10;
    innerShadow.Size = 8;
    innerShadow.Color = Color.HotPink;

    // 내보내기
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
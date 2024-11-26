---
title: Aspose.PSD for .NET 22.10 - 릴리스 노트
type: docs
weight: 30
url: /ko/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

{{% alert color="warning" %}}

- 이 릴리스에서 16비트 내보내기의 경우 회귀가 발생하므로 이 기능을 사용할 때 유의해 주시기 바랍니다.
16비트 이미지 처리가 주요 기능이라면 Aspose.PSD를 22.9-22.10으로 업데이트하지 말아 주세요.

이 문제들에 대한 해결 방법을 개발 중에 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-1287|Lfx2Resource의 오래 된 프로퍼티 제거|향상|
|PSDNET-1071|ZipWithoutPrediction 압축을 사용한 PSD (RGB/16비트)를 열 수 없음|버그|
|PSDNET-1257|타임라인 효과가 사라지고 이상하게 표시됨. (Photoshop에서)|버그|
|PSDNET-1278|내부 위치를 사용한 효과에 대한 투명도가 작동하지 않음|버그|
|PSDNET-1279|회귀: PSD 파일 열기 오류|버그|
|PSDNET-1284|일부 아시아 기호로 인해 텍스트 업데이트 실패. 특정 기호 구문 분석 오류|버그|
|PSDNET-1291|일부 아시아 기호로 인해 텍스트 업데이트 실패. 특정 기호 렌더링 오류|버그|
|PSDNET-1292|구체적인 아시아 기호 저장 후 Photoshop에서 내보낸 파일 열기 오류|버그|


## **공개 API 변경**
# **추가된 API:**
- 없음


# **제거된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **사용 예시:**

**PSDNET-1071. Aspose.PSD can't open PSD (RGB/16bit) with ZipWithoutPrediction compression**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Timeline effects disappear and show in a strange way. (in Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Create timeline with few frames.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. Transparency is not working for the Stroke effect with Inside Position**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regression: Error on the opening of PSD File**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. The text update fails with some Asian symbols. Error with parsing specific symbol**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟프就尲尳尴행족졲졳존졵졶졷졸졹졺졻졼졽졾졿
좀좁좂좃좄종";

testData = testData.Substring(25, 1); // 문제가 되는 기호 선택

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Remove obsolete properties in Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Update effect BlendMode option
    effect.BlendMode = BlendMode.Darken;

    // Update effect Opacity option
    effect.Opacity = 128; // 50%

    // Update stroke effect fill Color option
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. The text update fails with some Asian symbols. Error on rendering specific symbol**

{{< highlight csharp >}}
string testData = @"뜀뜁뜂뜃뜄뜕뜆뜇뜍뜏뜐뜑뜒뜖뜗뜘뜜뜤뜬뜭띞띡
띢띣띤띥띦";

testData = testData.Substring(40, 25); // 문제가 되는 기호 선택

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Error on opening the exported file by Photoshop after saving specific Asian symbols**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚프就행족졲졳졶졷졻졼종좆
좇좡좢좣좤";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}

---
title: Aspose.PSD for .NET 24.6 - 릴리스 노트
type: docs
weight: 70
url: /ko/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지는 [Aspose.PSD for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트를 포함합니다.

{{% /alert %}}

| **키**     | **요약**                                                                         | **카테고리** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | 그라디언트 맵 레이어 지원 구현                                                                               | 기능      |
| PSDNET-1670 | [AI 형식] AI 형식에 XPacket 메타데이터 지원 추가                                                                               | 기능      |
| PSDNET-1831 | 팽창, 압축, 비틀기 유형의 와프 구현                                                                               | 기능      |
| PSDNET-1653 | RGB 및 Lab 모드는 ArtBoard 레이어를 포함하는 파일에서 3개 미만 또는 4개 초과의 채널을 포함할 수 없음                                                                               | 버그      |
| PSDNET-1775 | 특정 파일 처리 중 처리 영역 상단은 양수여야 함. (매개 변수 'areaToProcess')                                                                               | 버그      |
| PSDNET-2052 | 저장 후 캔버스 이미지가 잘림. 데이터 손실은 있지만 미리보기는 정상적으로 보임                                                                               | 버그      |

## **공개 API 변경 사항**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-1450. 그라디언트 맵 레이어 지원 구현**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // 그라디언트 맵 조정 레이어 추가.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// 저장된 변경 사항 확인
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [AI 형식] AI 형식에 XPacket 메타데이터 지원 추가**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objects are not equal.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Test object are null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Xmp 메타데이터가 추가되었습니다.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // 이제 AI 파일의 Xmp 패키지에 액세스할 수 있습니다.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // 그리고 이러한 패키지의 내용에 액세스할 수 있습니다.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. 팽창, 압축, 비틀기 유형의 와프 구현**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. RGB 및 Lab 모드는 ArtBoard 레이어를 포함하는 파일에서 3개 미만 또는 4개 초과의 채널을 포함할 수 없음**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // 여기에는 예외가 없어야 합니다.
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. 특정 파일 처리 중 처리 영역 상단은 양수여야 함. (매개 변수 'areaToProcess')**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // 예외가 발생하지 않아야 함
}
{{< /highlight >}}

**PSDNET-2052. 저장 후 캔버스 이미지가 잘림. 데이터 손실은 있지만 미리보기는 정상적으로 보임**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // 여기에 오류가 없어야 합니다.
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // 여기에 오류가 없어야 합니다.
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

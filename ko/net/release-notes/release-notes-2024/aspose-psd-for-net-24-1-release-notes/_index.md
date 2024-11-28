---
title: Aspose.PSD for .NET 24.1 - 릴리스 노트
type: docs
weight: 120
url: /ko/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**      | **요약**                                                                                           | **카테고리** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI 형식] 다중 페이지 AI 이미지에 대한 기본 처리 추가                                           |   기능      |
| PSDNET-718  | 텍스트에 Warp Text 효과가 적용되지 않음                                                          |     버그    |
| PSDNET-1620 | 특정 파일에서 마스크의 잘못된 렌더링                                                             |     버그    |
| PSDNET-1855 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor에서 NullReferenceException |     버그    |
| PSDNET-1883 | [AI 형식] AiExporterUtils에서 메모리 사용량 수정                                                   |     버그    |



## **공개 API 변경 사항**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **제거된 API:**
- 없음


## **사용 예시:**

**PSDNET-718. 텍스트에 Warp Text 효과가 적용되지 않음**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. 특정 파일에서 마스크의 잘못된 렌더링**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI 형식] 다중 페이지 AI 이미지에 대한 기본 처리 추가**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// AI 이미지 로드
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // 기본적으로 ActivePageIndex는 0입니다.
    // 이 속성을 변경하지 않고 AI 이미지를 저장하면 첫 번째 페이지가 렌더링되어 저장됩니다.
    image.Save(firstPageOutputPng, new PngOptions());

    // ActivePageIndex를 두 번째 페이지로 변경
    image.ActivePageIndex = 1;

    // AI 이미지의 두 번째 페이지를 PNG 이미지로 저장
    image.Save(secondPageOutputPng, new PngOptions());

    // ActivePageIndex를 세 번째 페이지로 변경
    image.ActivePageIndex = 2;

    // AI 이미지의 세 번째 페이지를 PNG 이미지로 저장
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor에서 NullReferenceException**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI 형식] AiExporterUtils에서 메모리 사용량 수정**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// AI 이미지 로드
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // AI 이미지의 첫 번째 페이지를 PNG 이미지로 저장
    image.Save(firstPageOutputPng, new PngOptions());

    // ActivePageIndex를 두 번째 페이지로 변경
    image.ActivePageIndex = 1;

    // AI 이미지의 두 번째 페이지를 PNG 이미지로 저장
    image.Save(secondPageOutputPng, new PngOptions());

    // ActivePageIndex를 세 번째 페이지로 변경
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("메모리 사용량이 너무 많습니다. " + memoryUsed + " 대신 " + MemoryLimit.ToString("F1") + "을(를) 사용했습니다");
}
{{< /highlight >}}

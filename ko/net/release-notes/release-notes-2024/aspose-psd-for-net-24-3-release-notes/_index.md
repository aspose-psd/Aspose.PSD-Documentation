---
title: Aspose.PSD for .NET 24.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지는 [Aspose.PSD for .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트를 포함합니다.

{{% /alert %}}

| **키**     | **요약**                                                          | **카테고리** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI 형식] 대규모 다중 페이지 AI 이미지의 로딩 시간 감소         |     향상     |
| PSDNET-1905 | 8비트를 16비트로 변환한 PSD 파일이 읽을 수 없게 됨 |     버그     |
| PSDNET-1906 | 8비트를 32비트로 변환한 PSD 파일이 읽을 수 없게 됨 |     버그     |
| PSDNET-1921 | [AI 형식] AI 파일의 Short Curve 렌더링 수정                 |     버그     |

## **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-1905. 8비트를 16비트로 변환한 PSD 파일이 읽을 수 없게 됨**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("잘못된 글로벌 리소스, 첫 번째 리소스는 Lr16Resource여야 함");
    }
}
{{< /highlight >}}

**PSDNET-1906. 8비트를 32비트로 변환한 PSD 파일이 읽을 수 없게 됨**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("잘못된 글로벌 리소스, 첫 번째 리소스는 Lr32Resource여야 함");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI 형식] AI 파일의 Short Curve 렌더링 수정**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

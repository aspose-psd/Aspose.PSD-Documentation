---
title: Aspose.PSD for .NET 22.6 - 릴리스 노트
type: docs
weight: 70
url: /ko/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-940|다른 파일에서 유사한 레이어의 고유 해시를 가져 오는 API 생성|개선사항|
|PSDNET-678|패턴이 하나 이상이고 레이어 순서가 변경된 경우 FillLayer의 잘못된 렌더링|버그|
|PSDNET-1125|CMYK 색상 모드를 사용하는 특정 PSD 파일로드시 예외 발생|버그|


## **공개 API 변경**
# **추가 된 API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **제거 된 API:**
- 없음


## **사용 예시:**

**PSDNET-678. 패턴이 하나 이상이고 레이어 순서가 변경된 경우 FillLayer의 잘못된 렌더링**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. 다른 파일에서 유사한 레이어의 고유 해시를 가져 오는 API 생성**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        // 코드 생략
    }

    // 기타 메소드들 생략
}
{{< /highlight >}}

**PSDNET-1125. CMYK 색상 모드를 사용하는 특정 PSD 파일로드시 예외 발생**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
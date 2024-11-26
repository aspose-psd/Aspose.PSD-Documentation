---
title: Aspose.PSD for .NET 21.6 - 릴리스 노트
type: docs
weight: 70
url: /ko/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**개요**|**범주**|
| :- | :- | :- |
|PSDNET-546|그룹에 대한 클리핑 마스크가 올바르게 렌더링되지 않음|버그|
|PSDNET-547|레이어 그룹의 일반 또는 벡터 마스크가 렌더링 중 무시됨|버그|
|PSDNET-647|저장 시 벡터 레이어 마스크를 비활성화 한 PSD 이미지는 벡터 마스크를 활성화함|버그|
|PSDNET-786|255자를 초과하는 긴 텍스트를 포함하는 TextLayer를 만들 때 예외 발생|버그|
|PSDNET-900|Linux에서 Text 레이어의 텍스트가 렌더링되지 않음|향상|

## **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-546. 그룹에 대한 클리핑 마스크가 올바르게 렌더링되지 않음**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. 레이어 그룹의 일반 또는 벡터 마스크가 렌더링 중 무시됨**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. 저장 시 벡터 레이어 마스크를 비활성화 한 PSD 이미지는 벡터 마스크를 활성화함**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. 255자를 초과하는 긴 텍스트를 포함하는 TextLayer를 만들 때 예외 발생**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}

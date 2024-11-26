---
title: Aspose.PSD for .NET 22.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-210|레이어 그룹에 대한 IsOpen 속성 추가|기능|
|PSDNET-643|래스터 레이어 마스크가 있는 PSD 이미지가 16비트 PSD 이미지로 저장 시 마스크가 삭제됨|버그|
|PSDNET-899|디졸브 혼합 모드가 마스크가 있는 폴더에 적용되지 않음|버그|
|PSDNET-1047|Aspose.PSD 21.11에서 저장 후 Photoshop에서 특정 파일을 열 수 없음|버그|
|PSDNET-1068|선형 더지 (더하기) 블렌드 모드를 가진 레이어의 잘못된 렌더링|버그|
|PSDNET-1069|로드 후 패턴 채우기 레이어가 업데이트 시 예외 발생|버그|


## **퍼블릭 API 변경 사항**
# **추가된 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **제거된 API:**
- 없음


## **사용 예시:**

**PSDNET-210. 레이어 그룹에 대한 IsOpen 속성 추가**

{{< highlight csharp >}}
// 런타임에서 IsOpen 속성을 읽고 쓰는 예시.
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. 래스터 레이어 마스크가 있는 PSD 이미지가 16비트 PSD 이미지로 저장 시 마스크가 삭제됨**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. 디졸브 혼합 모드가 마스크가 있는 폴더에 적용되지 않음**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Aspose.PSD 21.11에서 저장 후 Photoshop에서 특정 파일을 열 수 없음**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // Photoshop으로 출력 PSD를 수동으로 열어야 함.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // 예외가 발생하지 않음.
            }
{{< /highlight >}}

**PSDNET-1068. 선형 더지 (더하기) 블렌드 모드를 가진 레이어의 잘못된 렌더링**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. 로드 후 패턴 채우기 레이어가 업데이트 시 예외 발생**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}

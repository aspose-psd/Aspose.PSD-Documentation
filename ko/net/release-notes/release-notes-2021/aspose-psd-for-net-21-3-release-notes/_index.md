---
title: Aspose.PSD for .NET 21.3 - 릴리스 노트
type: docs
weight: 100
url: /ko/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}} 

이 페이지는 [Aspose.PSD for .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트를 포함하고 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-823|레이어 그룹과의 경험을 향상시키기 위해 SectionDividerLayer를 추가|강화|
|PSDNET-694|PattResource를 읽을 때 너비와 높이가 바뀌었습니다|버그|
|PSDNET-789|둘 이상의 레이어 효과의 부정확한 블렌딩|버그|
|PSDNET-805|둘 이상의 레이어 효과가 있는 경우 부정확한 블렌딩 순서 및 논리|버그|
|PSDNET-842|스트로크 효과 속성이 PSD 파일에 저장되지 않음|버그|

## **공개 API 변경**
# **추가된 API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-694. PattResource를 읽을 때 너비와 높이가 바뀌었습니다**

{{< highlight csharp >}}
            string sourceFile = "Untitled-1.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[1];
                fillLayer.Update(); // 패턴 렌더링 호출

                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. 둘 이상의 레이어 효과의 부정확한 블렌딩**

{{< highlight csharp >}}
            string srcFile = "source_789.psd";
            string outputSmartObjectPath = "output789.png";
            string outputFile = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var imageInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < imageInSmart.Layers.Length; j++)

                                {
                                    // 텍스트 레이어 찾기
                                    var textLayer = imageInSmart.Layers[j] as TextLayer;
                                    if (textLayer != null)
                                    {
                                        var textData = textLayer.TextData;

                                        textData.Items[0].Text = "Best";
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageInSmart);
                            }
                        }

                        break;
                    }
                }
                // 이 방법으로 변경된 PSD 파일을 저장합니다
                image.Save(outputSmartObjectPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFile);
            }
{{< /highlight >}}

**PSDNET-805. 둘 이상의 레이어 효과가 있는 경우 부정확한 블렌딩 순서 및 논리**

{{< highlight csharp >}}
            string sourceFile = "1_200x200.psd";
            string contentFile = "Numbers1Best.png";

            string outputFilePng = "output.png";
            string outputFilePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(contentFile);
                        break;
                    }
                }

                // 이 방법으로 변경된 PSD 파일을 저장합니다
                image.Save(outputFilePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(outputFilePsd);
            }
{{< /highlight >}}

**PSDNET-823. 레이어 그룹과의 경험을 향상시키기 위해 SectionDividerLayer 추가**

{{< highlight csharp >}}
            // 다음 코드는 SectionDividerLayer 레이어 및 관련 LayerGroup을 가져오는 방법을 보여줍니다.

            // 레이어 계층 구조
            //    [0]: 'Layer group' 그룹 1에 대한 SectionDividerLayer
            //    [1]: '레이어 1' 일반 레이어
            //    [2]: '</레이어 그룹>' 그룹 2에 대한 SectionDividerLayer
            //    [3]: '</레이어 그룹>' 그룹 3에 대한 SectionDividerLayer
            //    [4]: '그룹 3' 그룹 레이어
            //    [5]: '그룹 2' 그룹 레이어
            //    [6]: '그룹 1' 그룹 레이어

            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objects are not equal.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // 레이어 계층 구조 만들기
                // 레이어 그룹 '그룹 1' 추가
                LayerGroup group1 = image.AddLayerGroup("그룹 1", 0, true);
                // 일반 레이어 추가
                Layer layer1 = new Layer();
                layer1.DisplayName = "레이어 1";
                group1.AddLayer(layer1);
                // 레이어 그룹 '그룹 2' 추가
                LayerGroup group2 = group1.AddLayerGroup("그룹 2", 1);
                // 레이어 그룹 '그룹 3' 추가
                LayerGroup group3 = group2.AddLayerGroup("그룹 3", 0);

                // SectionDividerLayer 가져오기
                SectionDividerLayer divider1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer divider2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer divider3 = (SectionDividerLayer)image.Layers[3];

                // SectionDividerLayer.GetRelatedLayerGroup() 메서드를 사용하여 관련 LayerGroup 인스턴스를 얻습니다.
                AssertAreEqual(group1.DisplayName, divider1.GetRelatedLayerGroup().DisplayName); // 동일한 LayerGroup
                AssertAreEqual(group2.DisplayName, divider2.GetRelatedLayerGroup().DisplayName); // 동일한 LayerGroup
                AssertAreEqual(group3.DisplayName, divider3.GetRelatedLayerGroup().DisplayName); // 동일한 LayerGroup

                LayerGroup folder1 = divider1.GetRelatedLayerGroup();
                AssertAreEqual(5, folder1.Layers.Length); // '그룹 1'에는 5개의 레이어가 있음
            }
{{< /highlight >}}

**PSDNET-842. 스트로크 효과 속성이 PSD 파일에 저장되지 않음**

{{< highlight csharp >}}
            void AssertAreEqual(object expected, object actual, string message = null)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new FormatException(message ?? "Objects are not equal.");
                }
            }

            string srcFile = "badStrokeEffect.psd";
            string output = "output.psd";

            using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var layer1 = new Layer();
                image.AddLayer(layer1);
                layer1.BlendingOptions.AddStroke(FillType.Color); // ArgumentNullException을 throw하지 않음

                StrokeEffect strokeEffect = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                strokeEffect.Size = 10;
                strokeEffect.Position = StrokePosition.Outside;
                strokeEffect.Overprint = true;

                image.Save(output);
            }

            // 저장된 값 확인
            using (var image = (PsdImage)Image.Load(output, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect strokeEffect = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, strokeEffect.Size);
                AssertAreEqual(StrokePosition.Outside, strokeEffect.Position);
                AssertAreEqual(true, strokeEffect.Overprint);
            }
{{< /highlight >}}

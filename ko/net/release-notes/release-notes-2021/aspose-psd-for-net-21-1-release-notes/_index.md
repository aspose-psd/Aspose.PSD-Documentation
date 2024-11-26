---
title: Aspose.PSD for .NET 21.1 - 릴리스 노트
type: docs
weight: 120
url: /ko/net/aspose-psd-for-net-21-1-release-notes/
---

{{% alert color="primary" %}} 

이 페이지에는 [Aspose.PSD for .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: 특정 Psd 파일을 png로 변환하려고 할 때 예외 발생|버그|
|PSDNET-792|스마트 객체가 포함된 PSD를 PNG로 저장할 때 예외 발생|버그|

## **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예시:**
**PSDNET-766. Aspose.PSD 20.10: 특정 Psd 파일을 png로 변환하려고 할 때 예외 발생**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET766_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "school-admission-flyer-template-05052019.psd";
            string outputFilePath = outputFolder + "chool-admission-flyer-template-05052019_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions();
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-792. 스마트 객체가 포함된 PSD를 PNG로 저장할 때 예외 발생**
{{< highlight csharp >}}
            const string baseFolder = "PSDNET792_1\\";
            const string outputFolder = baseFolder + "output\\";
            string sourceFilePath = baseFolder + "1.psd";
            string outputFilePath = outputFolder+ "1_output.psd";
            string outputPngFilePath = Path.ChangeExtension(outputFilePath, ".png");
            PsdLoadOptions options = new PsdLoadOptions() { LoadEffectsResource = true };
            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, options))
            {
                var length = image.Layers.Length;
                for (int i = 0; i < length; i++)
                {
                    // 스마트 객체 찾기
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        // 스마트 객체 레이어를 메모리 스트림에서로드하며,
                        // smart smart.ExportContents(somePath)를 사용하여 스마트 객체를 파일로 내보낼 수 있습니다
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
                                        // UpdateText를 사용할 수 있지만이 방법을 통해 텍스트를 부분적으로 편집할 수 있습니다
                                        // 여러 행의 텍스트 레이어 및 기타 텍스트 및 문단 스타일링 기능 생성
                                        // 주의해야 합니다. 스마트 객체 내용이 PSD가 아닌 경우 이 방법을 사용할 수 없습니다
                                        // 이 경우 그래픽 API를 사용해야합니다: https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var textData = textLayer.TextData;
                                        textData.Items[0].Text = "최고";

                                        // 이미지가 잘 보이도록 텍스트 크기를 변경해야 합니다.
                                        textData.Items[0].Style.FontSize = 170;
                                    }
                                }

                                // ReplaceContents를 사용하는 것이 좋습니다. 스마트 객체를 자동으로 재랜더링합니다
                                smart.ReplaceContents(imageInSmart);
                            }
                        }
                    }
                }

                // 변경된 PSD 파일을 저장하는 방법
                image.Save(outputFilePath, new PsdOptions(image));
                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

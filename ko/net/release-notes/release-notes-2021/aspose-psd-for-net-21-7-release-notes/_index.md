---
title: Aspose.PSD for .NET 21.7 - 릴리스 노트
type: docs
weight: 60
url: /ko/net/aspose-psd-for-net-21-7-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 21.7](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-806|TextPortions를 사용한 글꼴 편집 지원|기능|
|PSDNET-917|Aspose.PSD 21.6: PSD를 PNG로 변환하려는 시도 시 ImageSaveException 발생|버그|
|PSDNET-858|Aspose.PSD .Net 5.0 구성에 추가|기능 향상|

## **공개 API 변경 사항**
# **추가된 API:**
- M:Aspose.PSD.FontSettings.GetAdobeFontName(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontName

# **제거된 API:**
- 없음

## **사용 예제:**

**PSDNET-806. TextPortions를 사용한 글꼴 편집 지원**

{{< highlight csharp >}}
            string outputFilePng = "result_fontEditTest.png";
            string outputFilePsd = "fontEditTest.psd";

            void AssertAreEqual(object expected, object actual)
            {
                if (!object.Equals(expected, actual))
                {
                    throw new Exception("오브젝트가 동일하지 않습니다.");
                }
            }

            using (var image = new PsdImage(500, 500))
            {
                FillLayer backgroundFillLayer = FillLayer.CreateInstance(FillType.Color);
                ((IColorFillSettings)backgroundFillLayer.FillSettings).Color = Color.White;
                image.AddLayer(backgroundFillLayer);

                TextLayer textLayer = image.AddTextLayer("Text 1", new Rectangle(10, 35, image.Width, 35));

                ITextPortion firstPortion = textLayer.TextData.Items[0];
                firstPortion.Style.FontName = FontSettings.GetAdobeFontName("Comic Sans MS");

                var secondPortion = textLayer.TextData.ProducePortion();
                secondPortion.Text = "Text 2";
                secondPortion.Paragraph.Apply(firstPortion.Paragraph);
                secondPortion.Style.Apply(firstPortion.Style);
                secondPortion.Style.FontName = FontSettings.GetAdobeFontName("Arial");

                textLayer.TextData.AddPortion(secondPortion);
                textLayer.TextData.UpdateLayerData();

                image.Save(outputFilePng, new PngOptions());
                image.Save(outputFilePsd);
            }

            using (var image = (PsdImage)Image.Load(outputFilePsd))
            {
                TextLayer textLayer = (TextLayer)image.Layers[2];

                string adobeFontName1 = FontSettings.GetAdobeFontName("Comic Sans MS");
                string adobeFontName2 = FontSettings.GetAdobeFontName("Arial");

                AssertAreEqual(adobeFontName1, textLayer.TextData.Items[0].Style.FontName);
                AssertAreEqual(adobeFontName2, textLayer.TextData.Items[1].Style.FontName);
            }
{{< /highlight >}}

**PSDNET-917. Aspose.PSD 21.6: PSD를 PNG로 변환하려는 시도 시 ImageSaveException**

{{< highlight csharp >}}
            string srcFile = "input.psd";
            string output = "output.png";

            using (var image = Aspose.PSD.Image.Load(srcFile))
            {
                image.Save(output, new Aspose.PSD.ImageOptions.PngOptions());
            }
{{< /highlight >}}

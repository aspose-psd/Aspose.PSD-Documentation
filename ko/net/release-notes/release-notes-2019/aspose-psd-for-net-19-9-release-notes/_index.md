---
title: Aspose.PSD for .NET 19.9 - 릴리스 노트
type: docs
weight: 40
url: /ko/net/aspose-psd-for-net-19-9-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-160|잘못된 레이어 이름이 추출됨|기능|
|PSDNET-175|PSD TextLayer 내의 다른 텍스트 부분에서 텍스트 속성 가져오기|기능|
|PSDNET-190|레이어 그룹 추가 지원|기능|
|PSDNET-192|그라디언트 채우기 레이어의 스케일 속성 지원|기능|
|PSDNET-162|명도 조정|개선|
|PSDNET-174|PSD 이미지를 JPEG로 저장할 때 IndexOutOfRangeException 발생|버그|
|PSDNET-180|텍스트 레이어 텍스트를 업데이트하면 예외가 발생함|버그|
|PSDNET-182|RotateFlip 작업 후 PSD 이미지를 저장하면 파일 손상으로 열 수 없음|버그|

## **공용 API 변경**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **삭제된 API:**
- 없음

## **사용 예시:**
**PSDNET-160. 잘못된 레이어 이름이 추출됨**

레이어 이름을 제대로 표시하려면 **DisplayName** 속성을 사용하세요. 이 속성에 대한 setter가 추가되었고 이제 속성을 수정할 수 있습니다. Photoshop이 한글 문자를 Name 속성을 이용해 레이어 이름을 저장할 때 이를 ASCII의 바이트 63'?'로 저장합니다. Name 속성은 한글 문자를 지원하지 않으므로 **DisplayName** 속성을 사용하세요.

{{< highlight java >}}

             // 레이어 이름을 변경하고 저장합니다.

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // DisplayName 속성에 새 값 설정

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. PSD TextLayer 내의 다른 텍스트 부분에서 텍스트 속성 가져오기**

{{< highlight java >}}

            const double Tolerance = 0.0001;

            var filePath = "ThreeColorsParagraphs.psd";

            var outputPath = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var portions = layer.TextData.Items;

                        if (portions.Length != 4)

                        {

                            throw new Exception();

                        }

                        // 각 부분의 텍스트 확인

                        if (portions[0].Text != "Old " ||

                            portions[1].Text != "color" ||

                            portions[2].Text != " text\r" ||

                            portions[3].Text != "Second paragraph\r")

                        {

                            throw new Exception();

                        }

                        // 단락 데이터 확인

                        // 단락들은 다른 정당성을 가짐

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // 첫 번째와 두 번째 단락의 모든 다른 속성들이 동일함

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var paragraph = portions[j].Paragraph;

                            if (Math.Abs(paragraph.AutoLeading - 1.2) > Tolerance ||

                                paragraph.AutoHyphenate != false ||

                                paragraph.Burasagari != false ||

                                paragraph.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraph.StartIndent) > Tolerance ||

                                Math.Abs(paragraph.EndIndent) > Tolerance ||

                                paragraph.EveryLineComposer != false ||

                                Math.Abs(paragraph.FirstLineIndent) > Tolerance ||

                                paragraph.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraph.GlyphSpacing[0] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[1] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[2] - 1) > Tolerance ||

                                paragraph.Hanging != false ||

                                paragraph.HyphenatedWordSize != 6 ||

                                paragraph.KinsokuOrder != 0 ||

                                paragraph.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraph.LetterSpacing[0]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[1]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[2]) > Tolerance ||

                                paragraph.LeadingType != LeadingMode.Auto ||

                                paragraph.PreHyphen != 2 ||

                                paragraph.PostHyphen != 2 ||

                                Math.Abs(paragraph.SpaceBefore) > Tolerance ||

                                Math.Abs(paragraph.SpaceAfter) > Tolerance ||

                                paragraph.WordSpacing.Length != 3 ||

                                Math.Abs(paragraph.WordSpacing[0] - 0.8) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[1] - 1.0) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[2] - 1.33) > Tolerance ||

                                Math.Abs(paragraph.Zone - 36.0) > Tolerance)

                            {

                                throw new Exception();

                            }

                        }

                        // 스타일 데이터 확인

                        // 스타일은 다른 색상과 글꼴 크기를 가짐

                        if (Math.Abs(portions[0].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[1].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[2].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[3].Style.FontSize - 10) > Tolerance)

                        {

                            throw new Exception();

                        }

                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var style = portions[j].Style;

                            if (style.AutoLeading != false ||

                                style.HindiNumbers != false ||

                                style.Kerning != 0 ||

                                style.Leading != 0 ||

                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                style.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // 텍스트 편집 예시

                        portions[0].Text = "Hello ";

                        portions[1].Text = "World";

                        // 텍스트 부분 제거 예시

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // 새로운 텍스트 부분 추가 예시

                        var createdPortion = layer.TextData.ProducePortion();

                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // 부분에 대한 단락 및 스타일 편집 예시

                        // 정당화를 오른쪽으로 설정

                        portions[0].Paragraph.Justification = 1;

                        portions[1].Paragraph.Justification = 1;

                        portions[2].Paragraph.Justification = 1;

                        // 각 스타일을 위한 다른 색상. 변경되지만 렌더링은 완전히 지원되지 않음

                        portions[0].Style.FillColor = Color.Aquamarine;

                        portions[1].Style.FillColor = Color.Violet;

                        portions[2].Style.FillColor = Color.LightBlue;

                        // 다른 글꼴. 변경되지만 렌더링은 완전히 지원되지 않음

                        portions[0].Style.FontSize = 6;

                        portions[1].Style.FontSize = 8;

                        portions[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(outputPath, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. 레이어 그룹 추가 지원**

{{< highlight java >}}

             // -그룹 1

            // --레이어 1

            // --그룹 2

            // ---레이어 2

            // ---레이어 3

            // --레이어 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();

            createOptions.Source = new FileCreateSource(dataDir, false);

            createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

            {

                LayerGroup group1 = psdImage.AddLayerGroup("Group 1", 0, true);

                Layer layer1 = new Layer(psdImage);

                layer1.Name = "Layer 1";

                group1.AddLayer(layer1);

                LayerGroup group2 = group1.AddLayerGroup("Group 2", 1);

                Layer layer2 = new Layer(psdImage);

                layer2.Name = "Layer 2";

                group2.AddLayer(layer2);

                Layer layer3 = new Layer(psdImage);

                layer3.Name = "Layer 3";

                group2.AddLayer(layer3);

                Layer layer4 = new Layer(psdImage);

                layer4.Name = "Layer 4";

                group1.AddLayer(layer4);

                psdImage.Save();

            }

{{< /highlight >}}

**PSDNET-192. 그라디언트 채우기 레이어의 스케일 속성 지원**

{{< highlight java >}}

            using (var image = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // 채우기 레이어 가져오기

                FillLayer fillLayer = null;

                foreach (var layer in image.Layers)

                {

                    fillLayer = layer as FillLayer;

                    if (fillLayer != null)

                    {

                        break;

                    }

                }

                var settings = fillLayer.FillSettings as IGradientFillSettings;

                // 스케일 값 업데이트

                settings.Scale = 200;

                fillLayer.Update(); // 픽셀 데이터 업데이트

                image.Save("scaledImage.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-174. PSD 이미지를 JPEG로 저장할 때 IndexOutOfRangeException 발생**

{{< highlight java >}}

         using (var image = Aspose.PSD.Image.Load("SamplePSD.psd"))

        {

            image.Save("sampleJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. 텍스트 레이어 텍스트를 업데이트하면 예외가 발생함**

{{< highlight java >}}

           // 텍스트 레이어 텍스트를 업데이트하면 예외가 발생함

            string filePath = "FlipVertical.psd";

            string
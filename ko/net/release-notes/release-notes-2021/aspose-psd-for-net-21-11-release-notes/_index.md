---
title: Aspose.PSD for .NET 21.11 - 릴리스 노트
type: docs
weight: 20
url: /ko/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

이 페이지는 [Aspose.PSD for .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)의 릴리스 노트를 포함하고 있습니다.

{{% /alert %}} 

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDNET-767|기존 텍스트 레이어를 레이어 그룹에 추가할 때 예외 발생|버그|
|PSDNET-988|TextLayer.UpdateText에서 IndexOutOfRangeException 발생|버그|
|PSDNET-989|내보낸 모어들이 결과 파일에서 잘못된 좌표를 가짐|버그|
|PSDNET-1002|폴더 내보낼 때 벡터 모양이 잘못 내보내짐|버그|

## **공개 API 변경 사항**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDNET-767. 기존 텍스트 레이어를 레이어 그룹에 추가할 때 예외 발생**

{{< highlight csharp >}}
            string outputPsd = "out_dummy_group.psd";

            var psdOptions = new PsdOptions()
            {
                Source = new StreamSource(new MemoryStream(), true),
                ColorMode = ColorModes.Rgb,
                ChannelsCount = 4,
                ChannelBitsCount = 8,
                CompressionMethod = CompressionMethod.RLE
            };
            using (PsdImage image = (PsdImage)Image.Create(psdOptions, 10, 15))
            {
                var group = image.AddLayerGroup("TestGroup", 0, true);
                var layer = image.AddTextLayer("Text", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. TextLayer.UpdateText에서 IndexOutOfRangeException 발생**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fonts";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Mom", "Stacy" };
            string[] fonts = new[] { "Caveat", "Gochi Hand", "Lobster", "Satisfy" };

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                foreach (var layer in image.Layers)
                {
                    var txtLayer = layer as TextLayer;
                    if (txtLayer != null)
                    {
                        for (int w = 0; w < words.Length; w++)
                        {
                            for (int f = 0; f < fonts.Length; f++)
                            {
                                txtLayer.UpdateText(words[w]);
                                foreach (var txtItem in txtLayer.TextData.Items)
                                {
                                    txtItem.Style.FontName = FontSettings.GetAdobeFontName(fonts[f]);
                                }

                                txtLayer.TextData.UpdateLayerData();
                            }
                        }
                    }
                }

                image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-989. 내보낸 모양들이 결과 파일에서 잘못된 좌표를 가짐**

{{< highlight csharp >}}
        public void CreatingVectorPathExample()
        {
            string outputPsd = "outputPsd.psd";

            using (var psdImage = (PsdImage)Image.Create(new PsdOptions() { Source = new Sources.StreamSource(new MemoryStream()), }, 500, 500))
            {
                FillLayer layer = FillLayer.CreateInstance(PSD.FileFormats.Psd.Layers.FillSettings.FillType.Color);
                psdImage.AddLayer(layer);

                VectorPath vectorPath = VectorDataProvider.CreateVectorPathForLayer(layer);
                vectorPath.FillColor = Color.IndianRed;
                PathShape shape = new PathShape();
                shape.Points.Add(new BezierKnot(new PointF(50, 150), true));
                shape.Points.Add(new BezierKnot(new PointF(100, 200), true));
                shape.Points.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPath.Shapes.Add(shape);
                VectorDataProvider.UpdateLayerFromVectorPath(layer, vectorPath, true);

                psdImage.Save(outputPsd);
            }
        }
{{< /highlight >}}

**PSDNET-1002. 폴더 내보낼 때 벡터 모양이 잘못 내보내짐**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
---
title: Випускні примітки Aspose.PSD для .NET 21.11
type: документація
weight: 20
url: /uk/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить випускні примітки для [Aspose.PSD для .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-767|Виняток при додаванні існуючого текстового шару до групи шарів|Помилка|
|PSDNET-988|IndexOutOfRangeException при оновленні текстового шару TextLayer|Помилка|
|PSDNET-989|Експортовані фігури мають неправильні координати у вихідному файлі|Помилка|
|PSDNET-1002|Неправильний експорт векторної фігури під час експорту у папку|Помилка|

## **Зміни в публічному API**
# **Додано API:**
- Жодних

# **Видалено API:**
- Жодних

## **Приклади використання:**

**PSDNET-767. Виняток при додаванні існуючого текстового шару до групи шарів**

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

**PSDNET-988. IndexOutOfRangeException при оновленні текстового шару TextLayer**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Fonts";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Mom", "Stacy" };
            string[] fonts = new[] { "Caveat", "Gochi Hand", "Lubster", "Satisfy" };

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

**PSDNET-989. Експортовані фігури мають неправильні координати у вихідному файлі**

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
...
{{< /highlight >}}

**PSDNET-1002. Неправильний експорт векторної фігури під час експорту у папку**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
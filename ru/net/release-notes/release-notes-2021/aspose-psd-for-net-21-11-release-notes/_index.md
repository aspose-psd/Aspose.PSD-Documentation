---
title: Aspose.PSD для .NET 21.11 - Примечания к выпуску
type: docs
weight: 20
url: /ru/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-767|Исключение при добавлении существующего текстового слоя в группу слоев|Ошибка|
|PSDNET-988|IndexOutOfRangeException при обновлении текстового слоя TextLayer.UpdateText|Ошибка|
|PSDNET-989|Экспортированные формы имеют неправильные координаты в результирующем файле|Ошибка|
|PSDNET-1002|Некорректный экспорт векторной формы при экспорте в папку|Ошибка|

## **Изменения общедоступного API**
# **Добавлено API:**
- Отсутствует

# **Удалено API:**
- Отсутствует

## **Примеры использования:**

**PSDNET-767. Исключение при добавлении существующего текстового слоя в группу слоев**

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
                var group = image.AddLayerGroup("ТестоваяГруппа", 0, true);
                var layer = image.AddTextLayer("Текст", Rectangle.FromLeftTopRightBottom(-2, 3, 14, 17));
                group.AddLayer(layer);

                image.Save(outputPsd);
            }
{{< /highlight >}}

**PSDNET-988. IndexOutOfRangeException при обновлении текстового слоя TextLayer.UpdateText**

{{< highlight csharp >}}
            string srcFile = "M1TTTT16062021001.psd";
            string fontsFolder = "Шрифты";
            string outputPng = "out_M1TTTT16062021001.png";

            FontSettings.SetFontsFolder(fontsFolder);
            FontSettings.UpdateFonts();

            string[] words = new[] { "Мама", "Стейси" };
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

**PSDNET-989. Экспортированные формы имеют неправильные координаты в результирующем файле**

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


    #region Редактор векторных путей (в этом разделе находятся классы для редактирования векторных путей).

    /// <summary>
    /// Класс, который обеспечивает работу между <see cref="Layer"/> и <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        // Код методов опущен для уменьшения объема ответа
    }

    // Классы BezierKnot, PathShape и VectorPath опущены для уменьшения объема ответа

{{< /highlight >}}

**PSDNET-1002. Некорректный экспорт векторной формы при экспорте в папку**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
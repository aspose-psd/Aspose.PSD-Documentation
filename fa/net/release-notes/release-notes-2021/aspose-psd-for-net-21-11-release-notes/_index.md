---
title: Aspose.PSD for .NET 21.11 - یادداشت‌های انتشار
type: docs
weight: 20
url: /fa/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی یادداشت‌های انتشار برای [Aspose.PSD for .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته**|
| :- | :- | :- |
|PSDNET-767|خطای استثناء در اضافه کردن لایه متن موجود به یک گروه لایه|اشکال|
|PSDNET-988|خطای IndexOutOfRangeException در TextLayer.UpdateText|اشکال|
|PSDNET-989|فرم‌های صادرشده دارای مختصات غلط در پرونده نتیجه می‌باشد|اشکال|
|PSDNET-1002|صادرات نادرست اشکال برداری روی صدور پوشه|اشکال|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
- هیچکدام

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDNET-767. خطای استثناء در اضافه کردن لایه متن موجود به یک گروه لایه**

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

**PSDNET-988. خطای IndexOutOfRangeException در TextLayer.UpdateText**

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

**PSDNET-989. فرم‌های صادرشده دارای مختصات غلط در پرونده نتیجه می‌باشد**

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

**PSDNET-1002. صادرات نادرست اشکال برداری روی صدور پوشه**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
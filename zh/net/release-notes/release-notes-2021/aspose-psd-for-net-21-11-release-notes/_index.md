---
title: Aspose.PSD for .NET 21.11 - 发行说明
type: docs
weight: 20
url: /zh/net/aspose-psd-for-net-21-11-release-notes/
---

{{% alert color="primary" %}} 

此页面包含了 [Aspose.PSD for .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}} 

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-767|将现有文本图层添加到图层组时出现异常|错误|
|PSDNET-988|TextLayer.UpdateText 上的 IndexOutOfRangeException|错误|
|PSDNET-989|导出的形状在结果文件中具有错误的坐标|错误|
|PSDNET-1002|文件夹导出上矢量形状的不正确导出|错误|

## **公共 API 更改**
# **已添加 API:**
- 无

# **已移除 API:**
- 无

## **使用示例:**

**PSDNET-767. 将现有文本图层添加到图层组时出现异常**

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

**PSDNET-988. TextLayer.UpdateText 上的 IndexOutOfRangeException**

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

**PSDNET-989. 导出的形状在结果文件中具有错误的坐标**

{{< highlight csharp >}}
        public void 创建矢量路径示例()
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


    #region 矢量路径编辑器（这里放置了编辑矢量路径的类）。

    /// <summary>
    /// 提供 <see cref="Layer"/> 和 <see cref="VectorPath"/> 之间的工作的类。
    /// </summary>
    public static class VectorDataProvider
    {
        // 各种方法和函数的实现在这里省略。
    }
{{< /highlight >}}

**PSDNET-1002. 文件夹导出上矢量形状的不正确导出**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
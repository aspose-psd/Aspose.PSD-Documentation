---
title: Aspose.PSD cho .NET 21.11 - Ghi chú về phiên bản
type: docs
weight: 20
url: /vi/net/aspose-psd-cho-net-21-11-ghi-chu-ve-phien-ban/
---

{{% alert color="primary" %}} 

Trang này chứa các ghi chú về [Aspose.PSD cho .NET 21.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Khóa**|**Tóm tắt**|**Danh mục**|
| :- | :- | :- |
|PSDNET-767|Ngoại lệ khi thêm lớp văn bản hiện có vào nhóm lớp|Lỗi|
|PSDNET-988|IndexOutOfRangeException trên TextLayer.UpdateText|Lỗi|
|PSDNET-989|Các hình dạng được xuất có tọa độ sai trong tệp kết quả|Lỗi|
|PSDNET-1002|Xuất hình dạng vector không chính xác trong việc xuất thư mục|Lỗi|

## **Thay Đổi API Công Khai**
# **APIs Đã Thêm:**
- Không có

# **APIs Đã Xóa:**
- Không có

## **Ví dụ sử dụng:**

**PSDNET-767. Ngoại lệ khi thêm lớp văn bản hiện có vào nhóm lớp**

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

**PSDNET-988. IndexOutOfRangeException trên TextLayer.UpdateText**

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

**PSDNET-989. Các hình dạng được xuất có tọa độ sai trong tệp kết quả**

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

    #region Trình chỉnh sửa đường vector (Ở đây đặt các lớp để chỉnh sửa các đường vector).

    /// <summary>
    /// Lớp cung cấp công việc giữa <see cref="Layer"/> và <see cref="VectorPath"/>.
    /// </summary>
    public static class VectorDataProvider
    {
        // Đoạn mã của lớp
    }

    // Các lớp khác
{{< /highlight >}}

**PSDNET-1002. Xuất hình dạng vector không chính xác trong việc xuất thư mục**

{{< highlight csharp >}}
            string srcFile = "psdnet1002.psd";
            string outputPng = "output.png";

            using (var image = (PsdImage)Image.Load(srcFile))
            {
                image.Layers[4].Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}
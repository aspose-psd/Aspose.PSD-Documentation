---
title: Aspose.PSD cho .NET 19.11 - Ghi chú phát hành
type: docs
weight: 20
url: /vi/net/aspose-psd-cho-net-19-11-ghi-chu-phat-hanh/
---

{{% alert color="primary" %}}

Trang này chứa các ghi chú phát hành cho [Aspose.PSD cho .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-151|[Hỗ trợ Hiệu ứng Lớp Bóng bên trong](/psd/vi/net/hieu-ung-bong-trong-photoshop/#hieuungbongtrongphotoshop-hieuung-lapbongbentrong)|Tính năng|
|PSDNET-135|[Thực hiện hiển thị Lớp Fill: Mẫu](/psd/vi/net/hieu-ung-lap-fill/#hieuunglapfill-laplaptimhieuthu)|Tính năng|
|PSDNET-187|[Hỗ trợ Hình ảnh Raster trong Tập tin Định dạng AI](/psd/vi/net/thao-tac-voi-cac-dinh-dang-illustrator-adobe/#thaotacvoicacdinhfomatillustrator-adoberastertrongillustrator)|Tính năng|
|PSDNET-225|[Nhận các thuộc tính của định dạng nội dòng của lớp Text](/psd/vi/net/lam-viec-voi-layers-chu/#lamviecvoilayerchu-nhan-thuoctinhsanphamdinhvonoidongcuachuong)|Tính năng|
|PSDNET-214|Xuất PSD không chính xác sang các định dạng khác nếu chứa Hiệu ứng Lớp và Lớp Điều chỉnh|Lỗi|

## **Thay đổi API Công khai**
# **API được thêm vào:**
- T:Aspose.PSD.FileFormats.Ai.AiSection
- M:Aspose.PSD.FileFormats.Ai.AiSection.GetData
- P:Aspose.PSD.FileFormats.Ai.AiImage.Layers
- M:Aspose.PSD.FileFormats.Ai.AiImage.AddLayer(Aspose.PSD.FileFormats.Ai.AiLayerSection)
- T:Aspose.PSD.FileFormats.Ai.AiLayerSection
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.RasterImages
- M:Aspose.PSD.FileFormats.Ai.AiLayerSection.AddRasterImage(Aspose.PSD.FileFormats.Ai.AiRasterImageSection)
- T:Aspose.PSD.FileFormats.Ai.AiRasterImageSection
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Pixels
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.ImageRectangle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetX
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.OffsetY
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Width
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Angle
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.LeftBottomShift
- P:Aspose.PSD.FileFormats.Ai.AiRasterImageSection.Height
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddInnerShadow
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.UseGlobalLight
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Distance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Spread
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.IShadowEffect.Noise
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.GetFonts
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FontType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Script
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Synthetic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.PostScriptName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.FamilyName
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.TextFontInfo.Style
# **API bị xóa:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Ví dụ sử dụng:**
**PSDNET-151. Hỗ trợ Hiệu ứng Lớp Bóng bên trong**

{{< highlight java >}}

            string sourceFile = "mẫu.psd";

            string destName = "mẫu_đầu_ra.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Tải hình ảnh hiện có vào một thể hiện của lớp PsdImage

            using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))

            {

                var layer = image.Layers[image.Layers.Length - 1];

                var shadowEffect = (IShadowEffect)layer.BlendingOptions.Effects[0];

                shadowEffect.Color = Color.Green;

                shadowEffect.Opacity = 128;

                shadowEffect.Distance = 1;

                shadowEffect.UseGlobalLight = false;

                shadowEffect.Size = 2;

                shadowEffect.Angle = 45;

                shadowEffect.Spread = 50;

                shadowEffect.Noise = 5;

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-135. Thực hiện hiển thị Lớp Fill: Mẫu**

{{< highlight java >}}

            string sourceFile = "mẫu.psd";

            string destName = "mẫu_đầu_ra.psd";

            // Tải hình ảnh hiện có vào một thể hiện của lớp PsdImage

            using (var image = (PsdImage)Image.Load(sourceFile))

            {

                foreach (var layer in image.Layers)

                {

                    if (layer is FillLayer)

                    {

                        var fillLayer = (FillLayer)layer;

                        var settings = (IPatternFillSettings)fillLayer.FillSettings;

                        settings.HorizontalOffset = -5;

                        settings.VerticalOffset = 12;

                        settings.Scale = 300;

                        settings.Linked = true;

                        settings.PatternData = new int[]

                                                   {

                                                       Color.Black.ToArgb(), Color.Red.ToArgb(),

                                                       Color.Green.ToArgb(), Color.Blue.ToArgb(),

                                                       Color.White.ToArgb(), Color.AliceBlue.ToArgb(),

                                                       Color.Violet.ToArgb(), Color.Chocolate.ToArgb(),

                                                       Color.IndianRed.ToArgb(), Color.DarkOliveGreen.ToArgb(),

                                                       Color.CadetBlue.ToArgb(), Color.YellowGreen.ToArgb(),

                                                       Color.Black.ToArgb(), Color.Azure.ToArgb(),

                                                       Color.ForestGreen.ToArgb(), Color.Sienna.ToArgb(),

                                                   };

                        settings.PatternHeight = 4;

                        settings.PatternWidth = 4;

                        settings.PatternName = "$$$/Presets/Patterns/ColorfulSquare=Hình vuông đầy màu mới\0";

                        settings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                        break;

                    }

                }

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-187. Hỗ trợ Hình ảnh Raster trong Tập tin Định dạng AI**

{{< highlight java >}}

            const double DefaultTolerance = 1e-6;

void AssertIsTrue(bool condition, string message) {

 if (!condition) {

  throw new FormatException(message);

 }

}

string sourceFile = "mẫu.ai";

using(AiImage image = (AiImage) Image.Load(sourceFile)) {

 AiLayerSection layer = image.Layers[0];

 AssertIsTrue(layer.RasterImages != null, "Thuộc tính RasterImages không nên là null");

 AssertIsTrue(layer.RasterImages.Length == 1, "Thuộc tính RasterImages nên chứa chính xác một mục");

 AiRasterImageSection rasterImage = layer.RasterImages[0];

 AssertIsTrue(rasterImage.Pixels != null, "Thuộc tính rasterImage.Pixels không nên là null");

 AssertIsTrue(rasterImage.Pixels.Length == 100, "Thuộc tính rasterImage.Pixels nên chứa chính xác 100 mục");

 AssertIsTrue((uint) rasterImage.Pixels[99] == 0xFFB21616, "rasterImage.Pixels[99] nên là 0xFFB21616");

 AssertIsTrue((uint) rasterImage.Pixels[19] == 0xFF00FF00, "rasterImage.Pixels[19] nên là 0xFF00FF00");

 AssertIsTrue((uint) rasterImage.Pixels[10] == 0xFF01FD00, "rasterImage.Pixels[10] nên là 0xFF01FD00");

 AssertIsTrue((uint) rasterImage.Pixels[0] == 0xFF0000FF, "rasterImage.Pixels[0] nên là 0xFF0000FF");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Width) < DefaultTolerance, "rasterImage.Width nên là 0.99987");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Height) < DefaultTolerance, "rasterImage.Height nên là 0.99987");

 AssertIsTrue(Math.Abs(387 - rasterImage.OffsetX) < DefaultTolerance, "rasterImage.OffsetX nên là 387");

 AssertIsTrue(Math.Abs(379 - rasterImage.OffsetY) < DefaultTolerance, "rasterImage.OffsetY nên là 379");

 AssertIsTrue(Math.Abs(0 - rasterImage.Angle) < DefaultTolerance, "rasterImage.Angle nên là 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.LeftBottomShift) < DefaultTolerance, "rasterImage.LeftBottomShift nên là 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.X) < DefaultTolerance, "rasterImage.ImageRectangle.X nên là 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.Y) < DefaultTolerance, "rasterImage.ImageRectangle.Y nên là 0");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Width) < DefaultTolerance, "rasterImage.ImageRectangle.Width nên là 10");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Height) < DefaultTolerance, "rasterImage.ImageRectangle.Height nên là 10");

}

{{< /highlight >}}

**PSDNET-225. Nhận các thuộc tính của định dạng nội dòng của lớp Text**

{{< highlight java >}}

     using (var psdImage = (PsdImage)Image.Load("định_dạng_nội_nội.psd"))

            {

                List<ITextPortion> regularText = new List<ITextPortion>();

                List<ITextPortion> boldText = new List<ITextPortion>();

                List<ITextPortion> italicText = new List<ITextPortion>();

                var layers = psdImage.Layers;

                for (int index = 0; index < layers.Length; index++)

                {

                    var layer = layers[index];

                    if (!(layer is TextLayer))

                    {

                        continue;

                    }

                    var textLayer = (TextLayer)layer;

                    // lấy phông chữ chứa trong lớp văn bản

                    var fonts = textLayer.GetFonts();

                    var textPortions = textLayer.TextData.Items;

                    foreach (var textPortion in textPortions)

                    {

                        TextFontInfo font = fonts[textPortion.Style.FontIndex];

                        if (font != null)

                        {

                            switch (font.Style)

                            {

                                case FontStyle.Regular:

                                    regularText.Add(textPortion);

                                    break;

                                case FontStyle.Bold:

                                    boldText.Add(textPortion);

                                    break;

                                case FontStyle.Italic:

                                    italicText.Add(textPortion);

                                    break;

                                default:

                                    throw new ArgumentOutOfRangeException();

                            }

                        }

                    }

                }

            }

{{< /highlight >}}

**PSDNET-214. Xuất PSD không chính xác sang các định dạng khác nếu chứa Hiệu ứng Lớp và Lớp Điều chỉnh**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("đổ đổ bóng.psd", loadOptions))

   {

       image.Save("đầu_ra.png", new PngOptions());

   }

{{< /highlight >}}
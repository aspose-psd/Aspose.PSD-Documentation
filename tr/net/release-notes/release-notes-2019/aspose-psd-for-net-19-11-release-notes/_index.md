---
title: Aspose.PSD for .NET 19.11 - Sürüm Notları
type: docs
weight: 20
url: /tr/net/aspose-psd-for-net-19-11-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-151|[İç Gölge Katman Efekti Desteği](/psd/tr/net/shadow-effects-in-photoshop/#shadoweffectsinphotoshop-innershadoweffect)|Özellik|
|PSDNET-135|[Doldurma Katmanını Render Etme: Desen](/psd/tr/net/support-of-fill-layers/#supportoffilllayers-filllayerswithpatternfill)|Özellik|
|PSDNET-187|[AI Format Dosyalarında Raster Görüntülerinin Desteği](/psd/tr/net/manipulating-adobe-illustrator-formats/#manipulatingadobeillustratorformats-rasterimagesinillustrator)|Özellik|
|PSDNET-225|[TextLayer'ın iç biçimlendirme özelliklerini alın](/psd/tr/net/working-with-text-layers/#workingwithtextlayers-gettextpropertiesfromatextlayer)|Özellik|
|PSDNET-214|Katman Efektleri ve Ayar Katmanları içeren PSD'nin diğer formatlara yanlış dışa aktarımı|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
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
# **Kaldırılan API'lar:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Kullanım örnekleri:**
**PSDNET-151. İç Gölge Katman Efekti Desteği**

{{< highlight java >}}

            string sourceFile = "örnek.psd";

            string destName = "örnek_son.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Mevcut bir resmi PsdImage sınıfı örneğine yükle

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

**PSDNET-135. Doldurma Katmanını Render Etme: Desen**

{{< highlight java >}}

            string sourceFile = "örnek.psd";

            string destName = "örnek_son.psd";

            // Mevcut bir resmi PsdImage sınıfı örneğine yükle

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

                        settings.PatternName = "$$$/Presets/Patterns/ColorfulSquare=Colorful Square New\0";

                        settings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                        break;

                    }

                }

                image.Save(destName, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-187. AI Format Dosyalarında Raster Görüntülerinin Desteği**

{{< highlight java >}}

            const double DefaultTolerance = 1e-6;

void AssertIsTrue(bool condition, string message) {

 if (!condition) {

  throw new FormatException(message);

 }

}

string sourceFile = "örnek.ai";

using(AiImage image = (AiImage) Image.Load(sourceFile)) {

 AiLayerSection layer = image.Layers[0];

 AssertIsTrue(layer.RasterImages != null, "RasterImages özelliği boş olmamalı");

 AssertIsTrue(layer.RasterImages.Length == 1, "RasterImages özelliği tam olarak bir öğe içermelidir");

 AiRasterImageSection rasterImage = layer.RasterImages[0];

 AssertIsTrue(rasterImage.Pixels != null, "rasterImage.Pixels özelliği boş olmamalı");

 AssertIsTrue(rasterImage.Pixels.Length == 100, "rasterImage.Pixels özelliği tam olarak 100 öğe içermelidir");

 AssertIsTrue((uint) rasterImage.Pixels[99] == 0xFFB21616, "rasterImage.Pixels[99] 0xFFB21616 olmalı");

 AssertIsTrue((uint) rasterImage.Pixels[19] == 0xFF00FF00, "rasterImage.Pixels[19] 0xFF00FF00 olmalı");

 AssertIsTrue((uint) rasterImage.Pixels[10] == 0xFF01FD00, "rasterImage.Pixels[10] 0xFF01FD00 olmalı");

 AssertIsTrue((uint) rasterImage.Pixels[0] == 0xFF0000FF, "rasterImage.Pixels[0] 0xFF0000FF olmalı");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Width) < DefaultTolerance, "rasterImage.Width 0.99987 olmalı");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Height) < DefaultTolerance, "rasterImage.Height 0.99987 olmalı");

 AssertIsTrue(Math.Abs(387 - rasterImage.OffsetX) < DefaultTolerance, "rasterImage.OffsetX 387 olmalı");

 AssertIsTrue(Math.Abs(379 - rasterImage.OffsetY) < DefaultTolerance, "rasterImage.OffsetY 379 olmalı");

 AssertIsTrue(Math.Abs(0 - rasterImage.Angle) < DefaultTolerance, "rasterImage.Angle 0 olmalı");

 AssertIsTrue(Math.Abs(0 - rasterImage.LeftBottomShift) < DefaultTolerance, "rasterImage.LeftBottomShift 0 olmalı");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.X) < DefaultTolerance, "rasterImage.ImageRectangle.X 0 olmalı");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.Y) < DefaultTolerance, "rasterImage.ImageRectangle.Y 0 olmalı");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Width) < DefaultTolerance, "rasterImage.ImageRectangle.Width 10 olmalı");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Height) < DefaultTolerance, "rasterImage.ImageRectangle.Height 10 olmalı");

}

{{< /highlight >}}

**PSDNET-225. TextLayer'ın iç biçimlendirme özelliklerini alın**

{{< highlight java >}}

     using (var psdImage = (PsdImage)Image.Load("inline_formatting.psd"))

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

                    // Gets fonts that contains in text layer

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



**PSDNET-214. Katman Efektleri ve Ayar Katmanları içeren PSD'nin diğer formatlara yanlış dışa aktarımı**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("clip_shadow.psd", loadOptions))

   {

       image.Save("output.png", new PngOptions());

   }

{{< /highlight >}}
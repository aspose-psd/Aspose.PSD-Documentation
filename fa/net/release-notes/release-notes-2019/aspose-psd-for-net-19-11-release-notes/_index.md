---
title: دفترچه‌های انتشار Aspose.PSD برای .NET 19.11
type: documents
weight: 20
url: /fa/net/aspose-psd-for-net-19-11-release-notes/
---

{{% alert color="primary" %}} 

این صفحه حاوی دفترچه‌های انتشار [Aspose.PSD برای .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/) می‌باشد.

{{% /alert %}} 

|**کلید**|**خلاصه**|**دسته‌بندی**|
| :- | :- | :- |
|PSDNET-151|[پشتیبانی از افکت لایه سایه داخلی](/psd/fa/net/shadow-effects-in-photoshop/#shadoweffectsinphotoshop-innershadoweffect)|ویژگی|
|PSDNET-135|[پیاده‌سازی رندر لایه پر کننده: الگو](/psd/fa/net/support-of-fill-layers/#supportoffilllayers-filllayerswithpatternfill)|ویژگی|
|PSDNET-187|[پشتیبانی از تصاویر شبکه‌ای در فایل‌های فرمت AI](/psd/fa/net/manipulating-adobe-illustrator-formats/#manipulatingadobeillustratorformats-rasterimagesinillustrator)|ویژگی|
|PSDNET-225|[دریافت ویژگی‌های فرمت‌بندی درونی متن لایه](/psd/fa/net/working-with-text-layers/#workingwithtextlayers-gettextpropertiesfromatextlayer)|ویژگی|
|PSDNET-214|صادرات نادرست PSD به سایر فرمت‌ها در صورت داشتن افکت‌های لایه و لایه‌های تنظیم|اشکال|

## **تغییرات API عمومی**
# **API‌های اضافه شده:**
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
# **API‌های حذف شده:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **مثال‌های استفاده:**
**PSDNET-151. پشتیبانی از افکت لایه سایه داخلی**

{{< highlight java >}}

            string sourceFile = "نمونه.psd";

            string destName = "نمونه_خروجی.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // بارگذاری تصوير موجود به یک نمونه از کلاس PsdImage

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

**PSDNET-135. پیاده‌سازی رندر لایه پر کننده: الگو**

{{< highlight java >}}

            string sourceFile = "نمونه.psd";

            string destName = "نمونه_خروجی.psd";

            // بارگذاری تصویر موجود به یک نمونه از کلاس PsdImage

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

**PSDNET-187. پشتیبانی از تصاویر شبکه‌ای در فایل‌های فرمت AI**

{{< highlight java >}}

            const double DefaultTolerance = 1e-6;

void AssertIsTrue(bool condition, string message) {

 if (!condition) {

  throw new FormatException(message);

 }

}

string sourceFile = "نمونه.ai";

using(AiImage image = (AiImage) Image.Load(sourceFile)) {

 AiLayerSection layer = image.Layers[0];

 AssertIsTrue(layer.RasterImages != null, "خصوصیت RasterImages باید غیرخالی باشد");

 AssertIsTrue(layer.RasterImages.Length == 1, "خصوصیت RasterImages باید دقیقا یک آیتم داشته باشد");

 AiRasterImageSection rasterImage = layer.RasterImages[0];

 AssertIsTrue(rasterImage.Pixels != null, "خصوصیت rasterImage.Pixels باید غیرخالی باشد");

 AssertIsTrue(rasterImage.Pixels.Length == 100, "خصوصیت rasterImage.Pixels باید دقیقا 100 آیتم داشته باشد");

 AssertIsTrue((uint) rasterImage.Pixels[99] == 0xFFB21616, "rasterImage.Pixels[99] باید برابر 0xFFB21616 باشد");

 AssertIsTrue((uint) rasterImage.Pixels[19] == 0xFF00FF00, "rasterImage.Pixels[19] باید برابر 0xFF00FF00 باشد");

 AssertIsTrue((uint) rasterImage.Pixels[10] == 0xFF01FD00, "rasterImage.Pixels[10] باید برابر 0xFF01FD00 باشد");

 AssertIsTrue((uint) rasterImage.Pixels[0] == 0xFF0000FF, "rasterImage.Pixels[0] باید برابر 0xFF0000FF باشد");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Width) < DefaultTolerance, "عرض rasterImage باید 0.99987 باشد");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Height) < DefaultTolerance, "ارتفاع rasterImage باید 0.99987 باشد");

 AssertIsTrue(Math.Abs(387 - rasterImage.OffsetX) < DefaultTolerance, "OffsetX rasterImage باید 387 باشد");

 AssertIsTrue(Math.Abs(379 - rasterImage.OffsetY) < DefaultTolerance, "OffsetY rasterImage باید 379 باشد");

 AssertIsTrue(Math.Abs(0 - rasterImage.Angle) < DefaultTolerance, "زاویه rasterImage باید 0 باشد");

 AssertIsTrue(Math.Abs(0 - rasterImage.LeftBottomShift) < DefaultTolerance, "LeftBottomShift rasterImage باید 0 باشد");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.X) < DefaultTolerance, "ImageRectangle.X rasterImage باید 0 باشد");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.Y) < DefaultTolerance, "ImageRectangle.Y rasterImage باید 0 باشد");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Width) < DefaultTolerance, "ImageRectangle.Width rasterImage باید 10 باشد");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Height) < DefaultTolerance, "ImageRectangle.Height rasterImage باید 10 باشد");

}

{{< /highlight >}}

**PSDNET-225. گرفتن ویژگی‌های فرمت‌بندی درونی متن لایه**

{{< highlight java >}}

     using (var psdImage = (PsdImage)Image.Load("فرمت_بندی_درونی.psd"))

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

                    // گرفتن فونت‌هایی که شامل آنهاست در لایه متن

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



**PSDNET-214. صادرات نادرست PSD به سایر فرمت‌ها در صورت داشتن افکت‌های لایه و لایه‌های تنظیم**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("clip_shadow.psd", loadOptions))

   {

       image.Save("output.png", new PngOptions());

   }

{{< /highlight >}}




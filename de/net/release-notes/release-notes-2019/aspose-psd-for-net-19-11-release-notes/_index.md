---
title: Aspose.PSD für .NET 19.11 - Versionshinweise
type: docs
weight: 20
url: /de/net/aspose-psd-für-net-19-11-versionshinweise/
---

{{% alert color="primary" %}} 

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-151|[Unterstützung des Inner Shadow Layer Effects](/psd/de/net/schatten-effekte-in-photoshop/#schatteneffekteinphotoshop-innererschatteneffekt)|Feature|
|PSDNET-135|[Implementierung der Darstellung von Füllschicht: Muster](/psd/de/net/unterstützung-von-füllschichten/#unterstützungvonfüllschichten-füllungmitmuster)|Feature|
|PSDNET-187|[Unterstützung von Rasterbildern in AI-Formatdateien](/psd/de/net/manipulation-von-adobe-illustrator-formaten/#manipulationvonadobeillustratorformaten-rasterbilderinillustrator)|Feature|
|PSDNET-225|[Abrufen von Eigenschaften der Inline-Formatierung von TextLayer](/psd/de/net/arbeit-mit-textschichten/#arbeitenmittextschichten-texteigenschaftenvoneinetextschichtabrufen)|Feature|
|PSDNET-214|Fehlerhafte Exportierung von PSD in andere Formate, wenn sie Layer Effects und Adjustment Layers enthält|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
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
# **Entfernte APIs:**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Beispiele zur Verwendung:**
**PSDNET-151. Unterstützung des Inner Shadow Layer Effects**

{{< highlight java >}}

            string sourceFile = "beispiel.psd";

            string destName = "beispiel_out.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Lädt ein vorhandenes Bild in eine Instanz der Klasse PsdImage

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

**PSDNET-135. Implementierung der Darstellung von Füllschicht: Muster**

{{< highlight java >}}

            string sourceFile = "beispiel.psd";

            string destName = "beispiel_out.psd";

            // Lädt ein vorhandenes Bild in eine Instanz der Klasse PsdImage

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

**PSDNET-187. Unterstützung von Rasterbildern in AI-Formatdateien**

{{< highlight java >}}

            const double Standard-Toleranz = 1e-6;

void AssertIsTrue(bool Bedingung, string Nachricht) {

 if (!Bedingung) {

  throw new FormatException(Nachricht);

 }

}

string sourceFile = "beispiel.ai";

using(AiImage image = (AiImage) Image.Load(sourceFile)) {

 AiLayerSection layer = image.Layers[0];

 AssertIsTrue(layer.RasterImages != null, "RasterImages-Eigenschaft sollte nicht null sein");

 AssertIsTrue(layer.RasterImages.Length == 1, "RasterImages-Eigenschaft sollte genau ein Element enthalten");

 AiRasterImageSection rasterImage = layer.RasterImages[0];

 AssertIsTrue(rasterImage.Pixels != null, "rasterImage.Pixels-Eigenschaft sollte nicht null sein");

 AssertIsTrue(rasterImage.Pixels.Length == 100, "rasterImage.Pixels-Eigenschaft sollte genau 100 Elemente enthalten");

 AssertIsTrue((uint) rasterImage.Pixels[99] == 0xFFB21616, "rasterImage.Pixels[99] sollte 0xFFB21616 sein");

 AssertIsTrue((uint) rasterImage.Pixels[19] == 0xFF00FF00, "rasterImage.Pixels[19] sollte 0xFF00FF00 sein");

 AssertIsTrue((uint) rasterImage.Pixels[10] == 0xFF01FD00, "rasterImage.Pixels[10] sollte 0xFF01FD00 sein");

 AssertIsTrue((uint) rasterImage.Pixels[0] == 0xFF0000FF, "rasterImage.Pixels[0] sollte 0xFF0000FF sein");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Width) < Standard-Toleranz, "rasterImage.Width sollte 0.99987 sein");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Height) < Standard-Toleranz, "rasterImage.Height sollte 0.99987 sein");

 AssertIsTrue(Math.Abs(387 - rasterImage.OffsetX) < Standard-Toleranz, "rasterImage.OffsetX sollte 387 sein");

 AssertIsTrue(Math.Abs(379 - rasterImage.OffsetY) < Standard-Toleranz, "rasterImage.OffsetY sollte 379 sein");

 AssertIsTrue(Math.Abs(0 - rasterImage.Angle) < Standard-Toleranz, "rasterImage.Angle sollte 0 sein");

 AssertIsTrue(Math.Abs(0 - rasterImage.LeftBottomShift) < Standard-Toleranz, "rasterImage.LeftBottomShift sollte 0 sein");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.X) < Standard-Toleranz, "rasterImage.ImageRectangle.X sollte 0 sein");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.Y) < Standard-Toleranz, "rasterImage.ImageRectangle.Y sollte 0 sein");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Width) < Standard-Toleranz, "rasterImage.ImageRectangle.Width sollte 10 sein");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Height) < Standard-Toleranz, "rasterImage.ImageRectangle.Height sollte 10 sein");

}

{{< /highlight >}}

**PSDNET-225. Abrufen von Eigenschaften der Inline-Formatierung von TextLayer**

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

                    // erhält Schriftarten, die in der Textebene enthalten sind

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

**PSDNET-214. Fehlerhafte Exportierung von PSD in andere Formate, wenn sie Layer Effects und Adjustment Layers enthält**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("clip_shadow.psd", loadOptions))

   {

       image.Save("output.png", new PngOptions());

   }

{{< /highlight >}}
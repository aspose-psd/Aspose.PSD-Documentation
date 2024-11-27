---
title: Notes de version Aspose.PSD pour .NET 19.11
type: docs
weight: 20
url: /fr/net/aspose-psd-pour-net-19-11-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 19.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-151|[Prise en charge de l'effet de calque d'ombre interne](/psd/fr/net/effets-d-ombre-dans-photoshop/#effet-d-ombre-interne-dans-photoshop)|Fonctionnalité|
|PSDNET-135|[Mise en œuvre du rendu de calque de remplissage : Modèle](/psd/fr/net/support-des-couches-de-remplissage/#support-des-couches-de-remplissage-couches-de-remplissage-avec-remplissage-modele)|Fonctionnalité|
|PSDNET-187|[Prise en charge des images matricielles dans les fichiers au format AI](/psd/fr/net/manipulation-des-formats-adobe-illustrator/#manipulation-de-formats-adobe-illustrator-images-matricielles-dans-illustrator)|Fonctionnalité|
|PSDNET-225|[Obtenir les propriétés de la mise en forme en ligne de la couche de texte](/psd/fr/net/travailler-avec-les-couches-de-texte/#travailler-avec-les-couches-de-texte-obtenir-les-proprietes-du-texte-a-partir-d-une-couche-de-texte)|Fonctionnalité|
|PSDNET-214|Export incorrect du PSD vers d'autres formats s'il contient des effets de calque et des calques d'ajustement|Bogue|

## **Changements d'API publics**
# **APIs ajoutées :**

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
# **APIs supprimées :**
- M:Aspose.PSD.FileFormats.Ai.AiFinalizeSection.GetData
- M:Aspose.PSD.FileFormats.Ai.AiSetupSection.GetData

## **Exemples d'utilisation :**
**PSDNET-151. Prise en charge de l'effet de calque d'ombre interne**

{{< highlight java >}}

            string sourceFile = "sample.psd";

            string destName = "sample_out.psd";

            var loadOptions = new PsdLoadOptions()

            {

                LoadEffectsResource = true

            };

            // Chargez une image existante dans une instance de la classe PsdImage

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

**PSDNET-135. Mise en œuvre du rendu de calque de remplissage : Modèle**

{{< highlight java >}}

            string sourceFile = "sample.psd";

            string destName = "sample_out.psd";

            // Chargez une image existante dans une instance de la classe PsdImage

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

**PSDNET-187. Prise en charge des images matricielles dans les fichiers au format AI**

{{< highlight java >}}

            const double DefaultTolerance = 1e-6;

void AssertIsTrue(bool condition, string message) {

 if (!condition) {

  throw new FormatException(message);

 }

}

string sourceFile = "sample.ai";

using(AiImage image = (AiImage) Image.Load(sourceFile)) {

 AiLayerSection layer = image.Layers[0];

 AssertIsTrue(layer.RasterImages != null, "La propriété RasterImages ne doit pas être nulle");

 AssertIsTrue(layer.RasterImages.Length == 1, "La propriété RasterImages doit contenir exactement un élément");

 AiRasterImageSection rasterImage = layer.RasterImages[0];

 AssertIsTrue(rasterImage.Pixels != null, "La propriété Pixels de rasterImage ne doit pas être nulle");

 AssertIsTrue(rasterImage.Pixels.Length == 100, "La propriété Pixels de rasterImage doit contenir exactement 100 éléments");

 AssertIsTrue((uint) rasterImage.Pixels[99] == 0xFFB21616, "rasterImage.Pixels[99] doit être 0xFFB21616");

 AssertIsTrue((uint) rasterImage.Pixels[19] == 0xFF00FF00, "rasterImage.Pixels[19] doit être 0xFF00FF00");

 AssertIsTrue((uint) rasterImage.Pixels[10] == 0xFF01FD00, "rasterImage.Pixels[10] doit être 0xFF01FD00");

 AssertIsTrue((uint) rasterImage.Pixels[0] == 0xFF0000FF, "rasterImage.Pixels[0] doit être 0xFF0000FF");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Width) < DefaultTolerance, "La largeur de rasterImage doit être 0,99987");

 AssertIsTrue(Math.Abs(0.999875 - rasterImage.Height) < DefaultTolerance, "La hauteur de rasterImage doit être 0,99987");

 AssertIsTrue(Math.Abs(387 - rasterImage.OffsetX) < DefaultTolerance, "Le décalage X de rasterImage doit être 387");

 AssertIsTrue(Math.Abs(379 - rasterImage.OffsetY) < DefaultTolerance, "Le décalage Y de rasterImage doit être 379");

 AssertIsTrue(Math.Abs(0 - rasterImage.Angle) < DefaultTolerance, "L'angle de rasterImage doit être 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.LeftBottomShift) < DefaultTolerance, "Le décalage inférieur gauche de rasterImage doit être 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.X) < DefaultTolerance, "La coordonnée X de l'image de rasterImage doit être 0");

 AssertIsTrue(Math.Abs(0 - rasterImage.ImageRectangle.Y) < DefaultTolerance, "La coordonnée Y de l'image de rasterImage doit être 0");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Width) < DefaultTolerance, "La largeur de l'image de rasterImage doit être 10");

 AssertIsTrue(Math.Abs(10 - rasterImage.ImageRectangle.Height) < DefaultTolerance, "La hauteur de l'image de rasterImage doit être 10");

}

{{< /highlight >}}

**PSDNET-225. Obtenir les propriétés de la mise en forme en ligne de la couche de texte**

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

                    // Obtenir les polices contenues dans la couche de texte

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



**PSDNET-214. Export incorrect du PSD vers d'autres formats s'il contient des effets de calque et des calques d'ajustement**

{{< highlight java >}}

     var loadOptions = new PsdLoadOptions();

   loadOptions.LoadEffectsResource = true;

   using (var image = (PsdImage)Image.Load("clip_shadow.psd", loadOptions))

   {

       image.Save("output.png", new PngOptions());

   }

{{< /highlight >}}
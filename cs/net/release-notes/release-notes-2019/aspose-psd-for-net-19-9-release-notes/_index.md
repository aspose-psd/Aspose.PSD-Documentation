---
title: Aspose.PSD pro .NET 19.9 - Poznámky k vydání
type: docs
weight: 40
url: /cs/net/aspose-psd-pro-net-19-9-poznamky-k-vydani/
---

{{% alert color="primary" %}} 

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klíč**|**Shrnutí**|**Kategorie**|
| :- | :- | :- |
|PSDNET-160|Nesprávně extrahovaný název vrstvy|Funkce|
|PSDNET-175|Získávání vlastností textu z jiné části textu uvnitř vrstvy PSD TextLayer|Funkce|
|PSDNET-190|Podpora pro přidání skupiny vrstev|Funkce|
|PSDNET-192|Podpora vlastnosti měřítka pro vrstvu s přechodovým plněním Gradient Fill Layer|Funkce|
|PSDNET-162|Upravení jasu|Vylepšení|
|PSDNET-174|IndexOutOfRangeException při ukládání obrázku PSD jako JPEG|Chyba|
|PSDNET-180|Aktualizace textové vrstvy vrstvy textu vyvolá výjimku|Chyba|
|PSDNET-182|Ukládání obrázku PSD po operaci RotateFlip produkuje poškozený soubor, který nelze otevřít|Chyba|

## **Změny ve veřejném API**
# **Nově přidaná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale
# **Odstraněná API:**
- Žádné

## **Příklady použití:**
**PSDNET-160. Nesprávně extrahovaný název vrstvy**

Pro správné zobrazení názvu vrstvy použijte vlastnost **DisplayName**. Nyní je přidán setter pro tuto vlastnost a lze ji upravit. Když Photoshop ukládá název vrstvy pomocí vlastnosti Name, korejské znaky jsou uloženy jako bajt 63'?' v ASCII.  Použijte vlastnost **DisplayName**, protože vlastnost Name nepodporuje korejské znaky.

{{< highlight java >}}

             // provedení změn v názvech vrstev a jejich uložení

            using (var image = (PsdImage)Image.Load("vrstvy_s_nazvy.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // nastavit novou hodnotu do vlastnosti DisplayName

                    layer.DisplayName += "_changed";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Získání vlastností textu z jiné části textu uvnitř vrstvy PSD TextLayer**

{{< highlight java >}}

            const double Tolerance = 0.0001;

            var filePath = "ThreeColorsParagraphs.psd";

            var outputPath = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var layer = im.Layers[i] as TextLayer;

                    if (layer != null)

                    {

                        var portions = layer.TextData.Items;

                        if (portions.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Kontrola textu každé části

                        if (

                            portions[0].Text != "Old " ||

                            portions[1].Text != "color" ||

                            portions[2].Text != " text\r" ||

                            portions[3].Text != "Second paragraph\r")

                        {

                            throw new Exception();

                        }

                        // Kontrola dat odstavců

                        // Odstavce mají různou justifikaci

                        if (

                            portions[0].Paragraph.Justification != 0 ||

                            portions[1].Paragraph.Justification != 0 ||

                            portions[2].Paragraph.Justification != 0 ||

                            portions[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Všechny ostatní vlastnosti prvního a druhého odstavce jsou stejné

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var paragraph = portions[j].Paragraph;

                            if (Math.Abs(paragraph.AutoLeading - 1.2) > Tolerance ||

                                paragraph.AutoHyphenate != false ||

                                paragraph.Burasagari != false ||

                                paragraph.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraph.StartIndent) > Tolerance ||

                                Math.Abs(paragraph.EndIndent) > Tolerance ||

                                paragraph.EveryLineComposer != false ||

                                Math.Abs(paragraph.FirstLineIndent) > Tolerance ||

                                paragraph.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraph.GlyphSpacing[0] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[1] - 1) > Tolerance ||

                                Math.Abs(paragraph.GlyphSpacing[2] - 1) > Tolerance ||

                                paragraph.Hanging != false ||

                                paragraph.HyphenatedWordSize != 6 ||

                                paragraph.KinsokuOrder != 0 ||

                                paragraph.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraph.LetterSpacing[0]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[1]) > Tolerance ||

                                Math.Abs(paragraph.LetterSpacing[2]) > Tolerance ||

                                paragraph.LeadingType != LeadingMode.Auto ||

                                paragraph.PreHyphen != 2 ||

                                paragraph.PostHyphen != 2 ||

                                Math.Abs(paragraph.SpaceBefore) > Tolerance ||

                                Math.Abs(paragraph.SpaceAfter) > Tolerance ||

                                paragraph.WordSpacing.Length != 3 ||

                                Math.Abs(paragraph.WordSpacing[0] - 0.8) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[1] - 1.0) > Tolerance ||

                                Math.Abs(paragraph.WordSpacing[2] - 1.33) > Tolerance ||

                                Math.Abs(paragraph.Zone - 36.0) > Tolerance)

                            {

                                throw new Exception();

                            }

                        }

                        // Kontrola stylu textu

                        // Styly mají různé barvy a velikost písma

                        if (Math.Abs(portions[0].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[1].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[2].Style.FontSize - 12) > Tolerance ||

                            Math.Abs(portions[3].Style.FontSize - 10) > Tolerance)

                        {

                            throw new Exception();

                        }

                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < portions.Length; j++)

                        {

                            var style = portions[j].Style;

                            if (style.AutoLeading != false ||

                                style.HindiNumbers != false ||

                                style.Kerning != 0 ||

                                style.Leading != 0 ||

                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                style.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Příklad úpravy textu

                        portions[0].Text = "Hello ";

                        portions[1].Text = "World";

                        // Příklad odebrání částí textu

                        layer.TextData.RemovePortion(3);

                        layer.TextData.RemovePortion(2);

                        // Příklad přidání nové části textu

                        var createdPortion = layer.TextData.ProducePortion();

                        createdPortion.Text = "!!!\r";

                        layer.TextData.AddPortion(createdPortion);

                        portions = layer.TextData.Items;

                        // Příklad úpravy odstavce a stylu pro části textu

                        // Nastavení správné justifikace

                        portions[0].Paragraph.Justification = 1;

                        portions[1].Paragraph.Justification = 1;

                        portions[2].Paragraph.Justification = 1;

                        // Různé barvy pro každý styl. Budou změněny, ale vykreslování není plně podporováno

                        portions[0].Style.FillColor = Color.Aquamarine;

                        portions[1].Style.FillColor = Color.Violet;

                        portions[2].Style.FillColor = Color.LightBlue;

                        // Různé písma. Budou změněny, ale vykreslování není plně podporováno

                        portions[0].Style.FontSize = 6;

                        portions[1].Style.FontSize = 8;

                        portions[2].Style.FontSize = 10;

                        layer.TextData.UpdateLayerData();

                        im.Save(outputPath, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Podpora pro přidání skupiny vrstev**

{{< highlight java >}}

             // -Skupina 1

            // --Vrstva 1

            // --Skupina 2

            // ---Vrstva 2

            // ---Vrstva 3

            // --Vrstva 4

            string dataDir = "psdnet190_test.psd";

            var createOptions = new PsdOptions();

            createOptions.Source = new FileCreateSource(dataDir, false);

            createOptions.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(createOptions, 500, 500))

            {

                LayerGroup group1 = psdImage.AddLayerGroup("Skupina 1", 0, true);

                Layer layer1 = new Layer(psdImage);

                layer1.Name = "Vrstva 1";

                group1.AddLayer(layer1);

                LayerGroup group2 = group1.AddLayerGroup("Skupina 2", 1);

                Layer layer2 = new Layer(psdImage);

                layer2.Name = "Vrstva 2";

                group2.AddLayer(layer2);

                Layer layer3 = new Layer(psdImage);

                layer3.Name = "Vrstva 3";

                group2.AddLayer(layer3);

                Layer layer4 = new Layer(psdImage);

                layer4.Name = "Vrstva 4";

                group1.AddLayer(layer4);

                psdImage.Save();

            }

{{< /highlight >}}

**PSDNET-192. Podpora vlastnosti měřítka pro vrstvu Gradient Fill Layer**

{{< highlight java >}}

            using (var image = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // získání vrstvy plnění

                FillLayer fillLayer = null;

                foreach (var layer in image.Layers)

                {

                    fillLayer = layer as FillLayer;

                    if (fillLayer != null)

                    {

                        break;

                    }

                }

                var settings = fillLayer.FillSettings as IGradientFillSettings;

                // aktualizace hodnoty měřítka

                settings.Scale = 200;

                fillLayer.Update(); // Aktualizuje data pixelů

                image.Save("scaledImage.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}



**PSDNET-174. IndexOutOfRangeException při ukládání obrázku PSD jako JPEG**

{{< highlight java >}}

         using (var image = Aspose.PSD.Image.Load("SamplePSD.psd"))

        {

            image.Save("sampleJPG.jpg", new JpegOptions());

        }

{{< /highlight >}}

**PSDNET-180. Aktualizace textové vrstvy textu vyvolá výjimku**

{{< highlight java >}}

           //
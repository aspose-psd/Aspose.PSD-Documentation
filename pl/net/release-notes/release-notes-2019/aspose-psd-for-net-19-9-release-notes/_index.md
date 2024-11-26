---
title: Aspose.PSD dla .NET 19.9 - Notatki wydania
type: docs
weight: 40
url: /pl/net/aspose-psd-dla-net-19-9-notatki-wydania/
---

{{% alert color="primary" %}} 

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-160|Zła nazwa warstwy wyodrębniona|Funkcja|
|PSDNET-175|Pobieranie właściwości tekstu z innego fragmentu tekstu w warstwie tekstowej PSD|Funkcja|
|PSDNET-190|Wsparcie dla dodawania grupy warstw|Funkcja|
|PSDNET-192|Wsparcie właściwości skalowania warstwy gradientu wypełnienia|Funkcja|
|PSDNET-162|Dostosowanie jasności|Udoskonalenie|
|PSDNET-174|IndexOutOfRangeException podczas zapisywania obrazu PSD jako JPEG|Błąd|
|PSDNET-180|Aktualizacja tekstu warstwy tekstowej powoduje wyjątek|Błąd|
|PSDNET-182|Zapisywanie obrazu PSD po operacji RotateFlip powoduje uszkodzony plik, który nie może być otwarty|Błąd|

## **Zmiany w interfejsie API publicznego**
# **Dodane API:**
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
# **Usunięte API:**
- Brak

## **Przykłady użycia:**
**PSDNET-160. Zła nazwa warstwy wyodrębniona**

Aby wyświetlić nazwę warstwy poprawnie, użyj właściwości **DisplayName**. Setter jest teraz dodany dla tej właściwości i można ją modyfikować. Kiedy Photoshop zapisuje nazwę warstwy, używając właściwości Name, koreańskie znaki są przechowywane jako bajt 63'?' w ASCII. Użyj właściwości **DisplayName**, ponieważ właściwość Name nie obsługuje koreańskich znaków.

{{< highlight java >}}

             // dokonaj zmian w nazwach warstw i zapisz je

            using (var image = (PsdImage)Image.Load("layers with names.psd"))

            {

                for (int i = 0; i < image.Layers.Length; i++)

                {

                    var layer = image.Layers[i];

                    // ustaw nową wartość do właściwości DisplayName

                    layer.DisplayName += "_zmienione";

                }

                image.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Pobieranie właściwości tekstu z innego fragmentu tekstu w warstwie tekstowej PSD**

{{< highlight java >}}

            const double Tolerancja = 0.0001;

            var ścieżkaPliku = "ThreeColorsParagraphs.psd";

            var ścieżkaWyjściowa = "ThreeColorsParagraph_out.psd";

            using (var im = (PsdImage)Image.Load(ścieżkaPliku))

            {

                for (int i = 0; i < im.Layers.Length; i++)

                {

                    var warstwa = im.Layers[i] as TextLayer;

                    if (warstwa != null)

                    {

                        var fragmenty = warstwa.TextData.Items;

                        if (fragmenty.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Sprawdzenie tekstu każdego fragmentu

                        if (fragmenty[0].Text != "Stary " ||

                            fragmenty[1].Text != "kolor" ||

                            fragmenty[2].Text != " tekst\r" ||

                            fragmenty[3].Text != "Drugi akapit\r")

                        {

                            throw new Exception();

                        }

                        // Sprawdzenie danych akapitów

                        // Akapity mają różne justyfikacje

                        if (

                            fragmenty[0].Paragraph.Justification != 0 ||

                            fragmenty[1].Paragraph.Justification != 0 ||

                            fragmenty[2].Paragraph.Justification != 0 ||

                            fragmenty[3].Paragraph.Justification != 2)

                        {

                            throw new Exception();

                        }

                        // Wszystkie inne właściwości pierwszego i drugiego akapitu są równe

                        for (int j = 0; j < fragmenty.Length; j++)

                        {

                            var akapit = fragmenty[j].Paragraph;

                            if (Math.Abs(akapit.AutoLeading - 1.2) > Tolerancja ||

                                akapit.AutoHyphenate != false ||

                                akapit.Burasagari != false ||

                                akapit.ConsecutiveHyphens != 8 ||

                                Math.Abs(akapit.StartIndent) > Tolerancja ||

                                Math.Abs(akapit.EndIndent) > Tolerancja ||

                                akapit.EveryLineComposer != false ||

                                Math.Abs(akapit.FirstLineIndent) > Tolerancja ||

                                akapit.GlyphSpacing.Length != 3 ||

                                Math.Abs(akapit.GlyphSpacing[0] - 1) > Tolerancja ||

                                Math.Abs(akapit.GlyphSpacing[1] - 1) > Tolerancja ||

                                Math.Abs(akapit.GlyphSpacing[2] - 1) > Tolerancja ||

                                akapit.Hanging != false ||

                                akapit.HyphenatedWordSize != 6 ||

                                akapit.KinsokuOrder != 0 ||

                                akapit.LetterSpacing.Length != 3 ||

                                Math.Abs(akapit.LetterSpacing[0]) > Tolerancja ||

                                Math.Abs(akapit.LetterSpacing[1]) > Tolerancja ||

                                Math.Abs(akapit.LetterSpacing[2]) > Tolerancja ||

                                akapit.LeadingType != LeadingMode.Auto ||

                                akapit.PreHyphen != 2 ||

                                akapit.PostHyphen != 2 ||

                                Math.Abs(akapit.SpaceBefore) > Tolerancja ||

                                Math.Abs(akapit.SpaceAfter) > Tolerancja ||

                                akapit.WordSpacing.Length != 3 ||

                                Math.Abs(akapit.WordSpacing[0] - 0.8) > Tolerancja ||

                                Math.Abs(akapit.WordSpacing[1] - 1.0) > Tolerancja ||

                                Math.Abs(akapit.WordSpacing[2] - 1.33) > Tolerancja ||

                                Math.Abs(akapit.Zone - 36.0) > Tolerancja)

                            {

                                throw new Exception();

                            }

                        }

                        // Sprawdzenie danych stylu

                        // Style mają różne kolory i rozmiar czcionki

                        if (Math.Abs(fragmenty[0].Style.FontSize - 12) > Tolerancja ||

                            Math.Abs(fragmenty[1].Style.FontSize - 12) > Tolerancja ||

                            Math.Abs(fragmenty[2].Style.FontSize - 12) > Tolerancja ||

                            Math.Abs(fragmenty[3].Style.FontSize - 10) > Tolerancja)

                        {

                            throw new Exception();

                        }

                        if (fragmenty[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||

                            fragmenty[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||

                            fragmenty[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||

                            fragmenty[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < fragmenty.Length; j++)

                        {

                            var styl = fragmenty[j].Style;

                            if (styl.AutoLeading != false ||

                                styl.HindiNumbers != false ||

                                styl.Kerning != 0 ||

                                styl.Leading != 0 ||

                                styl.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||

                                styl.Tracking != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Przykład edycji tekstu

                        fragmenty[0].Text = "Witaj ";

                        fragmenty[1].Text = "Świecie";

                        // Przykład usuwania fragmentów tekstu

                        warstwa.TextData.RemovePortion(3);

                        warstwa.TextData.RemovePortion(2);

                        // Przykład dodawania nowego fragmentu tekstu

                        var nowyFragment = warstwa.TextData.ProducePortion();

                        nowyFragment.Text = "!!!\r";

                        warstwa.TextData.AddPortion(nowyFragment);

                        fragmenty = warstwa.TextData.Items;

                        // Przykład edycji akapitu i stylu dla fragmentów

                        // Ustawienie właściwej justyfikacji

                        fragmenty[0].Paragraph.Justification = 1;

                        fragmenty[1].Paragraph.Justification = 1;

                        fragmenty[2].Paragraph.Justification = 1;

                        // Różne kolory dla każdego stylu. Zostaną one zmienione, ale renderowanie nie jest w pełni obsługiwane

                        fragmenty[0].Style.FillColor = Color.Aquamarine;

                        fragmenty[1].Style.FillColor = Color.Violet;

                        fragmenty[2].Style.FillColor = Color.LightBlue;

                        // Różna czcionka. Zostanie zmieniona, ale renderowanie nie jest w pełni obsługiwane

                        fragmenty[0].Style.FontSize = 6;

                        fragmenty[1].Style.FontSize = 8;

                        fragmenty[2].Style.FontSize = 10;

                        warstwa.TextData.UpdateLayerData();

                        im.Save(ścieżkaWyjściowa, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Wsparcie dla dodawania grupy warstw**

{{< highlight java >}}

             // -Grupa 1

            // --Warstwa 1

            // --Grupa 2

            // ---Warstwa 2

            // ---Warstwa 3

            // --Warstwa 4

            string katalogDanych = "psdnet190_test.psd";

            var opcjeTworzenia = new PsdOptions();

            opcjeTworzenia.Source = new FileCreateSource(katalogDanych, false);

            opcjeTworzenia.Palette = new PsdColorPalette(new Color[] { Color.Green });

            using (var psdImage = (PsdImage)Image.Create(opcjeTworzenia, 500, 500))

            {

                LayerGroup grupa1 = psdImage.AddLayerGroup("Grupa 1", 0, true);

                Layer warstwa1 = new Layer(psdImage);

                warstwa1.Name = "Warstwa 1";

                grupa1.AddLayer(warstwa1);

                LayerGroup grupa2 = grupa1.AddLayerGroup("Grupa 2", 1);

                Layer warstwa2 = new Layer(psdImage);

                warstwa2.Name = "Warstwa 2";

                grupa2.AddLayer(warstwa2);

                Layer warstwa3 = new Layer(psdImage);

                warstwa3.Name = "Warstwa 3";

                grupa2.AddLayer(warstwa3);

                Layer warstwa4 = new Layer(psdImage);

                warstwa4.Name = "Warstwa 4";

                grupa1.AddLayer(warstwa4);

                psdImage.Save();

            }

{{< /highlight >}}

**PSDNET-192. Wsparcie właściwości skalowania warstwy gradientu wypełnienia**

{{< highlight java >}}

            using (var image = (PsdImage)Image.Load("FillLayerGradient.psd"))

            {

                // uzyskanie warstwy wypełnienia

                FillLayer warstwaWypełnienia = null;

                foreach (var warstwa in image.Layers)

                {

                    warstwaWypełnienia = warstwa as FillLayer;

                    if (warstwaWypełnienia != null)

                    {

                        break;

                    }

                }

               
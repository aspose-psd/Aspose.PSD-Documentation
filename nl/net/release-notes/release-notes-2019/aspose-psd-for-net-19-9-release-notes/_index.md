---
title: Aspose.PSD voor .NET 19.9 - Release-opmerkingen
type: docs
weight: 40
url: /nl/net/aspose-psd-voor-net-19-9-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-160|Verkeerde laagnaam geëxtraheerd|Functie|
|PSDNET-175|Eigenschappen van tekst verkrijgen uit een ander deel van tekst binnen PSD TextLayer|Functie|
|PSDNET-190|Ondersteuning voor Toevoegen laaggroep|Functie|
|PSDNET-192|Ondersteuning van Schaal Eigenschap voor Verloopvullingslaag|Functie|
|PSDNET-162|Helderheid aanpassen|Verbetering|
|PSDNET-174|IndexOutOfRangeException bij opslaan PSD-afbeelding als JPEG|Fout|
|PSDNET-180|Het bijwerken van tekstlaagtekst genereert een uitzondering|Fout|
|PSDNET-182|Het opslaan van PSD-afbeelding na RotateFlip-operatie produceert een beschadigd bestand dat niet kan worden geopend|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
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
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-160. Verkeerde laagnaam geëxtraheerd**

Om de laagnaam correct weer te geven, gebruik de **DisplayName** eigenschap. Er is nu een setter toegevoegd voor deze eigenschap en de eigenschap kan worden aangepast. Wanneer Photoshop de laagnaam opslaat met behulp van de Naam eigenschap, worden de Koreaanse karakters opgeslagen als byte 63'?' in ASCII. Gebruik de **DisplayName** eigenschap omdat de Naam eigenschap geen Koreaanse karakters ondersteunt.

{{< highlight java >}}

             // wijzigingen aanbrengen in laagnamen en opslaan

            using (var afbeelding = (PsdImage)Image.Load("lagen met namen.psd"))

            {

                for (int i = 0; i < afbeelding.Lagen.Length; i++)

                {

                    var laag = afbeelding.Lagen[i];

                    // nieuwe waarde instellen in DisplayName eigenschap

                    laag.DisplayName += "_gewijzigd";

                }

                afbeelding.Save("output.psd");

            }

{{< /highlight >}}

**PSDNET-175. Eigenschappen van tekst verkrijgen uit een ander deel van tekst binnen PSD TextLayer**

{{< highlight java >}}

            const double Tolerantie = 0.0001;

            var bestandsnaam = "DrieKleurParagrafen.psd";

            var uitvoerpad = "DrieKleurParagrafen_uit.psd";

            using (var im = (PsdImage)Image.Load(bestandsnaam))

            {

                for (int i = 0; i < im.Lagen.Length; i++)

                {

                    var laag = im.Lagen[i] as TextLayer;

                    if (laag != null)

                    {

                        var gedeelten = laag.TextData.Items;

                        if (gedeelten.Length != 4)

                        {

                            throw new Exception();

                        }

                        // Tekst van elk gedeelte controleren

                        if (gedeelten[0].Text != "Oud " ||

                            gedeelten[1].Text != "kleur" ||

                            gedeelten[2].Text != " tekst\r" ||

                            gedeelten[3].Text != "Tweede alinea\r")

                        {

                            throw new Exception();

                        }

                        // Paragraafgegevens controleren

                        // Paragrafen hebben verschillende rechtvaardiging

                        if (

                            gedeelten[0].Paragraaf.Rechtvaardiging != 0 ||

                            gedeelten[1].Paragraaf.Rechtvaardiging != 0 ||

                            gedeelten[2].Paragraaf.Rechtvaardiging != 0 ||

                            gedeelten[3].Paragraaf.Rechtvaardiging != 2)

                        {

                            throw new Exception();

                        }

                        // Alle andere eigenschappen van de eerste en tweede alinea zijn gelijk

                        for (int j = 0; j < gedeelten.Length; j++)

                        {

                            var paragraaf = gedeelten[j].Paragraaf;

                            if (Math.Abs(paragraaf.AutoLeading - 1.2) > Tolerantie ||

                                paragraaf.AutoHyphenate != false ||

                                paragraaf.Burasagari != false ||

                                paragraaf.ConsecutiveHyphens != 8 ||

                                Math.Abs(paragraaf.StartIndent) > Tolerantie ||

                                Math.Abs(paragraaf.EndIndent) > Tolerantie ||

                                paragraaf.EveryLineComposer != false ||

                                Math.Abs(paragraaf.FirstLineIndent) > Tolerantie ||

                                paragraaf.GlyphSpacing.Length != 3 ||

                                Math.Abs(paragraaf.GlyphSpacing[0] - 1) > Tolerantie ||

                                Math.Abs(paragraaf.GlyphSpacing[1] - 1) > Tolerantie ||

                                Math.Abs(paragraaf.GlyphSpacing[2] - 1) > Tolerantie ||

                                paragraaf.Hanging != false ||

                                paragraaf.HyphenatedWordSize != 6 ||

                                paragraaf.KinsokuOrder != 0 ||

                                paragraaf.LetterSpacing.Length != 3 ||

                                Math.Abs(paragraaf.LetterSpacing[0]) > Tolerantie ||

                                Math.Abs(paragraaf.LetterSpacing[1]) > Tolerantie ||

                                Math.Abs(paragraaf.LetterSpacing[2]) > Tolerantie ||

                                paragraaf.LeadingType != LeadingMode.Auto ||

                                paragraaf.PreHyphen != 2 ||

                                paragraaf.PostHyphen != 2 ||

                                Math.Abs(paragraaf.SpaceBefore) > Tolerantie ||

                                Math.Abs(paragraaf.SpaceAfter) > Tolerantie ||

                                paragraaf.WordSpacing.Length != 3 ||

                                Math.Abs(paragraaf.WordSpacing[0] - 0.8) > Tolerantie ||

                                Math.Abs(paragraaf.WordSpacing[1] - 1.0) > Tolerantie ||

                                Math.Abs(paragraaf.WordSpacing[2] - 1.33) > Tolerantie ||

                                Math.Abs(paragraaf.Zone - 36.0) > Tolerantie)

                            {

                                throw new Exception();

                            }

                        }

                        // Stijlgegevens controleren

                        // Stijlen hebben verschillende kleuren en lettergrootte

                        if (Math.Abs(gedeelten[0].Stijl.FontGrootte - 12) > Tolerantie ||

                            Math.Abs(gedeelten[1].Stijl.FontGrootte - 12) > Tolerantie ||

                            Math.Abs(gedeelten[2].Stijl.FontGrootte - 12) > Tolerantie ||

                            Math.Abs(gedeelten[3].Stijl.FontGrootte - 10) > Tolerantie)

                        {

                            throw new Exception();

                        }

                        if (gedeelten[0].Stijl.VulKleur != Kleur.FromArgb(255, 145, 0, 0) ||

                            gedeelten[1].Stijl.VulKleur != Kleur.FromArgb(255, 201, 128, 2) ||

                            gedeelten[2].Stijl.VulKleur != Kleur.FromArgb(255, 18, 143, 4) ||

                            gedeelten[3].Stijl.VulKleur != Kleur.FromArgb(255, 145, 42, 100))

                        {

                            throw new Exception();

                        }

                        for (int j = 0; j < gedeelten.Length; j++)

                        {

                            var stijl = gedeelten[j].Stijl;

                            if (stijl.AutoLeading != false ||

                                stijl.HindiNummers != false ||

                                stijl.Spatiëring != 0 ||

                                stijl.Leidende != 0 ||

                                stijl.StreekKleur != Kleur.FromArgb(255, 175, 90, 163) ||

                                stijl.Opvolging != 50)

                            {

                                throw new Exception();

                            }

                        }

                        // Voorbeeld van tekstbewerking

                        gedeelten[0].Tekst = "Hallo ";

                        gedeelten[1].Tekst = "Wereld";

                        // Voorbeeld van verwijderen van tekstgedeelten

                        laag.TextData.RemovePortion(3);

                        laag.TextData.RemovePortion(2);

                        // Voorbeeld van toevoegen van nieuw tekstgedeelte

                        var aangemaaktGedeelte = laag.TextData.ProducePortion();

                        aangemaaktGedeelte.Tekst = "!!!\r";

                        laag.TextData.AddPortion(aangemaaktGedeelte);

                        gedeelten = laag.TextData.Items;

                        // Voorbeeld van alinea- en stijlbewerking voor gedeelten

                        // Rechtvaardiging instellen

                        gedeelten[0].Paragraaf.Rechtvaardiging = 1;

                        gedeelten[1].Paragraaf.Rechtvaardiging = 1;

                        gedeelten[2].Paragraaf.Rechtvaardiging = 1;

                        // Verschillende kleuren voor elke stijl. Ze zullen veranderen, maar de weergave wordt niet volledig ondersteund

                        gedeelten[0].Stijl.VulKleur = Kleur.Aquamarijn;

                        gedeelten[1].Stijl.VulKleur = Kleur.Violet;

                        gedeelten[2].Stijl.VulKleur = Kleur.Lichtblauw;

                        // Verschillend lettertype. Ze zullen veranderen, maar de weergave wordt niet volledig ondersteund

                        gedeelten[0].Stijl.FontGrootte = 6;

                        gedeelten[1].Stijl.FontGrootte = 8;

                        gedeelten[2].Stijl.FontGrootte = 10;

                        laag.TextData.UpdateLayerData();

                        im.Save(uitvoerpad, new PsdOptions(im));

                        break;

                    }

                }

            }

{{< /highlight >}}

**PSDNET-190. Ondersteuning voor Toevoegen laaggroep**

{{< highlight java >}}

             // -Groep 1

            // --Laag 1

            // --Groep 2

            // ---Laag 2

            // ---Laag 3

            // --Laag 4

            string databestand = "psdnet190_test.psd";

            var maakOpties = new PsdOptions();

            maakOpties.Bron = new BestandCreateSource(databestand, false);

            maakOpties.Palet = new PsdColorPalet(new Kleur[] { Kleur.Groen });

            using (var psdAfbeelding = (PsdAfbeelding)Afbeelding.Create(maakOpties, 500, 500))

            {

                Laaggroep groep1 = psdAfbeelding.AddLaaggroep("Groep 1", 0, true);

                Laag laag1 = new Laag(psdAfbeelding);

                laag1.Naam = "Laag 1";

                groep1.AddLaag(laag1);

                Laaggroep groep2 = groep1.AddLaaggroep("Groep 2", 1);

                Laag laag2 = new Laag(psdAfbeelding);

                laag2.Naam = "Laag 2";

                groep2.AddLaag(laag2);

                Laag laag3 = new Laag(psdAfbeelding);

                laag3.Naam = "Laag 3";

                groep2.AddLaag(laag3);

                Laag laag4 = new Laag(psdAfbeelding);

                laag4.Naam = "Laag 4";

                groep1.AddLaag(laag4);

               
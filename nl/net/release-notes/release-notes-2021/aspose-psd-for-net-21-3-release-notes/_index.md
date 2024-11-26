---
title: Aspose.PSD voor .NET 21.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-21-3-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Belangrijk**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-823|Voeg de SectionDividerLayer toe om de ervaring met laaggroepen te verbeteren|Verbetering|
|PSDNET-694|Bij het lezen van PattResource, werden breedte en hoogte omgewisseld|Fout|
|PSDNET-789|Onjuist mengen van meer dan één laageffect|Fout|
|PSDNET-805|Onjuiste mengvolgorde en logica wanneer er meer dan één laageffect is|Fout|
|PSDNET-842|Eigenschappen van de slageffecten worden niet opgeslagen in het PSD-bestand|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **Verwijderde API's:**
- Geen

## **Gebruikvoorbeelden:**

**PSDNET-694. Bij het lezen van PattResource werden breedte en hoogte omgewisseld**

{{< highlight csharp >}}
            string bronbestand = "Untitled-1.psd";
            string uitvoerbestand = "output.png";

            using (var afbeelding = (PsdImage)Image.Load(bronbestand))
            {
                var vulLaag = (FillLayer)afbeelding.Layers[1];
                vulLaag.Update(); // roept patroonweergave aan

                afbeelding.Save(uitvoerbestand, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Onjuist mengen van meer dan één laageffect**

{{< highlight csharp >}}
            string bronbestand = "bron_789.psd";
            string uitvoerSmartObjectPad = "uitvoer789.png";
            string uitvoerbestand = "uitvoer789.psd";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronbestand, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var lengte = afbeelding.Layers.Length;
                for (int i = 0; i < lengte; i++)
                {
                    var smart = afbeelding.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var stream = new MemoryStream(smart.Contents))
                        {
                            stream.Position = 0;
                            using (var afbInSmart = (PsdImage)Image.Load(stream))
                            {
                                for (int j = 0; j < afbInSmart.Layers.Length; j++)

                                {
                                    // Zoeken naar tekstlaag
                                    var tekstlaag = afbInSmart.Layers[j] as TextLayer;
                                    if (tekstlaag != null)
                                    {
                                        var tekstgegevens = tekstlaag.TextData;

                                        tekstgegevens.Items[0].Text = "Best";
                                        tekstgegevens.Items[0].Stijl.Fontgrootte = 170;
                                    }
                                }

                                smart.VervangInhoud(afbInSmart);
                            }
                        }

                        break;
                    }
                }
                // Op deze manier slaan we het gewijzigde PSD-bestand op
                afbeelding.Save(uitvoerSmartObjectPad, new PngOptions() { Colortype = PngColorType.TruecolorWithAlpha });
                afbeelding.Save(uitvoerbestand);
            }
{{< /highlight >}}

**PSDNET-805. Onjuiste mengvolgorde en logica wanneer er meer dan één laageffect is**

{{< highlight csharp >}}
            string bronbestand = "1_200x200.psd";
            string inhoudsbestand = "Numbers1Best.png";

            string uitvoerbestandPng = "output.png";
            string uitvoerbestandPsd = "output.psd";

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronbestand, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var lengte = afbeelding.Layers.Length;
                for (int i = 0; i < lengte; i++)
                {
                    var smart = afbeelding.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.VervangInhoud(inhoudsbestand);
                        break;
                    }
                }

                // Op deze manier slaan we het gewijzigde PSD-bestand op
                afbeelding.Save(uitvoerbestandPng, new PngOptions() { Colortype = PngColorType.TruecolorWithAlpha });
                afbeelding.Save(uitvoerbestandPsd);
            }
{{< /highlight >}}

**PSDNET-823. Voeg de SectionDividerLayer toe om de ervaring met laaggroepen te verbeteren**

{{< highlight csharp >}}
            // De volgende code toont SectionDividerLayer-lagen en hoe je de eraan gerelateerde LayerGroup kunt krijgen.

            // Lagenhiërarchie
            //    [0]: '</Laaggroep>' SectionDividerLayer voor Groep 1
            //    [1]: 'Laag 1' Reguliere Laag
            //    [2]: '</Laaggroep>' SectionDividerLayer voor Groep 2
            //    [3]: '</Laaggroep>' SectionDividerLayer voor Groep 3
            //    [4]: 'Groep 3' Groepslaag
            //    [5]: 'Groep 2' Groepslaag
            //    [6]: 'Groep 1' Groepslaag

            void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
            {
                if (!object.Equals(verwacht, werkelijk))
                {
                    throw new FormatException(bericht ?? "Objecten zijn niet gelijk.");
                }
            }

            using (var afbeelding = new PsdImage(100, 100))
            {
                // Lagenhiërarchie maken
                // Voeg de LayerGroup 'Groep 1' toe
                LayerGroup groep1 = afbeelding.AddLayerGroup("Groep 1", 0, true);
                // Voeg reguliere laag toe
                Layer laag1 = new Layer();
                laag1.Weergavenaam = "Laag 1";
                groep1.AddLayer(laag1);
                // Voeg de LayerGroup 'Groep 2' toe
                LayerGroup groep2 = groep1.AddLayerGroup("Groep 2", 1);
                // Voeg de LayerGroup 'Groep 3' toe
                LayerGroup groep3 = groep2.AddLayerGroup("Groep 3", 0);

                // Krijgt de SectionDividerLayer's
                SectionDividerLayer verdeler1 = (SectionDividerLayer)afbeelding.Lagen[0];
                SectionDividerLayer verdeler2 = (SectionDividerLayer)afbeelding.Lagen[2];
                SectionDividerLayer verdeler3 = (SectionDividerLayer)afbeelding.Lagen[3];

                // Gebruik de methode SectionDividerLayer.GetRelatedLayerGroup() om de gerelateerde LayerGroup-instantie te verkrijgen.
                AssertAreEqual(groep1.Weergavenaam, verdeler1.GetRelatedLayerGroup().Weergavenaam); // dezelfde LayerGroup
                AssertAreEqual(groep2.Weergavenaam, verdeler2.GetRelatedLayerGroup().Weergavenaam); // dezelfde LayerGroup
                AssertAreEqual(groep3.Weergavenaam, verdeler3.GetRelatedLayerGroup().Weergavenaam); // dezelfde LayerGroup

                LayerGroup map1 = verdeler1.GetRelatedLayerGroup();
                AssertAreEqual(5, map1.Lagen.Length); // 'Groep 1' bevat 5 lagen
            }
{{< /highlight >}}

**PSDNET-842. Eigenschappen van slageffecten worden niet opgeslagen in het PSD-bestand**

{{< highlight csharp >}}
            void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
            {
                if (!object.Equals(verwacht, werkelijk))
                {
                    throw new FormatException(bericht ?? "Objecten zijn niet gelijk.");
                }
            }

            string bronbestand = "slechtSlageffect.psd";
            string uitvoer = "output.psd";

            using (var afbeelding = (PsdImage)Image.Load(bronbestand, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var laag1 = new Layer();
                image.AddLayer(laag1);
                laag1.BlendingOptions.AddStroke(FillType.Color); // Zal geen ArgumentNullException gooien

                StrokeEffect slageffect = afbeelding.Lagen[1].BlendingOptions.AddStroke(FillType.Color);
                slageffect.Grootte = 10;
                slageffect.Positie = StrokePosition.Buiten;
                slageffect.Overprint = true;

                afbeelding.Save(uitvoer);
            }

            // Controleert opgeslagen waarden
            using (var afbeelding = (PsdImage)Image.Load(uitvoer, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect slageffect = (StrokeEffect)afbeelding.Lagen[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, slageffect.Grootte);
                AssertAreEqual(StrokePosition.Buiten, slageffect.Positie);
                AssertAreEqual(true, slageffect.Overprint);
            }
{{< /highlight >}}

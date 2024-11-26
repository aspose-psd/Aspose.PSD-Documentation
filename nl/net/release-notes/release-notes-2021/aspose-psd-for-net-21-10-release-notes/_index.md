---
title: Aspose.PSD voor .NET 21.10 - Release-opmerkingen
type: docs
weight: 30
url: /nl/net/aspose-psd-voor-net-21-10-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 21.10](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-128|Ondersteuning van het Smart Filters-mechanisme|Functie|
|PSDNET-414|Ondersteuning van Fxid/FEidResource|Functie|
|PSDNET-556|Fout bij het laden van AliasStructure|Fout|
|PSDNET-948|Wijziging van lettertype en kleur voor TextLayer PSD|Fout|
|PSDNET-971|Mogelijkheid toegevoegd om een laag met een vector masker op maat te maken|Verbetering|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.SmartFilters
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Naam
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.Distributie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.HoeveelheidRuis
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.IsEenkleurig
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.AddNoiseSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Naam
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.Straal
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.GaussianBlurSmartFilter.FilterType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gelijkmatig
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.NoiseDistribution.Gaussisch
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Naam
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.FilterId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.IsIngeschakeld
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Dekking
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Mengmodus
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Toepassen(Aspose.PSD.RasterImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.ToepassenOpMasker(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.BijLaden
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.Clone
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.SmartFilter.bronDescriptor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.Naam
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.Filters.UnknownSmartFilter.FilterId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsIngeschakeld
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsValidOpPositie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskerIngeschakeld
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskerGekoppeld
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.IsMaskerUitgebreidMetWit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.Filters
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResources.SmartFilters.SmartFilters.WaardenVanHulpbronBijwerken
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.#ctor(Systeem.Int32,Systeem.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Handtekening
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Versie
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FilterEffectMaskers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Lengte
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.Opslaan(Aspose.PSD.StreamContainer,Systeem.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FEidTypeToolKey
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FXidResource.FXidTypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.#ctor(Systeem.String,Aspose.PSD.Rechthoek,Systeem.Int32,Systeem.Int32,Aspose.PSD.FileFormats.Psd.Layers.InformatieOverKanalen[],Aspose.PSD.FileFormats.Psd.Layers.InformatieOverKanalen,Aspose.PSD.Rechthoek,Aspose.PSD.FileFormats.Psd.Layers.InformatieOverKanalen)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Lengte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GID
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Rechthoek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.PixelDiepte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaximaleKanalen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Kanalen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.Gebruikersmasker
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.MaskerRechthoek
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.SheetMasker
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FilterEffectMaskData.GegevensOpslaan(Aspose.PSD.StreamContainer)

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-128. Ondersteuning van het Smart Filters-mechanisme**

{{< highlight csharp >}}
            string bronBestand = "r2_SmartFilters.psd";
             string uitvoerPsd = "uit_r2_SmartFilters.psd";

            void AssertAreEqual(object verwacht, object werkelijk)
            {
                if (!object.Equals(verwacht, werkelijk))
                {
                    throw new Exception("Objecten zijn niet gelijk.");
               }
             }

            using (var afbeelding = (PsdImage)Afbeelding.Laden(bronBestand))
            {
                SmartObjectLayer slimObj = (SmartObjectLayer)afbeelding.Lagen[1];

                // slimme filters bewerken
                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)slimObj.SmartFilters.Filters[0];

                // controleer filterwaarden
                AssertAreEqual(3.1, gaussianBlur.Straal);
                AssertAreEqual(BlendMode.Dissolve, gaussianBlur.Mengmodus);
                AssertAreEqual(90d, gaussianBlur.Dekking);
                AssertAreEqual(true, gaussianBlur.IsIngeschakeld);

                // bijwerken filterwaarden
                gaussianBlur.Straal = 1;
                gaussianBlur.Mengmodus = BlendMode.Divide;
                gaussianBlur.Dekking = 75;
                gaussianBlur.IsIngeschakeld = false;
                AddNoiseSmartFilter addNoise = (AddNoiseSmartFilter)slimObj.SmartFilters.Filters[1];
                addNoise.Distributie = NoiseDistribution.Gelijkmatig;

                // nieuwe filteritems toevoegen
                var filters = new List<SmartFilter>(slimObj.SmartFilters.Filters);
                filters.Add(new GaussianBlurSmartFilter());
                filters.Add(new AddNoiseSmartFilter());
                slimObj.SmartFilters.Filters = filters.ToArray();

                // wijzigingen toepassen
                slimObj.SmartFilters.WaardenVanHulpbronBijwerken();

                // Filters toepassen
                slimObj.SmartFilters.Filters[0].Toepassen(afbeelding.Lagen[2]);
                slimObj.SmartFilters.Filters[4].ToepassenOpMasker(afbeelding.Lagen[2]);

                afbeelding.Opslaan(uitvoerPsd);
            }

            using (var afbeelding = (PsdImage)Afbeelding.Laden(uitvoerPsd))
            {
                SmartObjectLayer slimObj = (SmartObjectLayer)afbeelding.Lagen[1];

                GaussianBlurSmartFilter gaussianBlur = (GaussianBlurSmartFilter)slimObj.SmartFilters.Filters[0];

                // controleer filterwaarden
                AssertAreEqual(1d, gaussianBlur.Straal);
                AssertAreEqual(BlendMode.Divide, gaussianBlur.Mengmodus);
                AssertAreEqual(75d, gaussianBlur.Dekking);
                AssertAreEqual(false, gaussianBlur.IsIngeschakeld);

                AssertAreEqual(true, slimObj.SmartFilters.Filters[5] is GaussianBlurSmartFilter);
                AssertAreEqual(true, slimObj.SmartFilters.Filters[6] is AddNoiseSmartFilter);
            }
{{< /highlight >}}

**PSDNET-414. Ondersteuning van Fxid/FEidResource**

{{< highlight csharp >}}
            string invoerBestandPad = "psdnet414_3.psd";
            string uitvoer = "uit_psdnet414_3.psd";

            int resLengte = 1144;
            int maskerLengte = 369;

            void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
            {
                 if (!object.Equals(verwacht, werkelijk))
                 {
                     throw new FormatException(bericht ?? "Objecten zijn niet gelijk.");
                 }
             }

            using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(invoerBestandPad))
            {
                FXidResource fXidResource = (FXidResource)psdAfbeelding.GlobaleLaagHulpbronnen[3];

                AssertAreEqual(resLengte, fXidResource.Lengte);
                foreach (var maskerData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskerLengte, maskerData.Lengte);
                }

                psdAfbeelding.Opslaan(uitvoer);
            }

            // controleer na opslaan
            using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(uitvoer))
            {
                FXidResource fXidResource = (FXidResource)psdAfbeelding.GlobaleLaagHulpbronnen[3];

                AssertAreEqual(resLengte, fXidResource.Lengte);
                foreach (var maskerData in fXidResource.FilterEffectMasks)
                {
                    AssertAreEqual(maskerLengte, maskerData.Lengte);
                }
            }
{{< /highlight >}}

**PSDNET-556. Fout bij het laden van AliasStructure**

{{< highlight csharp >}}
            string bronBestand = "Aspose.psd";
            string uitvoerPsd = "uit_Aspose.psd";
            string uitvoerPng = "uit_Aspose.png";

            void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
            {
                 if (!object.Equals(verwacht, werkelijk))
                 {
                     throw new FormatException(bericht ?? "Objecten zijn niet gelijk.");
             }
             }

             using (var afbeelding = (PsdImage)Afbeelding.Laden(bronBestand))
             {
                  LnkeResource lnkeResource = (LnkeResource)afbeelding.GlobaleLaagHulpbronnen[3];
                  LiFeDataSource dataSource = (LiFeDataSource)lnkeResource[0];
                  AssertAreEqual(2484L, dataSource.Lengte);

                  foreach (var laag in afbeelding.Lagen)
                  {
                       if (laag is TextLayer)
                       {
                           TextLayer tekstLaag = laag as TextLayer;
                           tekstLaag.UpdateText("Test", Aspose.PSD.Kleur.Zwart);
                       }
                  }

                  afbeelding.Opslaan(uitvoerPsd);
                  afbeelding.Opslaan(uitvoerPng, new PngOptions() { KleurType = PngColorType.GrijsMetAlpha });
           }
{{< /highlight >}}

**PSDNET-948. Wijziging van lettertype en kleur voor TextLayer PSD**

{{< highlight csharp >}}
            string bronBestandsNaam = "fontExamples948.psd";
            string testLettertypenMap = "Lettertypen";
            string uitvoerPng = "uitvoer.png";

            FontSettings.SetFontsFolder(testLettertypenMap);

            using (PsdImage afbeelding = (PsdImage)Aspose.PSD.Image.Load(bronBestandsNaam))
            {
                 foreach (var laag in afbeelding.Lagen)
                 {
                     var tekstLaag = laag as TextLayer;
                     if (tekstLaag != null)
                     {
                         ITextPortion tekstDeel = tekstLaag.TextData.Items[0];
                         tekstDeel.Style.FillColor = Color.BlueViolet;

                         tekstLaag.TextData.UpdateLayerData();
                     }
                 }

                 afbeelding.Opslaan(uitvoerPng, new PngOptions());
         }
{{< /highlight >}}

**PSDNET-971. Mogelijkheid toegevoegd om een laag met een vector masker op maat te maken**

{{< highlight csharp >}}
        public void EenVoorbeeldVanHetMakenVanEenVectorpad()
        {
            string bestandsNaam = "PathExample2.psd";

            string uitvoer```csharp
            string uitvoerPsd = "uit_CreatingVectorPathExampleTest.psd";
            string uitvoerPng = "uit_CreatingVectorPathExampleTest.png";

            using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(bestandsNaam))
            {
                VectorDataProvider.RemoveVectorPathDataFromLayer(psdAfbeelding.Lagen[2]);

                // VectorPath-object maken voor een bestaande laag zonder vectorpadgegevens.
                VectorPath vectorPad = VectorDataProvider.CreateVectorPathForLayer(psdAfbeelding.Lagen[1]);

                // De vulkleur van het vectorpad instellen
                vectorPad.FillColor = Color.MediumPurple;

                // nieuw vorm toevoegen
                PathShape nieuweVorm = new PathShape();
                nieuweVorm.Punten.Add(new BezierKnot(new PointF(65, 175), true));
                nieuweVorm.Punten.Add(new BezierKnot(new PointF(65, 210), true));
                nieuweVorm.Punten.Add(new BezierKnot(new PointF(190, 210), true));
                nieuweVorm.Punten.Add(new BezierKnot(new PointF(190, 175), true));
                vectorPad.Vormen.Add(nieuweVorm);

                // padgegevens bijwerken in laag
                VectorDataProvider.UpdateLayerFromVectorPath(psdAfbeelding.Lagen[1], vectorPad, true);

                // VectorPath-object maken voor nieuwe laag.
                FillLayer laag2 = FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Lagen.FillSettings.FillType.Kleur);
                laag2.Weer te geven naam = "Laag 2";
                psdAfbeelding.VoegLaagToe(laag2);
                VectorPath vectorPad2 = VectorDataProvider.CreateVectorPathForLayer(laag2);

                // De vulkleur van het vectorpad instellen
                vectorPad2.FillColor = Color.IndianRed;

                // nieuw vorm toevoegen
                PathShape nieuweVorm2 = new PathShape();
                nieuweVorm2.Punten.Add(new BezierKnot(new PointF(50, 150), true));
                nieuweVorm2.Punten.Add(new BezierKnot(new PointF(100, 200), true));
                nieuweVorm2.Punten.Add(new BezierKnot(new PointF(0, 200), true));
                vectorPad2.Vormen.Add(nieuweVorm2);

                // padgegevens bijwerken in laag
                VectorDataProvider.UpdateLayerFromVectorPath(laag2, vectorPad2, true);

                psdAfbeelding.Opslaan(uitvoerPsd);
                psdAfbeelding.Opslaan(uitvoerPng, new PngOptions() { KleurType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorMetAlpha });
            }
        }
```
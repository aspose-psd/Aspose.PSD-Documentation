---
title: Aspose.PSD voor .NET 20.2 - Release-opmerkingen
type: docs
weight: 110
url: /nl/net/aspose-psd-voor-net-20-2-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-206|Verbetering van de mogelijkheid om tekst in verschillende kleuren weer te geven in tekstlaag|Functie|
|PSDNET-369|Ondersteuning van clbl-bron (Laagbron bevat informatie over samenvoegingsklemmen)|Functie|
|PSDNET-274 |Ondersteuning van blwh-bron (Bron bevat gegevens van zwart-wit aanpassingslaag)|Functie|
|PSDNET-230|Mogelijkheid om laaggroep te exporteren naar Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf|Functie|
|PSDNET-372|Ondersteuning van lspf-bron (Bevat instellingen over laagbeveiliging)|Functie|
|PSDNET-370|Ondersteuning van infx-bron (Bevat gegevens over mengen van interne elementen)|Functie|
|PSDNET-251|Refactoring van PsdImage en Laag om transformatiegedrag te wijzigen (Juiste formaataanpassing/rotatie/bijsnijden voor laagmaskers als we één laag afzonderlijk transformeren)|Verbetering|
|PSDNET-276 |In sommige globalisatie-instellingen kan AI-afbeeldingsrasterafbeelding niet worden geopend|Fout|
|PSDNET-194|Na het uitvoeren van de FlipRotate operatie op de laag wordt de PSD-afbeelding onleesbaar|Fout|
|PSDNET-177. |System.ArgumentException tijdens het laden van PSD-bestand|Fout|
|PSDNET-249|Na het gebruik van een transformatiemethode voor alleen een laag heeft de opgeslagen laag onjuiste grenzen of een masker|Fout|

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerMaskDataFull.UserMaskRectangle
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.ReleaseManagedResources
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerGroup.Breedte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerGroup.Hoogte
- T:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Rood
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Geel
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Groen
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Cyaan
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Blauw
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Magenta
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.GebruikTint
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.BwPresetSoort
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.ZwartEnWitPresetBestandsnaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.Tintkleur
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.TintRood
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.TintGroen
- P:Aspose.PSD.FileFormats.Psd.Lagen.Aanpassingslagen.ZwartWitAanpassingslaag.TintBlauw
- T:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.#ctor
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Opslaan(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.TypeGereedschapsleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Lengte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Rood
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Geel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Groen
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Cyaan
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Blauw
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.Magenta
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.GebruikTint
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.BwPresetSoort
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.ZwartEnWitPresetBestandsnaam
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.BlwhBron.TintKleur
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.Lr16Bron.#ctor
- P:Aspose.PSD.Xmp.Types.Derived.RenditionClass.GedefinieerdeWaarden
- T:Aspose.PSD.AggregateException
- M:Aspose.PSD.CmykKleur.Equals(System.Object)
- T:Aspose.PSD.SamenstellingException
- T:Aspose.PSD.KernUitzonderingen.IndexUitDeReeksException
- M:Aspose.PSD.KernUitzonderingen.IndexUitDeReeksException.#ctor(System.String)
- M:Aspose.PSD.KernUitzonderingen.IndexUitDeReeksException.#ctor(System.String,System.Exception)
- F:Aspose.PSD.Bestandsformaat.Otg
- T:Aspose.PSD.FileFormats.Jpeg2000.Jpeg2000AangepasteUitzondering
- T:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.#ctor(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.Sleutel
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.Lengte
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.PsdVersie
- P:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.IsGegevensAfzonderlijkOpgeslagen
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.KrijgChannelGegevens(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.KrijgActieveBeheerder
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.Opslaan(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.KrijgCurveBeheerder
- F:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.CurvBron.TypeGereedschapsleutel
- T:Aspose.PSD.AfbeeldingOpties.TiffOptieUtils
- M:Aspose.PSD.AfbeeldingOpties.TiffOptieUtils.#ctor
- M:Aspose.PSD.AfbeeldingOpties.TiffOptieUtils.KrijgGeldigeMarkeringenTelling(Aspose.PSD.FileFormats.Tiff.TiffGegevenstype[])
- P:Aspose.PSD.AfbeeldingOptiesBase.VoortgangsEventHandler
- P:Aspose.PSD.LaadOpties.VoortgangsEventHandler
- M:Aspose.PSD.Matrix.#ctor(Aspose.PSD.Matrix)
- M:Aspose.PSD.Gemeten.Equals(System.Object)
- T:Aspose.PSD.VoortgangsEventHandler
- T:Aspose.PSD.Voortgangsmanagement.GevenType
- F:Aspose.PSD.Voortgangsmanagement.GevenType.RelatieveVoortgang
- F:Aspose.PSD.Voortgangsmanagement.GevenType.FaseWijziging
- F:Aspose.PSD.Voortgangsmanagement.GevenType.Initialisatie
- F:Aspose.PSD.Voortgangsmanagement.GevenType.VoorVerwerking
- F:Aspose.PSD.Voortgangsmanagement.GevenType.Verwerking
- F:Aspose.PSD.Voortgangsmanagement.GevenType.Voltooiing
- T:Aspose.PSD.Voortgangsmanagement.VoortgangsEventHandlerInfo
- P:Aspose.PSD.Voortgangsmanagement.VoortgangsEventHandlerInfo.Omschrijving
- P:Aspose.PSD.Voortgangsmanagement.VoortgangsEventHandlerInfo.GevenType
- P:Aspose.PSD.Voortgangsmanagement.VoortgangsEventHandlerInfo.MaxWaarde
- P:Aspose.PSD.Voortgangsmanagement.VoortgangsEventHandlerInfo.Waarde
- M:Aspose.PSD.RasterAfbeelding.KrijgSchuineHoek
- M:Aspose.PSD.RasterAfbeelding.NormaliseerHoek
- M:Aspose.PSD.RasterAfbeelding.NormaliseerHoek(System.Boolean,Aspose.PSD.Kleur)
# **Verwijderde API's:**
- M:Aspose.PSD.FileFormats.Ai.AiDataSection.Afsluiten
- P:Aspose.PSD.FileFormats.Ai.AiRasterAfbeelding.GebiedsRechthoek
- M:Aspose.PSD.FileFormats.Psd.Lagen.LayerResources.Lr16Bron.#ctor(System.Int32)
- F:Aspose.PSD.Xmp.Typen.Afgeleid.RenditieKlasse.GedefinieerdeWaarden

## **Gebruik voorbeelden:**
**PSDNET-206. Verbetering van de mogelijkheid om tekst in verschillende kleuren weer te geven in tekstlaag**

{{< highlight java >}}

  met (var psdAfbeelding = (PsdAfbeelding)Afbeelding.Laden("tekst_ethalon_verschillende_kleuren.psd"))

{

    var txtLaag = (TekstLaag)psdAfbeelding.Lagen[1];

    txtLaag.TekstGegevens.BijwerkenLaagGegevens();

    psdAfbeelding.Opslaan("output.png", new PngOpties());

}

{{< /highlight >}}

**PSDNET-369. Ondersteuning van clbl-bron (Laagbron bevat informatie over samenvoegingsklemmen)**

{{< highlight java >}}

        void AssertIsTrue(bool voorwaarde, string bericht)

        {

            als (!voorwaarde)

            {

                gooien nieuwe FormaatUitzondering(bericht);

            }

        }

        string bronBestandsnaam = "MonsterVoorBron.psd";

        string doelBestandsnaam = "Uitvoer" + bronBestandsnaam;

        ClblBron KrijgClblBron(PsdAfbeelding afb)

        {

            voor elk (var laag in afb.Lagen)

            {

                voor elk (var laagBron in laag.Bronnen)

                {

                    als (laagBron is ClblBron)

                    {

                        retourneer (ClblBron)laagBron;

                    }

                }

            }

            gooien nieuwe Uitzondering("De gespecificeerde ClblBron is niet gevonden");

        }

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam))

        {

            var bron = KrijgClblBron(afb);

            AssertIsTrue(bron.SamenvoegingsgeknipteElementen, "De ClblBron.SamenvoegingsgeknipteElementen zou waar moeten zijn");

            // Test bewerken en opslaan

            bron.SamenvoegingsgeknipteElementen = false;

            afb.Opslaan(doelBestandsnaam);

        }

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(doelBestandsnaam))

        {

            var bron = KrijgClblBron(afb);

            AssertIsTrue(!bron.SamenvoegingsgeknipteElementen, "De ClblBron.SamenvoegingsgeknipteElementen zou moeten veranderen naar onwaar");

        }

{{< /highlight >}}

**PSDNET-274. Ondersteuning van blwh-bron (Bron bevat gegevens van zwart-wit aanpassingslaag)**

{{< highlight java >}}

         const string WaardeBerichtIsVerkeerd = "Verwachte eigenschapswaarde is niet gelijk aan de feitelijke waarde";

        void AssertIsTrue(bool voorwaarde, string bericht)

        {

            als (!voorwaarde)

            {

                gooien nieuwe FormaatUitzondering(bericht);

            }

        }

        leeg VoorbeeldOndersteuningVanBlwhBron(

            string bronBestandsnaam,

            int rood,

            int geel,

            int groen,

            int cyaan,

            int blauw,

            int magenta,

            bool gebruikTint,

            int bwPresetSoort,

            string bwPresetBestandsnaam,

            dubbele tintKleurRood,

            dubbele tintKleurGroen,

            dubbele tintKleurBlauw,

            int tintKleur,

            int nieuweTintKleur)

        {

            string doelBestandsnaam = "Uitvoer" + bronBestandsnaam;

            bool isVereisteBronGevonden = false;

            met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam))

            {

                voor elk (var laag in afb.Lagen)

                {

                    voor elk (var laagBron in laag.Bronnen)

                    {

                        als (laagBron is BlwhBron)

                        {

                            var blwhBron = (BlwhBron)laagBron;

                            var blwhLaag = (ZwartWitAanpassingsLaag)laag;

                            isVereisteBronGevonden = waar;

                            AssertIsTrue(blwhBron.Rood == rood, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Geel == geel, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Groen == groen, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Cyaan == cyaan, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Blauw == blauw, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Magenta == magenta, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.GebruikTint == gebruikTint, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.TintKleur == tintKleur, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.BwPresetSoort == bwPresetSoort, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.ZwartEnWitPresetBestandsnaam == bwPresetBestandsnaam, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurRood - tintKleurRood) < 1e-6, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurGroen - tintKleurGroen) < 1e-6, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurBlauw - tintKleurBlauw) < 1e-6, WaardeBerichtIsVerkeerd);

                            // Test bewerken en opslaan

                            blwhBron.Rood = rood - 15;

                            blwhBron.Geel = geel - 15;

                            blwhBron.Groen = groen + 15;

15,

                            blwhBron.Cyaan = cyaan + 15;

                            blwhBron.Blauw = blauw - 15;

                            blwhBron.Magenta = magenta - 15;

                            blwhBron.GebruikTint = !gebruikTint;

                            blwhBron.BwPresetSoort = 4;

                            blwhBron.ZwartEnWitPresetBestandsnaam = "bwPresetBestandsnaam";

                            blwhLaag.TintKleurRood = tintKleurRood - 60;

                            blwhLaag.TintKleurGroen = tintKleurGroen - 60;

                            blwhLaag.TintKleurBlauw = tintKleurBlauw - 60;

                            afb.Opslaan(doelBestandsnaam);

                            breken;

                        }

                    }

                }

            }

            AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde BlwhBron is niet gevonden");

            isVereisteBronGevonden = false;

            met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(doelBestandsnaam))

            {

                voor elk (var laag in afb.Lagen)

                {

                    voor elk (var laagBron in laag.Bronnen)

                    {

                        als (laagBron is BlwhBron)

                        {

                            var blwhBron = (BlwhBron)laagBron;

                            var blwhLaag = (ZwartWitAanpassingsLaag)laag;

                            isVereisteBronGevonden = waar;

                            AssertIsTrue(blwhBron.Rood == rood - 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Geel == geel - 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Groen == groen + 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Cyaan == cyaan + 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Blauw == blauw - 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.Magenta == magenta - 15, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(!blwhBron.GebruikTint == gebruikTint, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.TintKleur == nieuweTintKleur, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.BwPresetSoort == 4, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(blwhBron.ZwartEnWitPresetBestandsnaam == "bwPresetBestandsnaam", WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurRood - tintKleurRood + 60) < 1e-6, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurGroen - tintKleurGroen + 60) < 1e-6, WaardeBerichtIsVerkeerd);

                            AssertIsTrue(Math.Abs(blwhLaag.TintKleurBlauw - tintKleurBlauw + 60) < 1e-6, WaardeBerichtIsVerkeerd);

                            breken;

                        }

                    }

                }

            }

            AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde BlwhBron is niet gevonden");

        }

        Console.WriteLine("BlwhBron bijwerken werkt zoals verwacht. Druk op een toets.");

{{< /highlight >}}

**PSDNET-230. Mogelijkheid om laaggroep te exporteren naar Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf**

{{< highlight java >}}

  met (var psdAfbeelding = (PsdAfbeelding)Afbeelding.Laden("1.psd"))

            {

                // map met achtergrond

                LaagGroep bg_map = (LaagGroep)psdAfbeelding.Lagen[0];

                // map met inhoud

                LaagGroep inhoud_map = (LaagGroep)psdAfbeelding.Lagen[4];

                bg_map.Opslaan("achtergrond.png", new PngOpties());

                inhoud_map.Opslaan("inhoud.png", new PngOpties());

            }

{{< /highlight >}}

` `**PSDNET-372. Ondersteuning van lspf-bron (Bevat instellingen over laagbeveiliging)**

{{< highlight java >}}

         const string WaardeBerichtIsVerkeerd = "Verwachte eigenschapswaarde is niet gelijk aan de feitelijke waarde";

        void AssertIsTrue(bool voorwaarde, string bericht)

        {

            als (!voorwaarde)

            {

                gooien nieuwe FormaatUitzondering(bericht);

            }

        }

        string bronBestandsnaam = "MonsterVoorBron.psd";

        string doelBestandsnaam = "Uitvoer" + bronBestandsnaam;

        bool isVereisteBronGevonden = false;

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam))

        {

            voor elk (var laag in afb.Lagen)

            {

                voor elk (var laagBron in laag.Bronnen)

                {

                    als (laagBron is LspfBron)

                    {

                        var bron = (LspfBron)laagBron;

                        isVereisteBronGevonden = waar;

                        AssertIsTrue(false == bron.IsSamengesteldBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsPositieBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsTransparantieBeveiligd, WaardeBerichtIsVerkeerd);

                        // Test bewerken en opslaan

                        bron.IsSamengesteldBeveiligd = waar;

                        AssertIsTrue(waar == bron.IsSamengesteldBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsPositieBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsTransparantieBeveiligd, WaardeBerichtIsVerkeerd);

                        bron.IsSamengesteldBeveiligd = false;

                        bron.IsPositieBeveiligd = waar;

                        AssertIsTrue(false == bron.IsSamengesteldBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(waar == bron.IsPositieBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsTransparantieBeveiligd, WaardeBerichtIsVerkeerd);

                        bron.IsPositieBeveiligd = false;

                        bron.IsTransparantieBeveiligd = waar;

                        AssertIsTrue(false == bron.IsSamengesteldBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(false == bron.IsPositieBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(waar == bron.IsTransparantieBeveiligd, WaardeBerichtIsVerkeerd);

                        bron.IsSamengesteldBeveiligd = waar;

                        bron.IsPositieBeveiligd = waar;

                        bron.IsTransparantieBeveiligd = waar;

                        afb.Opslaan(doelBestandsnaam);

                        breken;

                    }

                }

            }

        }

        AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde LspfBron is niet gevonden");

        isVereisteBronGevonden = false;

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(doelBestandsnaam))

        {

            voor elk (var laag in afb.Lagen)

            {

                voor elk (var laagBron in laag.Bronnen)

                {

                    als (laagBron is LspfBron)

                    {

                        var bron = (LspfBron)laagBron;

                        isVereisteBronGevonden = waar;

                        AssertIsTrue(bron.IsSamengesteldBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(bron.IsPositieBeveiligd, WaardeBerichtIsVerkeerd);

                        AssertIsTrue(bron.IsTransparantieBeveiligd, WaardeBerichtIsVerkeerd);

                        breken;

                    }

                }

            }

        }

        AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde LspfBron is niet gevonden");

        Console.WriteLine("LspfBron bijwerken werkt zoals verwacht. Druk op een toets.");

{{< /highlight >}}

` `**PSDNET-370. Ondersteuning van infx-bron (Bevat gegevens over mengen van interne elementen)**

{{< highlight java >}}

         void AssertIsTrue(bool voorwaarde, string bericht)

        {

            als (!voorwaarde)

            {

                gooien nieuwe FormaatUitzondering(bericht);

            }

        }

        string bronBestandsnaam = "MonsterVoorBron.psd";

        string doelBestandsnaam = "Uitvoer" + bronBestandsnaam;

        bool isVereisteBronGevonden = false;

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam))

        {

            voor elk (var laag in afb.Lagen)

            {

                voor elk (var laagBron in laag.Bronnen)

                {

                    als (laagBron is InfxBron)

                    {

                        var bron = (InfxBron)laagBron;

                        isVereisteBronGevonden = waar;

                        AssertIsTrue(!bron.BinnensteElementenMengen, "De InfxBron.BinnensteElementenMengen zou onwaar moeten zijn");

                        // Test bewerken en opslaan

                        bron.BinnensteElementenMengen = waar;

                        afb.Opslaan(doelBestandsnaam);

                        breken;

                    }

                }

            }

        }

        AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde InfxBron is niet gevonden");

        isVereisteBronGevonden = false;

        met (PsdAfbeelding afb = (PsdAfbeelding)Afbeelding.Laden(doelBestandsnaam))

        {

            voor elk (var laag in afb.Lagen)

            {

                voor elk (var laagBron in laag.Bronnen)

                {

                    als (laagBron is InfxBron)

                    {

                        var bron = (InfxBron)laagBron;

                        isVereisteBronGevonden = waar;

                        AssertIsTrue(bron.BinnensteElementenMengen, "De InfxBron.BinnensteElementenMengen zou moeten veranderen in waar");

                        breken;

                    }

                }

            }

        }

        AssertIsTrue(isVereisteBronGevonden, "De gespecificeerde InfxBron is niet gevonden");

{{< /highlight >}}

**PSDNET-251. Refactoring van PsdAfbeelding en Laag om transformatiegedrag te wijzigen (Juiste formaataanpassing/rotatie/bijsnijden voor laagmaskers als we één laag afzonderlijk transformeren)**

{{< highlight java >}}

             var enums = (RotateFlipType[])Enum.GetValues(typeof(RotateFlipType));

            var bestandsnamen = new string[]

            {

                "EénNormaalEnEénAanpassingMetVectorEnLaagmasker",

                "EénNormaalEnEénAanpassingMetLaagmasker", 

                "TekstLaag",

                "GekoppeldeVormenMetTekst"

            };

            voor elk (string bestandsnaam in bestandsnamen)

            {

                voor elk (RotateFlipType draaiKantelType in enums)

                {

                    string bronBestandsnaam = bestandsnaam + ".psd";

                    string doelBestandsnaam = bestandsnaam + "_" + draaiKantelType;

                    var psdLaadOpties = nieuwe PsdLaadOpties() { LaadEffectenBron = waar };

                    met (PsdAfbeelding afbeelding = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam, psdLaadOpties))

                    {

                        afbeelding.DraaiKantel(draaiKantelType);

                        afbeelding.Opslaan(doelBestandsnaam);

                    }

                }

            }

{{< /highlight >}}

**PSDNET-276. In sommige globalisatie-instellingen kan AI-afbeeldingsrasterafbeelding niet worden geopend**

{{< highlight java >}}

        string bronBestandsnaam = "form_raster_8.ai";

        System.Threading.Thread.CurrentThread.CurrentCulture = nieuwe System.Globalization.CultureInfo("ru_RU");

        System.Threading.Thread.CurrentThread.CurrentUICulture = System.Threading.Thread.CurrentThread.CurrentCulture;

        met (AiAfbeelding afbeelding = (AiAfbeelding)Afbeelding.Laden(bronBestandsnaam))

        {

            // er mag geen uitzondering worden gegenereerd

        }

{{< /highlight >}}

**PSDNET-194. Na het uitvoeren van de FlipRotate-operatie op de laag wordt de PSD-afbeelding onleesbaar**

{{< highlight java >}}

             string bronBestandsnaam = GetBestandInAangepasteMapTenOpzichteVanBasis(@"testdata\Problemen\IMAGINGNET-2617\1.psd");

            var draaiType = RotateFlipType.Rotate90FlipNone;

            var uitvoerBestandsnaamPsd = this.GetBestandInUitvoermap("RotateFlipTest2617.psd");

            probeer

            {

                met (PsdAfbeelding afbeelding = (PsdAfbeelding)Afbeelding.Laden(bronBestandsnaam))

                {

                    voor (int i = 0; i < afbeelding.Lagen.Lengte; i++)

                    {

                        var laag = afbeelding.Lagen[i];

                        als (!laag.Grenzen.IsEmpty)

                        {

                            laag.DraaiKantel(draaiType);

                        }

                    }

                    string uitvoerBestandsnaamPng = this.GetBestandInUitvoermap("RotateFlipTest2617.png");

                    afbeelding.Opslaan(uitvoerBestandsnaamPsd);

                }

            // Hier krijgen we een uitzondering. Voor PhotoShop is dit bestand ook onleesbaar,

            met (PsdAfbeelding afbeelding = (PsdAfbeelding)Afbeelding.Laden(uitvoerBestandsnaamPsd)) // Genereert een uitzondering

            {

                // Doe niets

            }

{{< /highlight >}}

**PSDNET-177. System.ArgumentException tijdens het laden van PSD-bestand**

{{< highlight java >}}

         string bronPad = "1.psd";

        string psdPad = "RotateFlipTest2617.psd";

        RotateFlipType draaiKantelType = RotateFlipType.Rotate270FlipXY;

        met (var im = (PsdAfbeelding)(Afbeelding.Laden(bronPad)))

        {

            im.DraaiKantel(draaiKantelType);

            im.Opslaan(psdPad);

        }

        met (var im = (PsdAfbeelding)(Afbeelding.Laden(psdPad))) // Hier mogen geen uitzonderingen worden gegenereerd

        {

            // doe niets

        }

{{< /highlight >}}

**PSDNET-249. Na het gebruik van een transformatiemethode voor alleen een laag heeft de opgeslagen laag onjuiste grenzen of een masker**

{{< highlight java >}}

         void AssertIsTrue(bool voorwaarde, string bericht)

        {

            als (!voorwaarde)

            {

                gooien nieuwe FormaatUitzondering(bericht);

            }

        }

        const dubbele Tolerantie = 1e-6;

        int nieuweBreedte = 132;

        int nieuweHoogte = 247;

        dubbele xSchaal = nieuweBreedte / 48.0;

        dubbele ySchaal = nieuweHoogte / 19.0;

        string bronBestandsnaam = "TekstLaag.psd";

        string uitvoerBestandsnaam = "TekstLaagResize" + nieuweBreedte + "_" + nieuweHoogte;

        var psdLaadOpties = nieuwe PsdLaadOpties() { LaadEffectenBron = waar };

        met (PsdAfbeelding afbeelding = (PsdAfbeelding) Afbeelding.Laden(bronBestandsnaam, psdLaadOpties))

        {

            var laag = afbeelding.Lagen[1] as TekstLaag;

            var nieuweLinks = laag.Links - (nieuweBreedte - laag.Breedte) / 2;

            var nieuweBoven = laag.Boven - (nieuweHoogte - laag.Hoogte) / 2;

            laag.FormaatAanpassen(nieuweBreedte, nieuweHoogte);

            AssertIsTrue(laag.Links == nieuweLinks, "Eigenschap Links van laag zou " + nieuweLinks moeten zijn");

            AssertIsTrue(laag.Boven == nieuweBoven, "Eigenschap Boven van laag zou " + nieuweBoven moeten zijn");

            AssertIsTrue(laag.Breedte == nieuweBreedte, "Eigenschap Breedte van la
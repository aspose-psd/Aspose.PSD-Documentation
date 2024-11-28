---
title: Aspose.PSD voor .NET 21.9 - Release-opmerkingen
type: docs
weight: 40
url: /nl/net/aspose-psd-voor-net-21-9-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat de release-opmerkingen voor [Aspose.PSD voor .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-574|Maak RLE-compressie standaard voor het opslaan van PSD om enorme uitvoer PSD te vermijden|Functie|
|PSDNET-747|Ondersteuning van de Overlay Pattern Layer Effects met de multikanaal kleurmodus in het PSD-bestand|Functie|
|PSDNET-951|Na het maken van de nieuwe laag is de eigenschap Resources null waardoor manipulaties worden voorkomen (bijvoorbeeld formaat wijzigen)|Fout|
|PSDNET-955|Niet ondersteund van compressiemethoden ZipWithPrediction voor 8bit|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- Geen

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-574. Maak RLE-compressie standaard voor het opslaan van PSD om enorme uitvoer PSD te vermijden**

{{< highlight csharp >}}
            string inputFilePath = "bestand.psd";
            string output1 = "output_oorspronkelijk.psd";
            string output2 = "output_psdOpties.psd";

            using (Afbeelding afbeelding = Afbeelding.Laden(inputFilePath))
            {
                afbeelding.Opslaan(output1);
                afbeelding.Opslaan(output2, new PsdOpties());
            }
{{< /highlight >}}

**PSDNET-747. Ondersteuning van de Overlay Pattern Layer Effects met de multikanaal kleurmodus in het PSD-bestand**

{{< highlight csharp >}}
            var bestandsnaam = "AlleEffecten.psd";
            var uitvoerBestand = "AlleEffecten_uit.psd";
            var laadOpties = new PsdLaadOpties()
            {
                LaadEffectenResource = true
            };

            // Moet geen uitzondering veroorzaken
            using (var afb = Afbeelding.Laden(bestandsnaam, laadOpties))
            {
                // Moet geen uitzondering veroorzaken
                afb.Opslaan(uitvoerBestand);
            }
{{< /highlight >}}

**PSDNET-951. Na het maken van de nieuwe laag is de eigenschap Resources null waardoor manipulaties worden voorkomen (bijvoorbeeld formaat wijzigen)**

{{< highlight csharp >}}
            string PSDBestand = "Laag1.psd";
            string laag1Bestand = "Laag2.png";
            string laag2Bestand = "Laag3.png";
            string uitvoerBestandsnaam = "definitieveUitvoer.psd";

            void VervangKleur(RasterAfbeelding afbeelding, Kleur oudeKleur, int verschil, Kleur nieuweKleur)
            {
                var pixels = afbeelding.LaadArgb32Pixels(afbeelding.Grenzen);
                var lengte = pixels.Lengte;

                var oudeRood = oudeKleur.R;
                var oudeGroen = oudeKleur.G;
                var oudeBlauw = oudeKleur.B;
                var nieuweKleurWaarde = nieuweKleur.ToArgb();

                for (int i = 0; i < lengte; i++)
                {
                    // Rood
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Groen
                    var g = (byte)((pixels[i] >> 8) & 0xff);
                    // Blauw
                    var b = (byte)(pixels[i] & 0xff);

                    int werkelijkVerschil = Math.Abs(r - oudeRood) + Math.Abs(g - oudeGroen) + Math.Abs(b - oudeBlauw);

                    if (werkelijkVerschil <= verschil)
                    {
                        pixels[i] = nieuweKleurWaarde;
                    }
                }

                afbeelding.OpslaanArgb32Pixels(afbeelding.Grenzen, pixels);
            }

            Laag Laag2 = null;
            Laag Laag3 = null;
            using (PsdAfbeelding afbeelding = (PsdAfbeelding)Afbeelding.Laden(PSDBestand))
            {
                #region Toevoegen van Laag 1

                using (var stroom = new Bestandsstroom(laag1Bestand, BestandsModus.Openen))
                {
                    Laag2 = new Laag(stroom);

                    Laag2.FormaatWijzigen(afbeelding.Breedte, afbeelding.Hoogte);
                    var breedte = Laag2.Breedte;
                    var hoogte = Laag2.Hoogte;

                    Laag2.Links = 675;
                    Laag2.Boven = 0;

                    Laag2.Rechts = Laag2.Links + breedte;
                    Laag2.Onder = Laag2.Boven + hoogte;

                    afbeelding.LaagToevoegen(Laag2);
                }

                #endregion

                using (var stroom = new Bestandsstroom(laag2Bestand, BestandsModus.Openen))
                {
                    Laag3 = new Laag(stroom);
                    // Vervangen van witte kleur door transparant
                    VervangKleur(Laag3, Kleur.Wit, 256, Kleur.Transparant);
                    Laag2.AfbeeldingTekenen(new Punt(0, 0), Laag3);
                }

                afbeelding.Opslaan(uitvoerBestandsnaam, new PsdOpties());
            }
{{< /highlight >}}

**PSDNET-955. Niet ondersteund van compressiemethoden ZipWithPrediction voor 8bit**

{{< highlight csharp >}}
            string inputBestandsnaam = "zipTest698.psd";
            string uitvoerZip8 = "uit_Zip8bit.psd";
            string uitvoerZip16 = "uit_Zip16bit.psd";

            using (PsdAfbeelding afbeelding = (PsdAfbeelding)Afbeelding.Laden(inputBestandsnaam))
            {
                afbeelding.Opslaan(uitvoerZip8, new PsdOpties() { CompressieMethode = CompressieMethode.ZipWithPrediction, KanaalBitstelling = 8 });
                afbeelding.Opslaan(uitvoerZip16, new PsdOpties() { CompressieMethode = CompressieMethode.ZipWithPrediction, KanaalBitstelling = 16 });
            }
{{< /highlight >}}

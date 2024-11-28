---
title: Aspose.PSD voor .NET 19.12 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-net-19-12-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-11|[Ondersteuning van gekoppelde laag](/psd/nl/net/working-with-layers/#workingwithlayer-ondersteuningvangekoppelde-lagen)|Functie|
|PSDNET-131|[Ondersteuning van SoCoResource](/psd/nl/net/support-of-socoresource/)|Functie|
|PSDNET-115|LineBreaks worden toegevoegd aan bestaande LineBreaks als TextLayer wordt bijgewerkt met een string|Fout|
|PSDNET-157|Opslaan van PSB als PNG bevriest|Fout|
|PSDNET-250|Uitzondering bij het laden van CMYK PSD-bestand zonder lagen met RLE-compressie|Fout|
|PSDNET-161|Uitzondering bij het bijwerken van tekstlagen|Fout|
|PSDNET-222|Formaat van sommige PSD-bestanden met laagmaskers wordt incorrect gewijzigd|Fout|
|PSDNET-244|Opslaan van PSD met sommige Globalization.CultureInfo.CurrentCulture leidt tot uitzonderingen bij het laden|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Verwijderde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Gebruik voorbeelden:**
**PSDNET-11. Ondersteuning van gekoppelde laag**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("voorbeeld.psd"))

            {

                Layer[] lagen = psd.Layers;

                // koppel alle lagen in één gekoppelde groep

                short lagenLinkGroupId = psd.LinkedLayersManager.LinkLayers(lagen);

                // krijg id voor één laag

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(lagen[0]);

                if (lagenLinkGroupId != linkGroupId)

                {

                    throw new Exception("lagenLinkGroupId en linkGroupId zijn niet gelijk.");

                }

                // krijg alle gekoppelde lagen op basis van groeps-ID.

                Layer[] gekoppeldeLagen = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // ontkoppel elke laag uit de groep

                foreach (var gekoppeldeLaag in gekoppeldeLagen)

                {

                    psd.LinkedLayersManager.UnlinkLayer(gekoppeldeLaag);

                }

                // haalt NULL op voor een groeps-ID die geen lagen in de groep heeft.

                gekoppeldeLagen = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (gekoppeldeLagen != null)

                {

                    throw new Exception("Het veld gekoppeldeLagen is niet NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Ondersteuning van SoCoResource**

{{< highlight java >}}

      // Ondersteuning van SoCoResource

    string bronBestandsNaam = "ColorFillLayer.psd";

    string exportPad = "SoCoResource_Bewerkt.psd";

    var afbeelding = (PsdImage)Image.Load(bronBestandsNaam);

    using (afbeelding)

    {

        foreach (var laag in afbeelding.Layers)

        {

            if (laag is FillLayer)

            {

                var vulLaag = (FillLayer)laag;

                foreach (var resource in vulLaag.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            afbeelding.Save(exportPad);

        }

    }

{{< /highlight >}}

**PSDNET-115. LineBreaks worden toegevoegd aan bestaande LineBreaks als TextLayer wordt bijgewerkt met een string**

{{< highlight java >}}

           const string NieuweTekst = "abcdef\rzxcvbn";

        string bronBestandsPad = "TestBestandVoorAziatischeTekens.psd");

        string uitvoerBestandsPad = "resultaat.psd";

        using (var afbeelding = (PsdImage)Image.Load(bronBestandsPad))

        {

            var laag = (TextLayer)afbeelding.Layers[0];

            var afbeeldingOpties = new PsdOptions(afbeelding);

            laag.UpdateText(NieuweTekst);

            afbeelding.Save(uitvoerBestandsPad, afbeeldingOpties);

        }

        using (var gecreëerdeAfbeelding = (PsdImage)Image.Load(uitvoerBestandsPad))

        {

            var gemaaktLaag = (TextLayer)gecreëerdeAfbeelding.Layers[0];

            if (NieuweTekst != gemaaktLaag.Tekst)

            {

                throw new InvalidDataException("Bijgewerkte tekst is ongeldig");

            }

        }

{{< /highlight >}}

**PSDNET-157. Opslaan van PSB als PNG bevriest**

{{< highlight java >}}

       // Opslaan van PSB als PNG 

    string bronBestandsNaam = "voorbeeld.psb";

    string uitBestandsNaam = "voorbeeld.png";

    using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsNaam))

    {

        PngOptions opties = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        afbeelding.Save(uitBestandsNaam, opties);

    }

{{< /highlight >}}



` `**PSDNET-250. Uitzondering bij laden van CMYK PSD-bestand zonder laag met RLE-compressie**

{{< highlight java >}}

     void LaadRuweGegevensUitPsd()

        {

            string bronPad = "CmykMetAlpha.psd";

            using (RasterImage afbeelding = (RasterImage)Image.Load(bronPad))

            {

                var ruweGegevensInstellingen = afbeelding.RuweGegevensInstellingen;

                RawDataTester lader = new RawDataTester();

                afbeelding.LoadRawData(afbeelding.Grenzen, ruweGegevensInstellingen, lader);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rechthoek, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rechthoek, byte[] pixels, Point start, Point end, LaadOpties laadOpties)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Uitzondering bij bijwerken van tekstlagen**

{{< highlight java >}}

      // Laad een PSD-bestand als afbeelding en cast het naar PsdImage

    using (PsdImage psdAfbeelding = (PsdImage)Image.Load("voorbeeld.psd"))

    {

        foreach (var laag in psdAfbeelding.Layers)

        {

            if (laag is TextLayer)

            {

                TextLayer tekstLaag = laag as TextLayer;

                tekstLaag.UpdateTekst("test bijwerken", new Point(0, 0), 15.0f, Color.Paars);

            }

        }

        psdAfbeelding.Save("BijwerkenTekstLaagInPSD-bestand_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. Formaat van sommige PSD-bestanden met laagmaskers werkt niet correct**

{{< highlight java >}}

     int schaal = 2;

        string[] namen = {

                             "EenRegelmatigEnEenAanpassingMetVectorEnLaagMasker",

                             "LevelsLaagMetLaagMaskerRgb",

                             "LevelsLaagMetLaagMaskerCmyk",

                             "KleurBalansAanpassingslaag"

                         };

        for (int i = 0; i < namen.Length; i++)

        {

            string bronBestandsPad = namen[i] + ".psd";

            string uitvoerBestandsPad = "uitvoer_" + bronBestandsPad;

            string outputPngBestandsPad = "uitvoer_" + namen[i] + ".png";

            var psdLaadOpties = new PsdLoadOptions() { LaadEffectenResource = true };

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsPad, psdLaadOpties))

            {

                afbeelding.FormaatWijzigen(afbeelding.Breedte * schaal, afbeelding.Hoogte * schaal);

                afbeelding.Save(uitvoerBestandsPad, new PsdOptions());

                afbeelding.Save(outputPngBestandsPad, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. Opslaan van PSD met sommige Globalization.CultureInfo.CurrentCulture leidt tot uitzonderingen bij laden**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string bronBestandsNaam = string.Format("voorbeeld-{0}.psd", i);

            var psdLaadOpties = new PsdLoadOptions() { LaadEffectenResource = true };

            var psdOpslaanOpties = new PsdOptions();

            var cultuur = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultuur;

            System.Threading.Thread.CurrentThread.CurrentUICultuur = cultuur;

            string uitvoerBestandsNaam = "output-" + bronBestandsNaam;

            // Laad een PSD-bestand als afbeelding en cast het naar PsdImage

            using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestandsNaam, psdLaadOpties))

            {

                afbeelding.FormaatWijzigen(160, 120);

                afbeelding.Save(uitvoerBestandsNaam, psdOpslaanOpties);

            }

            cultuur = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = cultuur;

            System.Threading.Thread.CurrentThread.CurrentUICultuur = cultuur;

            // Laad een PSD-bestand als afbeelding en cast het naar PsdImage

            using (PsdImage afbeelding2 = (PsdImage)Image.Load(bronBestandsNaam, psdLaadOpties))

            {

                afbeelding2.FormaatWijzigen(160, 120);

                afbeelding2.Save(uitvoerBestandsNaam, psdOpslaanOpties);

            }

        }

{{< /highlight >}}
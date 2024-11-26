---
title: Aspose.PSD voor .NET 23.7 - Release-opmerkingen
type: docs
weight: 60
url: /nl/net/aspose-psd-voor-net-23-7-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                              | **Categorie** |
|:--------------|:-------------------------------------------------------------|:-------------|
| PSDNET-802    | Mogelijkheid toegevoegd om elke laag van PSD-bestand te exporteren naar geanimeerd Gif-bestand | Functie       |
| PSDNET-1441   | Toewijzen van Vullingseigenschap van vormlaag uit vscg-bron  | Functie       |
| PSDNET-1534   | Toevoegen van nieuwe warp-types (boog & boog)                | Functie       |
| PSDNET-1543   | Verander de toepassing die het PSD-bestand opslaat naar Aspose.PSD als UpdateMetadata-eigenschap is ingesteld op true | Functie       |
| PSDNET-1567   | Vergroten van het berekeningsgebied van het warp-beeld       | Functie       |
| PSDNET-1471   | Aanpassingslaag Zwart en wit verwerkt semi-transparantie verkeerd | Fout         |
| PSDNET-1505   | SmartObject ReplaceContents (wanneer de optie AllowWarpRepaint actief is) valt na 2 minuten berekenen | Fout         |
| PSDNET-1585   | Mogelijkheid toegevoegd om de echte positie van LayerGroup links en bovenaan te verkrijgen | Fout         |
| PSDNET-1589   | Formaat van de laag werkt verkeerd wanneer psd-bestand VogkResource heeft met structuren in punten | Fout         |
| PSDNET-1608   | TextBound werkt niet zoals verwacht                          | Fout         |
| PSDNET-1612   | Toevoegen van een laag gemaakt met standaardconstructor naar PSD-beeld voegt geen standaardresources eraan toe | Fout         |
| PSDNET-1623   | Timeline.LoopesCount wordt genegeerd bij exporteren naar geanimeerd GIF | Fout         |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Verwijderde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Gebruik voorbeelden:**

**PSDNET-802. Mogelijkheid toegevoegd om elke laag van PSD-bestand te exporteren naar geanimeerd GIF-bestand**

{{< highlight csharp >}}
string src = "ElkeLaagIsFrame.psd";
string outputGif = "uit_ElkeLaagIsFrame.gif";
string outputPsd = "uit_ElkeLaagIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Frames maken voor elke laag.
    int framesTellen = psdImage.Layers.Length;
    var tijdlijn = psdImage.Tijdlijn;

    Frame[] frames = nieuwe Frame[framesTellen];
    for (int i = 0; i < framesTellen; i++)
    {
        frames[i] = nieuwe Frame();
        LayerState[] laagStatens = nieuwe LayerState[framesTellen];

        for (int j = 0; j < framesTellen; j++)
        {
            laagStatens[j] = nieuwe LayerState();
            laagStatens[j].Ingeschakeld = i == j;
        }

        frames[i].LayerStates = laagStatens;
    }

    tijdlijn.Frames = frames;

    // Huidige staten bijwerken
    Layer[] lagen = psdImage.Lagen;
    LayerState[] staten = tijdlijn.Frames[tijdlijn.ActiefFrameIndex].LaagStatens;
    voor (int i = 0; i < framesTellen; i++)
    {
        lagen[i].IsZichtbaar = staten[i].Ingeschakeld;
    }

    tijdlijn.Save(outputGif, nieuwe GifOpties());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Toewijzen van Vullingseigenschap van vormlaag uit vscg-bron**

{{< highlight csharp >}}
string srcBestand = "ShapeInternalSolid.psd";
string uitBestand = "ShapeInternalSolid.psd.uit.psd";

using (PsdImage afbeelding = (PsdImage)Image.Load(
    srcBestand,
    nieuwe PsdLaadOpties { LaadEffectenBron = true }))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Lagen[1];
    ColorFillSettings vullingInstellingen = (ColorFillSettings)vormLaag.Vulling;
    vullingInstellingen.Kleur = Color.Rood;

    vormLaag.Update();

    afbeelding.Save(uitBestand);
}

// Controleer opgeslagen wijzigingen
gebruik (PsdAfbeelding afbeelding = (PsdAfbeelding)Image.Load(
    uitBestand,
    nieuwe PsdLaadOpties { LaadEffectenBron = true }))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Lagen[1];
    ColorFillSettings vullingInstellingen = (ColorFillSettings)vormLaag.Vulling;

    AssertGelijk(Color.Rood, vullingInstellingen.Kleur);

    afbeelding.Save(uitBestand);
}

void AssertGelijk(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw nieuwe Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Aanpassingslaag Zwart en wit verwerkt semi-transparantie verkeerd**

{{< highlight csharp >}}
string srcBestand = "kikker_nosymb.psd";
string uitBestand = "kikker_nosymb.psd.uit.psd";

using (PsdAfbeelding psdAfbeelding = (PsdAfbeelding)Image.Load(srcBestand))
{
    psdAfbeelding.AddBlackWhiteAdjustmentLayer();
    psdAfbeelding.Save(uitBestand);
}

// Controleer opgeslagen wijzigingen
gebruik (PsdAfbeelding afbeelding = (PsdAfbeelding)Image.Load(
    uitBestand,
    nieuwe PsdLaadOpties { LaadEffectenBron = true }))
{
    AssertGelijk(2, afbeelding.Lagen.Lengte);

    BlackWhiteAdjustmentLayer zwartWitAanpassingslaag = (BlackWhiteAdjustmentLayer)afbeelding.Lagen[1];

    als (zwartWitAanpassingslaag == null)
    {
        throw nieuwe Exception("Laag 2 moet BlackWhiteAdjustmentLayer zijn");
    }

    afbeelding.Save(uitBestand);
}

void AssertGelijk(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw nieuwe Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1505. SmartObject ReplaceContents (wanneer de optie AllowWarpRepaint actief is) valt na 2 minuten berekenen**

{{< highlight csharp >}}
string bronBestand = "mok 4.psd";
string wijzigingsbestand = "kunstwerk voor vervanging.png";
string uitvoerBestand = "export.png";

int nieuweHoogte = 300;

gebruik (var psdAfbeelding = (PsdAfbeelding)Image.Load(bronBestand, nieuwe PsdLaadOpties() { ToestaanWarpRepaint = true, LaadEffectenBron = true }))
{
    SmartObjectLayer slimObjectLaag = (SmartObjectLayer)psdAfbeelding.Lagen[3];

    var schaal = (double)nieuweHoogte / slimObjectLaag.Hoogte;
    var nieuweBreedte = (int)Math.Round(slimObjectLaag.Breedte * schaal);

    PsdAfbeelding binnenAfbeelding = nieuwe PsdAfbeelding(nieuweBreedte, nieuweHoogte);
    binnenAfbeelding.SetResolutie(72, 72);

    Stream binnenStroom = nieuwe FileStream(wijzigingsbestand, FileMode.Open);
    Laag laag = nieuwe Laag(binnenStroom) { HorizontaleResolutie = 72, VerticaleResolutie = 72 };
    probeer
    {
        binnenAfbeelding.AddLayer(laag);

        slimObjectLaag.ReplaceContents(binnenAfbeelding);
        slimObjectLaag.UpdateGewijzigdeInhoud();

        psdAfbeelding.Save(uitvoerBestand, nieuwe PngOpties
        {
            Kleurtype = PngKleurtype.WerkelijkeKleurMetAlfa
        });
    }
    eindelijk
    {
        binnenAfbeelding.Dispose();
        binnenStroom.Dispose();
        laag.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Toevoegen van nieuwe warp-types (boog & boog)**

{{< highlight csharp >}}
string bronArcBestand = "boog_warp.psd";
string uitvoerArcBestand = "boog_export.png";

string bronArchBestand = "arch_warp.psd";
string uitvoerArchBestand = "arch_export.png";

gebruik (var psdAfbeelding = (PsdAfbeelding)Image.Load(bronArcBestand, nieuwe PsdLaadOpties() { ToestaanWarpRepaint = true, LaadEffectenBron = true }))
{
    psdAfbeelding.Save(uitvoerArcBestand, nieuwe PngOpties
    {
        Kleurtype = PngKleurtype.WerkelijkeKleurMetAlfa
    });
}

gebruik (var psdAfbeelding = (PsdAfbeelding)Image.Load(bronArchBestand, nieuwe PsdLaadOpties() { ToestaanWarpRepaint = true, LaadEffectenBron = true }))
{
    psdAfbeelding.Save(uitvoerArchBestand, nieuwe PngOpties
    {
        Kleurtype = PngKleurtype.WerkelijkeKleurMetAlfa
    });
}
{{< /highlight >}}

**PSDNET-1543. Verander de toepassing die het PSD-bestand opslaat naar Aspose.PSD als UpdateMetadata-eigenschap is ingesteld op true**

{{< highlight csharp >}}
string pad = "uitvoer.psd";
gebruik (var afbeelding = nieuwe PsdAfbeelding(100, 100))
{
    // Als je wilt dat de makerstool verandert, zorg ervoor dat de eigenschap "UpdateMetadata" is ingesteld op true. Standaard staat deze op true.
    var psdOpties = nieuwe PsdOpties();
    psdOpties.UpdateMetadata = true;

    // Afbeelding opslaan. 
    afbeelding.Save(pad, psdOpties);

    // Makerstool controleren in code.
    var xmpGegevens = afbeelding.XmpGegevens;
    var basisPakket = afbeelding.XmpGegevens.PakketOphalen(Namespaces.XmpBasic);

    // Hier zal de bijgewerkte makerstoolinfo zijn.
    var huidigeMakerstool = (string)basisPakket[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Vergroten van het berekeningsgebied van het warp-beeld**

{{< highlight csharp >}}
string bronBestand = "mok4_warp.psd";
string uitvoerBestand = "mok4_export.png";

gebruik (var psdAfbeelding = (PsdAfbeelding)Image.Load(bronBestand, nieuwe PsdLaadOpties() { ToestaanWarpRepaint = true, LaadEffectenBron = true }))
{
    psdAfbeelding.Save(uitvoerBestand, nieuwe PngOpties
    {
        Kleurtype = PngKleurtype.WerkelijkeKleurMetAlfa
    });
}
{{< /highlight >}}

**PSDNET-1585. Mogelijkheid toegevoegd om de echte positie van LayerGroup links en bovenaan te verkrijgen**

{{< highlight csharp >}}
string bronBestand = "LaagGroepFiguren.psd";

void AssertGelijk(object verwacht, object werkelijk)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw nieuwe Exception("Objecten zijn niet gelijk.");
    }
}

gebruik (var afbeelding = (PsdAfbeelding)Image.Load(bronBestand))
{
    var lagen = afbeelding.Lagen;

    voor (int i = 0; i < lagen.Lengte; i++)
    {
        var laag = lagen[i];

        als (laag is LaagGroep)
        {
            // LaagGroep ophalen.
            var groep = (LaagGroep)laag;

            var verwachteLinks = int.MaxValue;
            var verwachteBoven = int.MaxValue;
            var verwachteRechts = 0;
            var verwachteOnder = 0;

            // Echte positie van links, boven, rechts en onder berekenen.
            voor elk (var innerLaag in groep.Lagen)
            {
                als (innerLaag is Aanpassingslaag || innerLaag.Grens.Leeg)
                {
                    doorgaan;
                }

                verwachteLinks = Math.Min(verwachteLinks, innerLaag.Links);
                verwachteBoven = Math.Min(verwachteBoven, innerLaag.Boven);
                verwachteRechts = Math.Max((verwachteLinks + groep.Breedte), (innerLaag.Links + innerLaag.Breedte));
                verwachteOnder = Math.Max((verwachteBoven + groep.Hoogte), (innerLaag.Boven + innerLaag.Hoogte));
            }

            // Posities van LaagGroep links, boven, rechts en onder zijn nu correct berekend.
            AssertGelijk(groep.Links, verwachteLinks);
            AssertGelijk(groep.Boven, verwachteBoven);
            AssertGelijk(groep.Rechts, verwachteRechts);
            AssertGelijk(groep.Onder, verwachteOnder);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Formaat van de laag werkt verkeerd wanneer psd-bestand VogkResource heeft met structuren in punten**

{{< highlight csharp >}}
string[] bronBestanden = nieuwe string[]
{
    "PointsVectorOrigin.psd",
    "TopVogkResStruct.psd"
};

voor elke (string bronBestand in bronBestanden)
{
    gebruik (PsdAfbeelding afbeelding = (PsdAfbeelding)Image.Load(bronBestand))
    {
        Laag laag = afbeelding.Lagen[0];

        laag.GrootteWijzigen(50, 50);

        AssertGelijk(laag.Hoogte, 50);
        AssertGelijk(laag.Breedte, 50);
    }
}

void AssertGelijk(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw nieuwe Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound werkt niet zoals verwacht**

{{< highlight csharp >}}
string bronBestand = "input_Test_forTicket.psd";
string uitBestand = "uit_1608.psd";

Grootte nieuweTekstvak = nieuwe Grootte(-1, -1);
gebruik (PsdAfbeelding psdAfbeelding = (PsdAfbeelding)Aspose.PSD.Afbeelding.Load(bronBestand))
{
    //Stap: Tekst vervangen
    TekstLaag tekstLaag = (TekstLaag)psdAfbeelding.Lagen[3];
    tekstLaag.TekstGegevens.Items[0].Tekst = "Teksttest vervangen";

    //Stap: TekstBoundBox bijwerken
    tekstLaag.TekstGegevens.UpdateLaagGegevens();
    nieuweTekstvak = nieuwe Grootte((int)Math.Ceiling(tekstLaag.TekstBoundBox.Breedte), tekstLaag.Hoogte);

    tekstLaag.TekstBoundBox = nieuwe Aspose.PSD.VierkanteF(PointF.Empty, nieuweTekstvak);
    tekstLaag.TekstGegevens.UpdateLaagGegevens();

    psdAfbeelding.Save(uitBestand);
}

// Controleer wijzigingen
gebruik (var psdAfbeelding = (PsdAfbeelding
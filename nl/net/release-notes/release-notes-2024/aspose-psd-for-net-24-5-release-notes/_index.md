---
title: Aspose.PSD voor .NET 24.5 - Release-opmerkingen
type: docs
weight: 80
url: /nl/net/aspose-psd-voor-net-24-5-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                      | **Categorie** |
|:--------------|:--------------------------------------------------------------------------------------|:--------------|
| PSDNET-1897   | [AI-indeling] Ondersteuning toegevoegd voor het verwerken van AI-bestanden met EPSF-koptekst | Functie    |
| PSDNET-1755   | Halfdoorzichtigheid wordt verkeerd verwerkt bij de voorbeeldweergave van het psd-bestand  | Fout  |
| PSDNET-1942   | Renderng van vormlaag gedeeltelijk onjuist                                             | Fout  |
| PSDNET-1957   | Uitzondering bij het opslaan van PSD-bestanden met een grootte groter dan 200 MB en grote afmetingen | Fout  |
| PSDNET-1998   | Fout bij het opslaan van afbeelding uitzondering bij opslaan naar PDF na update van 23.7 naar 24.3 | Fout  |
| PSDNET-2033   | Probleem in de methode GetFontInfoRecords oplossen voor de Chinese lettertypen         | Fout  |

## **Wijzigingen in openbare API** 
# **Toegevoegde API's:**
- P:Aspose.PSD.Afbeeldingsopties.PsdOpties.AchtergrondInhoud
- P:Aspose.PSD.Bestandsindelingen.Ai.AiLaagSectie.HeeftMeerdereLaagmaskers
- P:Aspose.PSD.Bestandsindelingen.Ai.AiLaagSectie.KleurIndex

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1755. Halfdoorzichtigheid wordt verkeerd verwerkt bij de voorbeeldweergave van het psd-bestand**

{{< highlight csharp >}}
// Halfdoorzichtigheid wordt verkeerd verwerkt bij de voorbeeldweergave van het psd-bestand.
// AchtergrondInhoud toegewezen aan Wit. Transparante gebieden moeten een witte kleur hebben.

string bronBestand = Path.Combine(basisMap, "frog_nosymb.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdAfbeelding = (PsdImage)Afbeelding.Laden(bronBestand))
{
    RawColor achtergrondKleur = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbWaarde = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    achtergrondKleur.StelInAlsInt(argbWaarde); // Wit

    PsdOpties psdOpties = new PsdOpties(psdAfbeelding)
    {
        KleurenModus = KleurModi.Rgb,
        CompressieMethode = CompressieMethode.RLE,
        AantalKanalen = 4,
        AchtergrondInhoud = achtergrondKleur,
    };

    psdAfbeelding.Opslaan(uitvoerBestand, psdOpties);
}
{{< /highlight >}}

**PSDNET-1897. [AI-indeling] Ondersteuning toegevoegd voor het verwerken van AI-bestanden met EPSF-koptekst**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "voorbeeld.ai");
string uitvoerBestandPad = Path.Combine(uitvoerMap, "voorbeeld.png");

void AssertAreEqual(object verwacht, object werkelijk)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception("Objecten zijn niet gelijk.");
    }
}

using (AiAfbeelding afbeelding = (AiAfbeelding)Afbeelding.Laden(bronBestand))
{
    AssertAreEqual(afbeelding.Lagen.Lengte, 2);
    AssertAreEqual(afbeelding.Lagen[0].HeeftMeerdereLaagmaskers, false);
    AssertAreEqual(afbeelding.Lagen[0].KleurIndex, -1);
    AssertAreEqual(afbeelding.Lagen[1].HeeftMeerdereLaagmaskers, false);
    AssertAreEqual(afbeelding.Lagen[1].KleurIndex, -1);

    afbeelding.Opslaan(uitvoerBestandPad, new PngOpties());
}
{{< /highlight >}}

**PSDNET-1942. Renderng van vormlaag gedeeltelijk onjuist**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "ShapeLayerTest.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "ShapeLayerTest_output.psd");
const int ImgTotPsdRatio = 256 * 65535;

using (var im = (PsdImage)Afbeelding.Laden(bronBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)im.Lagen[2];
    IPath pad = vormLaag.Pad;
    IPathShape[] padVormen = pad.GetItems();
    List<BezierKnotRecord> knopenLijst = new List<BezierKnotRecord>();
    foreach (IPathShape padVorm in padVormen)
    {
        BezierKnotRecord[] knopen = padVorm.GetItems();
        knopenLijst.AddRange(knopen);
    }

    // Laageigenschappen wijzigen
    var nieuweVorm = new PathShape();

    BezierKnotRecord[] bezierKnopen = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsGelinkt = true,
            Punten = new Point[3]
            {
                PointFNaarResourcePunt(
                    new PointF(100, 100),
                    vormLaag.Container.Grootte),
                PointFNaarResourcePunt(
                    new PointF(100, 100),
                    vormLaag.Container.Grootte),
                PointFNaarResourcePunt(
                    new PointF(100, 100),
                    vormLaag.Container.Grootte),
            },
        },
        new BezierKnotRecord()
        {
            IsGelinkt = true,
            Punten = new Point[3]
            {
                PointFNaarResourcePunt(
                    new PointF(50, 490),
                    vormLaag.Container.Grootte),
                PointFNaarResourcePunt(
                    new PointF(100, 490),
                    vormLaag.Container.Grootte), // Ankerpunt
                PointFNaarResourcePunt(
                    new PointF(150, 490),
                    vormLaag.Container.Grootte),
            },
        },
        new BezierKnotRecord()
        {
            IsGelinkt = true,
            Punten = new Point[3]
            {
                PointFNaarResourcePunt(
                    new PointF(490, 150),
                    vormLaag.Container.Grootte),
                PointFNaarResourcePunt(
                    new PointF(490, 50),
                    vormLaag.Container.Grootte),
                PointFNaarResourcePunt(
                    new PointF(490, 20),
                    vormLaag.Container.Grootte),
            },
        },
    };

    nieuweVorm.SetItems(bezierKnopen);

    List<IPathShape> nieuweVormen = new List<IPathShape>(padVormen);
    nieuweVormen.Add(nieuweVorm);

    IPathShape[] padVormNieuw = nieuweVormen.ToArray();
    pad.SetItems(padVormNieuw);

    vormLaag.Bijwerken();

    im.Opslaan(uitvoerBestand, new PsdOpties());
}

using (var im = (PsdImage)Afbeelding.Laden(uitvoerBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)im.Lagen[2];
    IPath pad = vormLaag.Pad;
    IPathShape[] padVormen = pad.GetItems();
    List<BezierKnotRecord> knopenLijst = new List<BezierKnotRecord>();
    foreach (IPathShape padVorm in padVormen)
    {
        BezierKnotRecord[] knopen = padVorm.GetItems();
        knopenLijst.AddRange(knopen);
    }

    AssertAreEqual(3, padVormen.Lengte);
    AssertAreEqual(42, vormLaag.Links);
    AssertAreEqual(14, vormLaag.Boven);
    AssertAreEqual(1600, vormLaag.Grenzen.Breedte);
    AssertAreEqual(1086, vormLaag.Grenzen.Hoogte);
}

Point PointFNaarResourcePunt(PointF punt, Grootte afbeeldingsGrootte)
{
    return new Point(
        (int)Math.Round(punt.Y * (ImgTotPsdRatio / afbeeldingsGrootte.Hoogte)),
        (int)Math.Round(punt.X * (ImgTotPsdRatio / afbeeldingsGrootte.Breedte)));
}

void AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1957. Uitzondering bij het opslaan van PSD-bestanden met een grootte groter dan 200 MB en grote afmetingen**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "grootbestand.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "output_raw.psd");

PsdOpties laadOpties = new PsdOpties()
{
    LaadEffectenBron = true,
    GebruikSchijfVoorLaadEffectenBron = true
};

using (var psdAfbeelding = (PsdAfbeelding)Afbeelding.Laden(bronBestand, laadOpties))
{
    // Er zou hier geen fout mogen zijn
    psdAfbeelding.Opslaan(uitvoerBestand, new PsdOpties { CompressieMethode = CompressieMethode.RLE });
}
{{< /highlight >}}

**PSDNET-1998. Fout bij het opslaan van afbeelding uitzondering bij opslaan naar PDF na update van 23.7 naar 24.3**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "CVFlor.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "_export.pdf");

using (var psdAfbeelding = (PsdAfbeelding)Afbeelding.Laden(bronBestand))
{
    PdfOpties opslaanOpties = new PdfOpties();
    opslaanOpties.PdfKernOpties = new PdfKernOpties();

    psdAfbeelding.Opslaan(uitvoerBestand, opslaanOpties);
}
{{< /highlight >}}

**PSDNET-2033. Probleem in de methode GetFontInfoRecords oplossen voor de Chinese lettertypen**

{{< highlight csharp >}}
var lettertypeMap = Path.Combine(basisMap, "Lettertype");
string bronBestand = Path.Combine(basisMap, "bd-worlds-best-pink.psd");

PsdOpties psdLaadOpties = new PsdOpties();
psdLaadOpties.LaadEffectenBron = true;
psdLaadOpties.ToestaanWarpRepaint = true;
try
{
    FontInstellingen.SetLettertypeMappen(new string[] { lettertypeMap }, true);
    FontInstellingen.WerkLettertypenBij();

    using (PsdAfbeelding afbeelding = (PsdAfbeelding)PsdAfbeelding.Laden(bronBestand, psdLaadOpties))
    {
        foreach (var laag in afbeelding.Lagen)
        {
            var tekstLaag = laag as TekstLaag;

            if (tekstLaag != null)
            {
                if (tekstLaag.Tekst == "best")
                {
                    // Zonder deze correctie zal hier een uitzondering zijn vanwege het Chinese lettertype.
                    tekstLaag.WerkTekstBij("SUСCESS");
                }
            }
        }
    }
}
finally
{
    FontInstellingen.Reset();
    FontInstellingen.WerkLettertypenBij();
}
{{< /highlight >}}

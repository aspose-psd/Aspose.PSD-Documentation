---
title: Aspose.PSD voor .NET 24.2 - Release-opmerkingen
type: docs
weight: 110
url: /nl/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat de release-opmerkingen voor [Aspose.PSD voor .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Samenvatting**                                                              | **Categorie** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Afhandeling van de eigenschap Angle voor PatternFillSettings                  |   Functie   |
| PSDNET-1719 | Ondersteuning van verticale en horizontale schaal voor TextLayer               |     Functie     |
| PSDNET-1783 | [AI-formaat] Implementeren van correcte weergave van achtergrond in op PDF gebaseerd AI-formaat |     Functie     |
| PSDNET-1611 | Wijzig mechanisme in warp voor vervorming                                     |     Verbetering     |
| PSDNET-1802 | Warp versnellen                                                               |     Verbetering     |
| PSDNET-995  | "Afbeelding laden mislukt." uitzondering bij openen document                    |     Fout     |
| PSDNET-1491 | Opslaan van psd-bestanden herstellen die Stroke Pattern hebben                 |     Fout     |
| PSDNET-1642 | De tekststijl is onjuist in een slim object wanneer we ReplaceContents gebruiken |     Fout     |
| PSDNET-1884 | [AI-formaat] Bezig met het oplossen van de Cubic Bezier-rendering bij AI-bestand |     Fout     |

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **Verwijderde API's:**
- Geen

## **Gebruikvoorbeelden:**

**PSDNET-1503. Afhandeling van eigenschap Angle voor PatternFillSettings**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "PatternFillLayerWide_0.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "PatternFillLayerWide_0_output.psd");

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer vulLaag = (FillLayer)afbeelding.Laag[1];
    PatternFillSettings vulInstellingen = (PatternFillSettings)vulLaag.FillSettings;
    vulInstellingen.Angle = 70;
    vulLaag.Update();
    afbeelding.Save(uitvoerBestand, new PsdOptions());
}

using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer vulLaag = (FillLayer)afbeelding.Laag[1];
    PatternFillSettings vulInstellingen = (PatternFillSettings)vulLaag.FillSettings;

    Assert.AreEqual(70, vulInstellingen.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Ondersteuning van verticale en horizontale schaal voor TextLayer**

{{< highlight csharp >}}
string bron = Path.Combine(basisMap, "1719_src.psd");
string uitvoer = Path.Combine(uitvoerMap, "out_1719.png");

using (var psdAfbeelding = (PsdImage)Image.Load(bron))
{
    psdAfbeelding.Save(uitvoer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [AI-formaat] Implementeer correcte weergave van achtergrond in op PDF gebaseerd AI-formaat**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "ananas.ai");
string uitvoerBestandPad = Path.Combine(uitvoerMap, "ananas.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand))
{
    afbeelding.Save(uitvoerBestandPad, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. "Afbeelding laden mislukt." uitzondering bij openen document**

{{< highlight csharp >}}
string bronBestand1 = Path.Combine(basisMap, "PRODUCT.ai");
string uitvoerBestand1 = Path.Combine(uitvoerMap, "PRODUCT.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand1))
{
    afbeelding.Save(uitvoerBestand1, new PngOptions());
}

string bronBestand2 = Path.Combine(basisMap, "Dolota.ai");
string uitvoerBestand2 = Path.Combine(uitvoerMap, "Dolota.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand2))
{
    afbeelding.Save(uitvoerBestand2, new PngOptions());
}

string bronBestand3 = Path.Combine(basisMap, "ARS_novelty_2108_out_01(1).ai");
string uitvoerBestand3 = Path.Combine(uitvoerMap, "ARS_novelty_2108_out_01(1).png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand3))
{
    afbeelding.Save(uitvoerBestand3, new PngOptions());
}

string bronBestand4 = Path.Combine(basisMap, "bit_gear.ai");
string uitvoerBestand4 = Path.Combine(uitvoerMap, "bit_gear.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand4))
{
    afbeelding.Save(uitvoerBestand4, new PngOptions());
}

string bronBestand5 = Path.Combine(basisMap, "test.ai");
string uitvoerBestand5 = Path.Combine(uitvoerMap, "test.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand5))
{
    afbeelding.Save(uitvoerBestand5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. Opslaan van psd-bestanden herstellen die Stroke Pattern hebben**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "StrokeShapePattern.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "StrokeShapePattern_output.psd");

Rechthoek nieuwePatternGrenzen = new Rechthoek(0, 0, 4, 4);
Guid uniekId = Guid.NewGuid();
string nieuwePatternNaam = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] nieuwPattern = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage afbeelding = (PsdImage)Image.Load(bronBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Lagen[1];
    PatternFillSettings strokeInterneVulInstellingen = (PatternFillSettings)vormLaag.Fill;

    PattResource pattResource;
    foreach (var globaleLaagResource in afbeelding.GlobaleLaagResources)
    {
        if (globaleLaagResource is PattResource)
        {
            pattResource = (PattResource)globaleLaagResource;
            PattResourceData patternItem = pattResource.Patterns[0]; // Interne slagpatroongegevens

            patternItem.PatternId = uniekId.ToString();
            patternItem.Name = nieuwePatternNaam;
            patternItem.SetPattern(nieuwPattern, nieuwePatternGrenzen);

            break;
        }
    }

    strokeInterneVulInstellingen.PatternName = nieuwePatternNaam;
    strokeInterneVulInstellingen.PatternId = uniekId.ToString() + "\0";

    vormLaag.Update();

    afbeelding.Save(uitvoerBestand);
}

// Controleer gewijzigde gegevens.
using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    ShapeLayer vormLaag = (ShapeLayer)afbeelding.Lagen[1];
    PatternFillSettings strokeInterneVulInstellingen = (PatternFillSettings)vormLaag.Fill;

    Assert.AreEqual(uniekId.ToString().ToUpper(), strokeInterneVulInstellingen.PatternId);
    Assert.AreEqual(nieuwePatternNaam, strokeInterneVulInstellingen.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. De tekststijl is incorrect in een slim object wanneer we ReplaceContents gebruiken**

{{< highlight csharp >}}
string invoerBestand = Path.Combine(basisMap, "bron.psd");
string uitvoer2 = Path.Combine(uitvoerMap, "uitvoer.png");

PsdLoadOptions psdLaadOpties = new PsdLoadOptions();
psdLaadOpties.LoadEffectsResource = true;

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(invoerBestand, psdLaadOpties))
{
    SmartObjectLayer slimObject = (SmartObjectLayer)psdAfbeelding.Lagen[1];

    using (PsdImage slimObjectAfbeelding = (PsdImage)slimObject.LoadContents(psdLaadOpties))
    {
        slimObject.ReplaceContents(slimObjectAfbeelding);
    }

    psdAfbeelding.Save(uitvoer2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [AI-formaat] Cubic Bezier-rendering in AI-bestand oplossen**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "Typography.ai");
string uitvoerBestandPad = Path.Combine(uitvoerMap, "Typography.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronBestand))
{
    afbeelding.Save(uitvoerBestandPad, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. Wijzig mechanisme voor vervorming in warp**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "crow_grid.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "export.png");

var opties = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(bronBestand, opties))
{
    img.Save(uitvoerBestand, new PngOptions() { CompressieNiveau = 9, KleurType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1802. Warp versnellen**

{{< highlight csharp >}}
string bronBestand = Path.Combine(basisMap, "output.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "export.png");

var opties = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var stopwatch = new Stopwatch();
stopwatch.Start();

using (PsdImage img = (PsdImage)Image.Load(bronBestand, opties))
{
    img.Save(uitvoerBestand, new PngOptions() { CompressieNiveau = 9, KleurType = PngColorType.TruecolorWithAlpha });
}

stopwatch.Stop();

// oude waarde = 193300
// nieuwe waarde = 55500
int tijdInSec = (int)stopwatch.Elapsed.TotalMilliseconds;
if (tijdInSec > 100000)
{
    throw new Exception("Procestijd is te lang");
}
{{< /highlight >}}

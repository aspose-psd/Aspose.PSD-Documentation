---
title: Aspose.PSD voor .NET 24.4 - Releasenotities
type: docs
weight: 90
url: /nl/net/aspose-psd-voor-net-24-4-releasenotities/
---

{{% alert color="primary" %}}

Deze pagina bevat releasenotities voor [Aspose.PSD voor .NET 24.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Samenvatting**                                      | **Categorie** |
|:------------|:------------------------------------------------------|:--------------|
| PSDNET-1871 | [AI-formaat] Toevoegen van XObjectForm-bronverwerking | Functie       |
| PSDNET-1961 | Toevoegen van Constructor voor de ShapeLayer          | Functie       |
| PSDNET-1879 | Oplossing voor conversie van Psd-bestand van RGB naar CMYK | Fout         |
| PSDNET-1966 | Specifiek PSD-bestand kan niet geëxporteerd worden met Aspose.PSD | Fout         |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**

**PSDNET-1871. [AI-formaat] Toevoegen van XObjectForm-bronverwerking**

{{< highlight csharp >}}
string bronbestand = Path.Combine(basisMap, "voorbeeld.ai");
string uitvoerBestandPad = Path.Combine(uitvoerMap, "voorbeeld.png");

using (AiImage afbeelding = (AiImage)Image.Load(bronbestand))
{
    afbeelding.Save(uitvoerBestandPad, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1879. Oplossing voor conversie van Psd-bestand van RGB naar CMYK**

{{< highlight csharp >}}
// Controleer of psd-bestand geconverteerd naar CMYK + RLE 4 kanalen van psd-bestand in RGB + RLE 4 kanalen, echt 4 kanalen heeft 
// en HasTransparencyData == false.

string bronbestand = Path.Combine(basisMap, "frog_nosymb.psd");
string uitvoerBestand = Path.Combine(uitvoerMap, "frog_nosymb_output.psd");

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(bronbestand))
{
    psdAfbeelding.HasTransparencyData = false;

    PsdOptions psdOpties = new PsdOptions(psdAfbeelding)
    {
        ColorMode = ColorModes.Cmyk,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
    };

    psdAfbeelding.Save(uitvoerBestand, psdOpties);
}

using (PsdImage psdAfbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    AssertAreEqual(false, psdAfbeelding.HasTransparencyData);
    AssertAreEqual((ushort)4, psdAfbeelding.Layers[0].ChannelsCount);
}

void AssertAreEqual(object verwacht, object daadwerkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, daadwerkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1961. Toevoegen van Constructor voor de ShapeLayer**

{{< highlight csharp >}}
string uitvoerBestand = Path.Combine(uitvoerMap, "AddShapeLayer_output.psd");

const int ImgToPsdRatio = 256 * 65535;

using (PsdImage nieuwPsd = new PsdImage(600, 400))
{
    ShapeLayer laag = nieuwPsd.AddShapeLayer();

    var nieuweVorm = GenereerNieuweVorm(nieuwPsd.Size);
    List<IPathShape> nieuweVormen = new List<IPathShape>();
    nieuweVormen.Add(nieuweVorm);
    laag.Path.SetItems(nieuweVormen.ToArray());

    laag.Update();

    nieuwPsd.Save(uitvoerBestand);
}

using (PsdImage afbeelding = (PsdImage)Image.Load(uitvoerBestand))
{
    AssertAreEqual(2, afbeelding.Layers.Length);

    ShapeLayer vormLaag = afbeelding.Layers[1] as ShapeLayer;
    ColorFillSettings interneVulling = vormLaag.Fill as ColorFillSettings;
    IStrokeSettings lijnstijlInstellingen = vormLaag.Stroke;
    ColorFillSettings lijnstijlVulling = vormLaag.Stroke.Fill as ColorFillSettings;

    AssertAreEqual(1, vormLaag.Path.GetItems().Length); // 1 Vorm
    AssertAreEqual(3, vormLaag.Path.GetItems()[0].GetItems().Length); // 3 knopen in een vorm

    AssertAreEqual(-16127182, interneVulling.Color.ToArgb()); // ff09eb32

    AssertAreEqual(7.41, lijnstijlInstellingen.Size);
    AssertAreEqual(false, lijnstijlInstellingen.Enabled);
    AssertAreEqual(StrokePosition.Center, lijnstijlInstellingen.LineAlignment);
    AssertAreEqual(LineCapType.ButtCap, lijnstijlInstellingen.LineCap);
    AssertAreEqual(LineJoinType.MiterJoin, lijnstijlInstellingen.LineJoin);
    AssertAreEqual(-16777216, lijnstijlVulling.Color.ToArgb()); // ff000000
}

PathShape GenereerNieuweVorm(Size afbeeldingsgrootte)
{
    var nieuweVorm = new PathShape();

    PointF punt1 = new PointF(20, 100);
    PointF punt2 = new PointF(200, 100);
    PointF punt3 = new PointF(300, 10);

    BezierKnotRecord[] BezierKnopen = new BezierKnotRecord[]
    {
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punt1, afbeeldingsgrootte),
                          PointFToResourcePoint(punt1, afbeeldingsgrootte),
                          PointFToResourcePoint(punt1, afbeeldingsgrootte),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punt2, afbeeldingsgrootte),
                          PointFToResourcePoint(punt2, afbeeldingsgrootte),
                          PointFToResourcePoint(punt2, afbeeldingsgrootte),
                      }
         },
         new BezierKnotRecord()
         {
             IsLinked = true,
             Points = new Point[3]
                      {
                          PointFToResourcePoint(punt3, afbeeldingsgrootte),
                          PointFToResourcePoint(punt3, afbeeldingsgrootte),
                          PointFToResourcePoint(punt3, afbeeldingsgrootte),
                      }
         },
    };

    nieuweVorm.SetItems(BezierKnopen);

    return nieuweVorm;
}

Point PointFToResourcePoint(PointF punt, Size afbeeldingsgrootte)
{
    return new Point(
        (int)Math.Round(punt.Y * (ImgToPsdRatio / afbeeldingsgrootte.Height)),
        (int)Math.Round(punt.X * (ImgToPsdRatio / afbeeldingsgrootte.Width)));
}

void AssertAreEqual(object verwacht, object daadwerkelijk, string bericht = null)
{
    if (!object.Equals(verwacht, daadwerkelijk))
    {
        throw new Exception(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1966. Specifiek PSD-bestand kan niet geëxporteerd worden met Aspose.PSD**

{{< highlight csharp >}}
string bronbestand = Path.Combine(basisMap, "1966source.psd");
string uitvoerPng = Path.Combine(uitvoerMap, "output.png");

using (var psdAfbeelding = (PsdAfbeelding)Image.Load(bronbestand, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    psdAfbeelding.Save(uitvoerPng, new PngOptions());
}
{{< /highlight >}}

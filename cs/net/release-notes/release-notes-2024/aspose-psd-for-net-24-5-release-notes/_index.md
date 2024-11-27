---
title: Aspose.PSD pro .NET 24.5 - poznámky k vydání
type: docs
weight: 80
url: /cs/net/aspose-psd-pro-net-24-5-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                          | **Kategorie** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [Formát AI] Přidána podpora pro zpracování souborů AI s hlavičkou EPSF                | Funkce      |
| PSDNET-1755 | Poloprůhlednost je špatně zpracována ve náhledu souboru PSD                          | Chyba      |
| PSDNET-1942 | Částečně nesprávné vykreslování vrstvy tvaru                                          | Chyba      |
| PSDNET-1957 | Výjimka při ukládání souborů PSD s velikostí více než 200 MB a velkými rozměry       | Chyba      |
| PSDNET-1998 | Výjimka při ukládání obrázku při ukládání do formátu PDF po aktualizaci z 23.7 na 24.3 | Chyba      |
| PSDNET-2033 | Oprava problému ve třídě metody GetFontInfoRecords pro čínské písma                  | Chyba      |

## **Veřejné změny API**
# **Přidané API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **Odstraněná API:**
- Žádné

## **Příklady použití:**

**PSDNET-1755. Poloprůhlednost je špatně zpracována ve náhledu souboru PSD**

{{< highlight csharp >}}
// Poloprůhlednost je špatně zpracována ve náhledu souboru PSD.
// BackgroundContents nastaven na bílou barvu. Průhledné oblasti by měly mít bílou barvu.

string zdrojovySoubor = Path.Combine(baseFolder, "frog_nosymb.psd");
string vystupniSoubor = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage psdImage = (PsdImage)Image.Load(zdrojovySoubor))
{
    RawColor pozadi = new RawColor(PixelDataFormat.Rgb32Bpp);
    int argbHodnota = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    pozadi.SetAsInt(argbHodnota); // Bílá

    PsdOptions psdOptions = new PsdOptions(psdImage)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = pozadi,
    };

    psdImage.Save(vystupniSoubor, psdOptions);
}
{{< /highlight >}}

**PSDNET-1897. [Formát AI] Přidána podpora pro zpracování souborů AI s hlavičkou EPSF**

{{< highlight csharp >}}
string zdrojovySoubor = Path.Combine(baseFolder, "example.ai");
string vystupniSoubor = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object ocekavano, object skutecne)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception("Objekty nejsou stejné.");
    }
}

using (AiImage obrazek = (AiImage)Image.Load(zdrojovySoubor))
{
    AssertAreEqual(obrazek.Layers.Length, 2);
    AssertAreEqual(obrazek.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(obrazek.Layers[0].ColorIndex, -1);
    AssertAreEqual(obrazek.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(obrazek.Layers[1].ColorIndex, -1);

    obrazek.Save(vystupniSoubor, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. Částečně nesprávné vykreslování vrstvy tvaru**

{{< highlight csharp >}}
string zdrojovySoubor = Path.Combine(baseFolder, "ShapeLayerTest.psd");
string vystupniSoubor = Path.Combine(outputFolder, "ShapeLayerTest_output.psd");
const int ImgToPsdRatio = 256 * 65535;

using (var im = (PsdImage)Image.Load(zdrojovySoubor))
{
    ShapeLayer vrstvaTvaru = (ShapeLayer)im.Layers[2];
    IPath cesta = vrstvaTvaru.Path;
    IPathShape[] tvaryCesty = cesta.GetItems();
    List<BezierKnotRecord> seznamUzlu = new List<BezierKnotRecord>();
    foreach (IPathShape tvarCesty in tvaryCesty)
    {
        BezierKnotRecord[] uzly = tvarCesty.GetItems();
        seznamUzlu.AddRange(uzly);
    }

    // Změna vlastností vrstvy
    var novyTvar = new PathShape();

    BezierKnotRecord[] bezierUzly = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(100, 100),
                    vrstvaTvaru.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    vrstvaTvaru.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    vrstvaTvaru.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(50, 490),
                    vrstvaTvaru.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 490),
                    vrstvaTvaru.Container.Size), // Ukotvený bod
                PointFToResourcePoint(
                    new PointF(150, 490),
                    vrstvaTvaru.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(490, 150),
                    vrstvaTvaru.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 50),
                    vrstvaTvaru.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 20),
                    vrstvaTvaru.Container.Size),
            },
        },
    };

    novyTvar.SetItems(bezierUzly);

    List<IPathShape> noveTvary = new List<IPathShape>(tvaryCesty);
    noveTvary.Add(novyTvar);

    IPathShape[] novaCesta = noveTvary.ToArray();
    cesta.SetItems(novaCesta);

    vrstvaTvaru.Update();

    im.Save(vystupniSoubor, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(vystupniSoubor))
{
    ShapeLayer vrstvaTvaru = (ShapeLayer)im.Layers[2];
    IPath cesta = vrstvaTvaru.Path;
    IPathShape[] tvaryCesty = cesta.GetItems();
    List<BezierKnotRecord> seznamUzlu = new List<BezierKnotRecord>();
    foreach (IPathShape tvarCesty in tvaryCesty)
    {
        BezierKnotRecord[] uzly = tvarCesty.GetItems();
        seznamUzlu.AddRange(uzly);
    }

    AssertAreEqual(3, tvaryCesty.Length);
    AssertAreEqual(42, vrstvaTvaru.Left);
    AssertAreEqual(14, vrstvaTvaru.Top);
    AssertAreEqual(1600, vrstvaTvaru.Bounds.Width);
    AssertAreEqual(1086, vrstvaTvaru.Bounds.Height);
}

Point PointFToResourcePoint(PointF bod, Size velikostObrazku)
{
    return new Point(
        (int)Math.Round(bod.Y * (ImgToPsdRatio / velikostObrazku.Height)),
        (int)Math.Round(bod.X * (ImgToPsdRatio / velikostObrazku.Width)));
}

void AssertAreEqual(object ocekavano, object skutecne, string zprava = null)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception(zprava ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1957. Výjimka při ukládání souborů PSD s velikostí více než 200 MB a velkými rozměry**

{{< highlight csharp >}}
string zdrojovySoubor = Path.Combine(baseFolder, "bigfile.psd");
string vystupniSoubor = Path.Combine(outputFolder, "output_raw.psd");

PsdLoadOptions moznostiNacitani = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(zdrojovySoubor, moznostiNacitani))
{
    // Zde by neměla být žádná chyba
    psdImage.Save(vystupniSoubor, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. Chyba při ukládání obrázku při ukládání do formátu PDF po aktualizaci z 23.7 na 24.3**

{{< highlight csharp >}}
string zdrojovySoubor = Path.Combine(baseFolder, "CVFlor.psd");
string vystupniSoubor = Path.Combine(outputFolder, "_export.pdf");

using (var psdImage = (PsdImage)Image.Load(zdrojovySoubor))
{
    PdfOptions moznostiUlozeni = new PdfOptions();
    moznostiUlozeni.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(vystupniSoubor, moznostiUlozeni);
}
{{< /highlight >}}

**PSDNET-2033. Oprava problému ve třídě metody GetFontInfoRecords pro čínská písma**

{{< highlight csharp >}}
var slozkaPisma = Path.Combine(baseFolder, "Pismo");
string zdrojovySoubor = Path.Combine(baseFolder, "bd-worlds-best-pink.psd");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { slozkaPisma }, true);
    FontSettings.UpdateFonts();

    using (PsdImage image = (PsdImage)PsdImage.Load(zdrojovySoubor, psdLoadOptions))
    {
        foreach (var vrstva in image.Layers)
        {
            var textovaVrstva = vrstva as TextLayer;

            if (textovaVrstva != null)
            {
                if (textovaVrstva.Text == "best")
                {
                    // Bez této opravy zde dojde k výjimce kvůli čínskému písmu
                    textovaVrstva.UpdateText("ÚSPĚCH");
                }
            }
        }
    }
}
finally
{
    FontSettings.Reset();
    FontSettings.UpdateFonts();
}
{{< /highlight >}}

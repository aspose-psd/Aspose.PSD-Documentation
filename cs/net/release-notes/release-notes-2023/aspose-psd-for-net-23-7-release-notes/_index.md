---
title: Vydání Aspose.PSD pro .NET 23.7
type: docs
weight: 60
url: /cs/net/aspose-psd-pro-net-23-7-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Shrnutí**                                                                                                  | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Přidat možnost exportovat každou vrstvu souboru PSD do animovaného souboru GIF                              | Funkce |
| PSDNET-1441 | Přiřadit vlastnost vyplnění vrstvy tvaru ze zdroje vscg                                                     | Funkce |
| PSDNET-1534 | Přidat nové typy modifikace (arc & arch)                                                                    | Funkce |
| PSDNET-1543 | Změnit aplikaci, která ukládá soubor PSD na Aspose.PSD, pokud je vlastnost UpdateMetadata nastavena na true  | Funkce |
| PSDNET-1567 | Zvětšit výpočetní oblast obrázku s modifikací                                                              | Funkce |
| PSDNET-1471 | Vrstvy úpravy černobílých barvy špatně zpracovávají polopropustnost                                          | Chyba     |
| PSDNET-1505 | Náhrada obsahu SmartObjectu (když je možnost AllowWarpRepaint aktivní) spadne po 2 minutách výpočtu         | Chyba     |
| PSDNET-1585 | Přidat možnost získat skutečnou pozici vrstvy v LayerGroupu                                                 | Chyba     |
| PSDNET-1589 | Změna velikosti vrstvy funguje špatně, když soubor PSD obsahuje VogkResource se strukturami v bodech          | Chyba     |
| PSDNET-1608 | TextBound nefunguje tak, jak se očekává                                                                   | Chyba     |
| PSDNET-1612 | Přidání vrstvy vytvořené výchozí konstruktorem do obrázku PSD nevytváří výchozí zdroje                     | Chyba     |
| PSDNET-1623 | Timeline.LoopesCount je ignorován při exportu do animovaného GIFu                                           | Chyba     |


## **Změny ve veřejném rozhraní API**
# **Přidaná API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **Odebraná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Příklady použití:**

**PSDNET-802. Přidat možnost exportovat každou vrstvu souboru PSD do animovaného souboru GIF**

{{< highlight csharp >}}
string src = "KaždáVrstvaJeRámec.psd";
string outputGif = "out_KazdaVrstvaJeRamec.gif";
string outputPsd = "out_KazdaVrstvaJeRamec.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Vytvořit snímky pro každou vrstvu.
    int pocetSnimku = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] snimky = new Frame[pocetSnimku];
    for (int i = 0; i < pocetSnimku; i++)
    {
        snimky[i] = new Frame();
        LayerState[] stavyVrstev = new LayerState[pocetSnimku];

        for (int j = 0; j < pocetSnimku; j++)
        {
            stavyVrstev[j] = new LayerState();
            stavyVrstev[j].Enabled = i == j;
        }

        snimky[i].LayerStates = stavyVrstev;
    }

    timeline.Frames = snimky;

    // Aktualizovat aktuální stavy
    Layer[] vrstvy = psdImage.Layers;
    LayerState[] stavy = timeline.Frames[timeline.ActiveFrameIndex].LayerStates;
    for (int i = 0; i < pocetSnimku; i++)
    {
        vrstvy[i].IsVisible = stavy[i].Enabled;
    }

    timeline.Save(outputGif, new GifOptions());
    psdImage.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1441. Přiřadit vlastnost vyplnění vrstvy tvaru ze zdroje vscg**

{{< highlight csharp >}}
string srcFile = "TvarInterniPlny.psd";
string outFile = "TvarInterniPlny.psd.out.psd";

using (PsdImage image = (PsdImage)Image.Load(
    srcFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer vrstvaTvaru = (ShapeLayer)image.Layers[1];
    ColorFillSettings nastaveniVyplne = (ColorFillSettings)vrstvaTvaru.Fill;
    nastaveniVyplne.Color = Color.Red;

    vrstvaTvaru.Update();

    image.Save(outFile);
}

// Zkontrolovat uložené změny
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    ShapeLayer vrstvaTvaru = (ShapeLayer)image.Layers[1];
    ColorFillSettings nastaveniVyplne = (ColorFillSettings)vrstvaTvaru.Fill;

    AssertAreEqual(Color.Red, nastaveniVyplne.Color);

    image.Save(outFile);
}

void AssertAreEqual(object ocekavano, object skutecne, string zprava = null)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception(zprava ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1471. Vrstvy úpravy černobílých barvy špatně zpracovávají polopropustnost**

{{< highlight csharp >}}
string srcFile = "zabi_nosymb.psd";
string outFile = "zabi_nosymb.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddBlackWhiteAdjustmentLayer();
    psdImage.Save(outFile);
}

// Zkontrolovat uložené změny
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    BlackWhiteAdjustmentLayer vrstvaUpravCernobile = (BlackWhiteAdjustmentLayer)image.Layers[1];

    if (vrstvaUpravCernobile == null)
    {
        throw new Exception("Vrstva 2 by měla být vrstva úpravy černobílých.");
    }

    image.Save(outFile);
}

void AssertAreEqual(object ocekavano, object skutecne, string zprava = null)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception(zprava ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1505. Náhrada obsahu SmartObjectu (když je možnost AllowWarpRepaint aktivní) spadne po 2 minutách výpočtu**

{{< highlight csharp >}}
string sourceFile = "hrnek 4.psd";
string changeFile = "umělecké dílo pro nahrazení.png";
string outputFile = "export.png";

int novaVyska = 300;

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    SmartObjectLayer vrstvaSmartObjektu = (SmartObjectLayer)psdImage.Layers[3];

    var meritko = (double)novaVyska / vrstvaSmartObjektu.Height;
    var novaSirka = (int)Math.Round(vrstvaSmartObjektu.Width * meritko);

    PsdImage vnitrniObrazek = new PsdImage(novaSirka, novaVyska);
    vnitrniObrazek.SetResolution(72, 72);

    Stream vnitrniStream = new FileStream(changeFile, FileMode.Open);
    Layer vrstva = new Layer(vnitrniStream) { HorizontalResolution = 72, VerticalResolution = 72 };
    try
    {
        vnitrniObrazek.AddLayer(vrstva);

        vrstvaSmartObjektu.ReplaceContents(vnitrniObrazek);
        vrstvaSmartObjektu.UpdateModifiedContent();

        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
    finally
    {
        vnitrniObrazek.Dispose();
        vnitrniStream.Dispose();
        vrstva.Dispose();
    }
}
{{< /highlight >}}

**PSDNET-1534. Přidat nové typy modifikace (arc & arch)**

{{< highlight csharp >}}
string sourceArcFile = "arc_modifikace.psd";
string outputArcFile = "arc_export.png";

string sourceArchFile = "arch_modifikace.psd";
string outputArchFile = "arch_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceArcFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArcFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}

using (var psdImage = (PsdImage)Image.Load(sourceArchFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputArchFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1543. Změnit aplikaci, která ukládá soubor PSD na Aspose.PSD, pokud je vlastnost UpdateMetadata nastavena na true**

{{< highlight csharp >}}
string cesta = "vystup.psd";
using (var obraz = new PsdImage(100, 100))
{
    // Pokud chcete změnit nástroj vytváření, ujistěte se, že vlastnost "UpdateMetadata" je nastavena na true. Je implicitně nastavena na true.
    var psdVolby = new PsdOptions();
    psdVolby.UpdateMetadata = true;

    // Uložení obrázku. 
    obraz.Save(cesta, psdVolby);

    // Kontrola nástroje vytváření v kódu.
    var xmpData = obraz.XmpData;
    var basicPackage = obraz.XmpData.GetPackage(Namespaces.XmpBasic);

    // Zde bude aktualizována informace o nástroji vytváření.
    var aktualniNastrojVytvareni = (string)basicPackage[":CreatorTool"];
}
{{< /highlight >}}

**PSDNET-1567. Zvětšit výpočetní oblast obrázku s modifikací**

{{< highlight csharp >}}
string sourceFile = "hrnek4_modifikace.psd";
string outputFile = "hrnek4_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1585. Přidat možnost získat skutečnou pozici LayerGroupu vlevo a nahoře**

{{< highlight csharp >}}
string sourceFile = "vrstvySkupinyObrazu.psd";

void AssertAreEqual(object ocekavano, object skutecne)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception("Objekty nejsou stejné.");
    }
}

using (var obraz = (PsdImage)Image.Load(sourceFile))
{
    var vrstvy = obraz.Layers;

    for (int i = 0; i < vrstvy.Length; i++)
    {
        var vrstva = vrstvy[i];

        if (vrstva is LayerGroup)
        {
            // Získání LayerGroup.
            var skupina = (LayerGroup)vrstva;

            var ocekavanyLevy = int.MaxValue;
            var ocekavanyHorni = int.MaxValue;
            var ocekavanyPravy = 0;
            var ocekavanyDolni = 0;

            // Výpočet skutečných hodnot pozice vlevo, nahoře, vpravo a dole.
            foreach (var vnejsiVrstva in skupina.Layers)
            {
                if (vnejsiVrstva is AdjustmentLayer || vnejsiVrstva.Bounds.IsEmpty)
                {
                    continue;
                }

                ocekavanyLevy = Math.Min(ocekavanyLevy, vnejsiVrstva.Left);
                ocekavanyHorni = Math.Min(ocekavanyHorni, vnejsiVrstva.Top);
                ocekavanyPravy = Math.Max((ocekavanyLevy + skupina.Width), (vnejsiVrstva.Left + vnejsiVrstva.Width));
                ocekavanyDolni = Math.Max((ocekavanyHorni + skupina.Height), (vnejsiVrstva.Top + vnejsiVrstva.Height));
            }

            // Pozice LayerGroup vlevo, nahoře, vpravo a dole jsou nyní počítány správně.
            AssertAreEqual(skupina.Left, ocekavanyLevy);
            AssertAreEqual(skupina.Top, ocekavanyHorni);
            AssertAreEqual(skupina.Right, ocekavanyPravy);
            AssertAreEqual(skupina.Bottom, ocekavanyDolni);
        }
    }
}
{{< /highlight >}}

**PSDNET-1589. Změna velikosti vrstvy funguje špatně, když soubor PSD obsahuje VogkResource se strukturami v bodech**

{{< highlight csharp >}}
string[] sourceFiles = new string[]
{
    "BodyVectorPuvod.psd",
    "TopVogkResStrukt.psd"
};

foreach (string sourceFile in sourceFiles)
{
    using (PsdImage image = (PsdImage)Image.Load(sourceFile))
    {
        Layer vrstva = image.Layers[0];

        vrstva.Resize(50, 50);

        AssertAreEqual(vrstva.Height, 50);
        AssertAreEqual(vrstva.Width, 50);
    }
}

void AssertAreEqual(object ocekavano, object skutecne, string zprava = null)
{
    if (!object.Equals(ocekavano, skutecne))
    {
        throw new Exception(zprava ?? "Objekty nejsou stejné.");
    }
}
{{< /highlight >}}

**PSDNET-1608. TextBound nefunguje tak, jak se očekává**

{{< highlight csharp >}}
string sourceFile = "vstup_ZkouskaNaVstupenku.psd";
string outFile = "out_1608.psd";

Size novaTextBox = new Size(-1, -1);
using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    //Krok: Nahrazení textu
    TextLayer textovaVrstva = (TextLayer)psdImage.Layers[3];
    textovaVrstva.TextData.Items[0].Text = "Test text nahrazen";

    //Krok: Aktualizace TextBoundBox
    textovaVrstva.TextData.UpdateLayerData();
    novaTextBox = new Size((int)Math.Ceiling(textovaVrstva.TextBoundBox.Width), text
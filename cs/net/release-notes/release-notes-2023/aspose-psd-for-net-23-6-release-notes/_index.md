---
title: Aspose.PSD pro .NET 23.6 - poznámky k vydání
type: docs
weight: 70
url: /cs/net/aspose-psd-pro-net-23-6-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                                                                      | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1401 | Přepracování API Časové osy                                                                                                                            | Vylepšení  |
| PSDNET-1517 | Odstranění artefaktů při vykreslování deformací                                                                                                             | Vylepšení  |
| PSDNET-1528 | Optimalizace vykreslování deformací                                                                                                                      | Vylepšení  |
| PSDNET-147  | Podpora úpravy s prahovou vrstvou                                                                                                            | Funkce      |
| PSDNET-149  | Podpora vrstvy úpravy selektivních barev                                                                                                      | Funkce      |
| PSDNET-801  | Možnost exportovat časovou osu PSD ve formátu animovaného GIF souboru                                                                                          | Funkce      |
| PSDNET-1555 | Přidána podpora pro vrstvu textu bez obdélníkových hran                                                                                            | Funkce      |
| PSDNET-1582 | Podpora vrstvy tvaru                                                                                                                            | Funkce      |
| PSDNET-864  | Při nahrazení obrázku ve chytrém objektu není aktualizováno                                                                                                  | Chyba          |
| PSDNET-1404 | Soubor PSD nelze uložit jako PSD s následujícím výjimkou: Módy Rgb a Lab nemohou obsahovat méně než 3 kanály a více než 4 kanály   | Chyba          |
| PSDNET-1546 | Ztráta zarovnání textu při otevření vrstvy textu v režimu úprav ve Photoshopu                                                                       | Chyba          |
| PSDNET-1548 | Vyvolání nulové odkazové výjimky při ukládání souboru PSD                                                                                                      | Chyba          |
| PSDNET-1578 | Výjimka při načítání vrstvy tvaru: Body pro původ hranice vektoru zatím nejsou podporovány                                                 | Chyba          |
| PSDNET-1579 | Výjimka při načítání zdroje VogkResource: Body jsou uloženy jako DoubleStructures, čteme jako UnitStructures                                            | Chyba          |
| PSDNET-1581 | Typ vrstvy ShapeLayer je prázdný                                                                                                                 | Chyba          |


## **Změny ve veřejném API**
# **Přidaná API:**
- Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.ActiveFrameIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.LoopesCount
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.String,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.Save(System.IO.Stream,Aspose.PSD.ImageOptionsBase)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Timeline.SwitchActiveFrame(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.PsdImage.Timeline
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeBoundingBox.PointsUnitType
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Cyan
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Magenta
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Yellow
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection.Black
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Relative
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CorrectionMethodTypes.Absolute
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Reds
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Yellows
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Greens
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Cyans
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blues
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Magentas
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Whites
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Neutrals
- F:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes.Blacks
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.CorrectionMethod
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.GetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes)
- M:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorLayer.SetCmykCorrection(Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.SelectiveColorsTypes,Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.CmykCorrection)
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddSelectiveColorAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ThresholdLayer.Level
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddThresholdAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.CreateInstance
- M:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Update
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Path


# **Odebraná API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.Frame.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.#ctor(System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.AFSt
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.FsID
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ActiveFrame
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LoopesCount
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.Frames
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.LayerIds
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.InitializeFrom(Aspose.PSD.FileFormats.Psd.PsdImage)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.TimeLine.ApplyTo(Aspose.PSD.FileFormats.Psd.PsdImage)


## **Příklady použití:**

**PSDNET-147. Podpora úpravy s prahovou vrstvou**

{{< highlight csharp >}}
string souborZdrojThrsLayer = "flowers_threshold_source.psd";
string výstupPsdThrsLayer = "flowers_threshold_output.psd";
string výstupPngThrsLayer = "flowers_threshold_output.png";

string souborBezThrsLayer = "flowers_source.psd";
string výstupBezThrsLayer = "flowers_output.psd";
string výstupBezThrsLayer = "flowers_output.png";

void Porovnání(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objekty nejsou shodné.");
    }
}

// Získání, zkontrolování a změna vrstvy úpravy prahu v obraze.
using (var image = (PsdImage)Image.Load(souborZdrojThrsLayer))
{
    foreach (var vrstva in image.Layers)
    {
        if (vrstva is ThresholdLayer)
        {
            // Získání vrstvy úpravy prahu.
            ThresholdLayer thrsLayer = (ThresholdLayer)vrstva;
            var úroveň = thrsLayer.Level;

            // Kontrola parametrů vrstevníků.
            Porovnání(úroveň, (krátké)115);

            // Nastavení parametrů vrstevníků.
            thrsLayer.Level = 50;

            image.Save(výstupPsdThrsLayer);
            image.Save(výstupPngThrsLayer, new PngOptions());
        }
    }
}

// Přidání a nastavení vrstvy úpravy prahu do obrázku.
using (var image = (PsdImage)Image.Load(souborBezThrsLayer))
{
    // Přidání vrstvy úpravy prahu.
    ThresholdLayer thresholdLayer = image.AddThresholdAdjustmentLayer();

    // Nastavení parametrů vrstevníků.
    thresholdLayer.Level = 115;

    image.Save(výstupPsdBezThrsLayer);
    image.Save(výstupPngBezThrsLayer, new PngOptions());
}
{{< /highlight >}}

**PSDNET-149. Podpora vrstvy úpravy selektivních barev**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-801. Možnost exportovat časovou osu PSD ve formátu animovaného GIF souboru**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-864. Při nahrazení obrázku ve chytrém objektu není aktualizováno**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1401. Přepracování API Časové osy**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1404. Soubor PSD nelze uložit jako PSD s následujícím výjimkou: Módy Rgb a Lab nemohou obsahovat méně než 3 kanály a více než 4 kanály**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1517. Odstranění artefaktů při vykreslování deformací**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1528. Optimalizace vykreslování deformací**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1546. Ztráta zarovnání textu při otevření vrstvy textu v režimu úprav Photoshopu**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1548. Vyvolání nulové odkazové výjimky při ukládání souboru PSD**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1555. Přidána podpora pro vrstvu textu bez obdélníkových hran**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1578. Výjimka při načítání vrstvy tvaru: Body pro původ hranice vektoru zatím nejsou podporovány**

**PSDNET-1579. Výjimka při načítání zdroje VogkResource: Body jsou uloženy jako DoubleStructures, čteme jako UnitStructures**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1581. Typ vrstvy ShapeLayer je prázdný**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}

**PSDNET-1582. Podpora vrstvy tvaru**

{{< highlight csharp >}}
// Insert translation here
{{< /highlight >}}
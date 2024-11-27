---
title: Aspose.PSD pro .NET 23.5 - Poznámky k vydání
type: docs
weight: 80
url: /cs/net/aspose-psd-pro-net-23-5-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Klíč**    | **Souhrn**                                                                   | **Kategorie** |
|:-----------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-343  | Podpora pro filtr: Zostřit -> Zostřit                                      | Funkce       |
| PSDNET-1179 | Ukládání souboru PSD (RGB/8bit nebo RGB/16bit) bez vrstev na 32bit          | Funkce       |
| PSDNET-1408 | Implementace zacházení s cestovými objekty z prostředků vsms nebo vmsk pro ShapeLayer | Funkce       |
| PSDNET-1508 | Přidání vlivu bodů sítě na sebe navzájem                                   | Funkce       |


## **Změny ve veřejném API**
# **Přidané API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Uložit(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.JeInvertováno
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.NeníPropojen
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.NeníPovoleno
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.ZískatPoložky
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.NastavitPoložky(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.JeUzavřeno
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.OperaceCesty
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.ZískatPoložky
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.NastavitPoložky(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.JeUzavřeno
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.OperaceCesty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IndexTvaru
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ZískatPoložky
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.NastavitPoložky(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.ZačínejteVýplníSvýmiPixely
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.BarvaVýplně
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Verze
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.NeníPovoleno
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.NeníPropojeno
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.JeInvertováno
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.ZískatPoložky
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.NastavitPoložky(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Název
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.IdFiltru
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.TypFiltru


# **Odebrané API:**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Uložit(Aspose.PSD.StreamContainer,System.Int32)


## **Příklady použití:**

**PSDNET-343. Podpora pro filtr: Zostřit -> Zostřit**

{{< highlight csharp >}}
string sourceFile = "sharpen_source.psd";
string outputPsd = "sharpen_output.psd";
string outputPng = "sharpen_output.png";

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objekty nejsou shodné.");
    }
}

using (var image = (PsdImage)Image.Load(sourceFile))
{
    SmartObjectLayer smartObj = (SmartObjectLayer)image.Layers[1];

    // úprava chytrých filtrů
    SharpenSmartFilter sharp = (SharpenSmartFilter)smartObj.SmartFilters.Filters[0];

    // ověření hodnot filtru
    AssertAreEqual(BlendMode.Normal, sharp.BlendMode);
    AssertAreEqual(100d, sharp.Opacity);
    AssertAreEqual(true, sharp.IsEnabled);

    // aktualizace hodnot filtru
    sharp.BlendMode = BlendMode.Divide;
    sharp.Opacity = 75;
    sharp.IsEnabled = false;

    // přidání nových filtrací
    var filtry = new List<SmartFilter>(smartObj.SmartFilters.Filters);
    filtry.Add(new SharpenSmartFilter());
    smartObj.SmartFilters.Filters = filtry.ToArray();

    // aplikace změn
    smartObj.SmartFilters.UpdateResourceValues();
    smartObj.UpdateModifiedContent();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1179. Uložení souboru PSD (RGB/8bit nebo RGB/16bit) bez vrstev na 32bit**

{{< highlight csharp >}}
string inputFile =  "input_8bit_rle.psd";
string outputPsdFile = "output_32bit.psd";
string outputImageFile32 = "output_from_32bit.png";

using (PsdImage srcImg = (PsdImage)Image.Load(inputFile))
{
    PsdOptions totalOptions = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    srcImg.Save(outputPsdFile, totalOptions);

    using (var img32 = Image.Load(outputPsdFile))
    {
        img32.Save(outputImageFile32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}

**PSDNET-1408. Implementace zacházení s cestovými objekty z prostředků vsms nebo vmsk pro ShapeLayer**

{{< highlight csharp >}}
string srcFile = "ShapeLayerTest.psd";
string outFile = "ShapeLayerTest-out.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = image.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool začínáVýplňVšemiPixely;
    List<IPathShape> tvarovéObjekty = ZískatTvaryZProstředků(vectorPathDataResource, out začínáVýplňVšemiPixely);

    // Odstranění jednoho tvaru
    tvarovéObjekty.RemoveAt(1);

    // Uložení změněných dat do prostředku
    List<VectorPathRecord> cesta = new List<VectorPathRecord>();
    cesta.Add(new PathFillRuleRecord(null));
    cesta.Add(new InitialFillRuleRecord(začínáVýplňVšemiPixely));

    for (ushort i = 0; i < tvarovéObjekty.Count; i++)
    {
        PathShape tvar = (PathShape)tvarovéObjekty[i];
        tvar.IndexTvaru = i;
        cesta.AddRange(tvar.ToVectorPathRecords());
    }

    vectorPathDataResource.Paths = cesta.ToArray();

    image.Save(outFile);
}

// Ověření změněných hodnot v uloženém souboru
using (PsdImage image = (PsdImage)Image.Load(outFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer shapeLayer = image.Layers[1];
    VectorPathDataResource vectorPathDataResource = (VectorPathDataResource)shapeLayer.Resources[1];

    bool začínáVýplňVšemiPixely;
    List<IPathShape> tvarovéObjekty = ZískatTvaryZProstředků(vectorPathDataResource, out začínáVýplňVšemiPixely);

    // Uložený soubor by měl obsahovat 1 tvar
    AssertAreEqual(1, tvarovéObjekty.Count);
}

void AssertAreEqual(object očekávané, object aktuální, string zpráva = null)
{
    if (!object.Equals(očekávané, aktuální))
    {
        throw new Exception(zpráva ?? "Objekty nejsou shodné.");
    }
}

List<IPathShape> ZískatTvaryZProstředků(VectorPathDataResource vectorPathDataResource, out bool začínáVýplňVšemiPixely)
{
    List<IPathShape> tvary = new List<IPathShape>();
    LengthRecord délkaZáznamů = null;
    začínáVýplňVšemiPixely = false;
    List<BezierKnotRecord> bezierKnotRecords = new List<BezierKnotRecord>();

    foreach (var záznamCesty in vectorPathDataResource.Paths)
    {
        if (záznamCesty is LengthRecord)
        {
            if (bezierKnotRecords.Count > 0)
            {
                tvary.Add(new PathShape(délkaZáznamů, bezierKnotRecords.ToArray()));
                délkaZáznamů = null;
                bezierKnotRecords.Clear();
            }

            délkaZáznamů = (LengthRecord)záznamCesty;
        }
        else if (záznamCesty is BezierKnotRecord)
        {
            bezierKnotRecords.Add((BezierKnotRecord)záznamCesty);
        }
        else if (záznamCesty is InitialFillRuleRecord)
        {
            InitialFillRuleRecord inicializačníZáznamVýplně = (InitialFillRuleRecord)záznamCesty;
            začínáVýplňVšemiPixely = inicializačníZáznamVýplně.JeVýplňZačínáVšemiPixely;
        }
    }

    if (bezierKnotRecords.Count > 0)
    {
        tvary.Add(new PathShape(délkaZáznamů, bezierKnotRecords.ToArray()));
        délkaZáznamů = null;
        bezierKnotRecords.Clear();
    }

    return tvary;
}
{{< /highlight >}}

**PSDNET-1508. Přidání vlivu bodů sítě na sebe navzájem**

{{< highlight csharp >}}
string sourceFile = "Bottom_Right.psd";
string outputFile = "output.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    image.Save(outputFile, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}
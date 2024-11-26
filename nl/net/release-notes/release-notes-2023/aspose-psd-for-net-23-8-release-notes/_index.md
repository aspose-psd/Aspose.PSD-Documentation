---
title: Aspose.PSD voor .NET 23.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-23-8-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel** | **Samenvatting** | **Categorie** |
|:------------|:-----------------|:-------------|
| PSDNET-1566 | Nieuw type warp toevoegen (Flag) | Feature |
| PSDNET-1621 | Nieuwe warp types toevoegen: boog omhoog, boog omlaag, bol | Feature |
| PSDNET-1682 | Implementeer nieuwe methode PsdImage.AddPosterizeAdjustmentLayer om nieuwe posterize laag toe te voegen | Feature |
| PSDNET-913  | PSD-informatie gaat verloren bij alleen openen en opslaan | Bug |
| PSDNET-1352 | Laden van afbeelding mislukt | Bug |
| PSDNET-1553 | Laden van afbeelding mislukt: Kan object van type UnknownStructure niet casten naar type DescriptorStructure | Bug |
| PSDNET-1631 | Bestand gewijzigd in de bibliotheek van derden beschadigt PSD-bestand maar kan worden geopend in Photoshop | Bug |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-913. PSD-informatie gaat verloren bij alleen openen en opslaan**

{{< highlight csharp >}}
string src = "OrigineelBestand.psd";
string outputPsd = "uit_OrigineelBestand.psd";
string outputPng = "uit_OrigineelBestand.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Laden van afbeelding mislukt**

{{< highlight csharp >}}
string srcBestand1 = "test_tekst.psd";
string srcBestand2 = "test_slim_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcBestand1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcBestand2))
{
}
{{< /highlight >}}

**PSDNET-1553. Laden van afbeelding mislukt: Kan object van type UnknownStructure niet casten naar type DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Zou correct moeten laden
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Bestand gewijzigd in de bibliotheek van derden beschadigt PSD-bestand maar kan worden geopend in Photoshop**

{{< highlight csharp >}}
string bronBestand = "uitvoer.psd";
string uitvoerBestand = "export.png";

using (PsdImage img = (PsdImage)Image.Load(bronBestand, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(uitvoerBestand, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Nieuw type warp toevoegen (Flag)**

{{< highlight csharp >}}
string bronBestand = "vlag_warp.psd";
string uitvoerBestand = "vlag_export.png";

using (var psdImage = (PsdImage)Image.Load(bronBestand, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(uitvoerBestand, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Nieuwe warp types toevoegen: boog omhoog, boog omlaag, bol**

{{< highlight csharp >}}
string bronBestandBoogOmhoog = "boog_bovenste_warp.psd";
string bronBestandBoogOmlaag = "boog_onderste_warp.psd";
string bronBestandBolling =  "bolling_warp.psd";

string uitvoerBestandBoogOmhoog ="BoogBovenste_export.png";
string uitvoerBestandBoogOmlaag = "BoogOnderste_export.png";
string uitvoerBestandBolling = "Bolling_export.png";

using (var psdImage = (PsdImage)Image.Load(bronBestandBoogOmhoog, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(uitvoerBestandBoogOmhoog, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(bronBestandBoogOmlaag, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(uitvoerBestandBoogOmlaag, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(bronBestandBolling, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(uitvoerBestandBolling, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementeer nieuwe methode PsdImage.AddPosterizeAdjustmentLayer om nieuwe posterize laag toe te voegen**

{{< highlight csharp >}}
string bronBestand = "zendeya.psd";
string uitBestand = "zendeya.psd.uit.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(bronBestand))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(uitBestand);
}

// Controleer opgeslagen wijzigingen
using (PsdImage image = (PsdImage)Image.Load(
    uitBestand,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object verwacht, object werkelijk, string boodschap = null)
{
    if (!object.Equals(verwacht, werkelijk))
    {
        throw new Exception(boodschap ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

---
title: Aspose.PSD voor .NET 23.1 - Uitgaveopmerkingen
type: docs
weight: 120
url: /nl/net/aspose-psd-voor-dotnet-23-1-uitgaveopmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat de uitgaveopmerkingen voor [Aspose.PSD voor .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-401|Ondersteuning van vstkResource|Functie|
|PSDNET-1346|Toevoegen van de bewerkbare eigenschap BaselineDirection/IsStandardVerticalRomanAlignmentEnabled aan de IText-interface|Functie|
|PSDNET-181|PSD wordt niet correct geconverteerd naar JPEG|Fout|
|PSDNET-958|PSB naar PDF mislukt voor grote bestanden|Fout|
|PSDNET-1171|Toevoegen van verwerking van klemmasker naar aanpassingslaag|Fout|
|PSDNET-1252|Na het formaat wijzigen van de volledige afbeelding en vervolgens na het formaat wijzigen van de specifieke laag gooit Aspose.PSD een uitzondering bij het opslaan van de laag|Fout|


## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsStandardVerticalRomanAlignmentEnabled
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.RoundCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.SquareCap
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineCapType.ButtCap
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.BevelJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.RoundJoin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.LineJoinType.MiterJoin
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillEnabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineDashOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleMiterLimit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineCapWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineJoinType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleLineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleScaleLock
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleStrokeAdjust
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleBlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleOpacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleResolution
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.StrokeStyleContent
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Levels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PostResource.TypeToolKey


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-181. PSD wordt niet correct geconverteerd naar JPEG**

{{< highlight csharp >}}
string srcFile = "helicopter.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Ondersteuning van vstkResource**

{{< highlight csharp >}}
string srcFile = "StrokeShapeTest1.psd";
string dstFile = "StrokeShapeTest2.psd";

using (PsdImage image = (PsdImage)Image.Load(srcFile))
{
    Layer layer = image.Layers[1];
    foreach (LayerResource resource in layer.Resources)
    {
        if (resource is VstkResource)
        {
            VstkResource vstkResource = (VstkResource)resource;
            vstkResource.StrokeStyleLineAlignment = StrokePosition.Outside;
            vstkResource.StrokeStyleLineWidth = 20;
        }
    }

    image.Save(dstFile);
}
{{< /highlight >}}

**PSDNET-958. PSB naar PDF mislukt voor grote bestanden**

{{< highlight csharp >}}
string inputPath = "SteveKohli-CarTOP.psb";
string outputPath ="output.pdf";

using (var image = Image.Load(inputPath))
{
    image.Save(outputPath, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Toevoegen van verwerking van klemmasker naar aanpassingslaag**

{{< highlight csharp >}}
string srcFile = "helicopter_part.psd";
string outputJpg = "output.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Na het formaat wijzigen van de volledige afbeelding en vervolgens na het formaat wijzigen van de specifieke laag gooit Aspose.PSD een uitzondering bij het opslaan van de laag**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string imgFile1 = "img1.png";
string imgFile2 = "img2.png";

var loadOptions = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Eerst wijzigen we het formaat van de hele afbeelding
    image.Resize(110, 90);
    var layers = image.Layers;

    var layerOk = layers[0];
    layerOk.Resize(100, 80);

    var layerUitzondering = layers[1];
    layerUitzondering.Resize(100, 80);

    // Hier zal alles goed gaan
    layerOk.Save(imgFile1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // Nu zal hier alles goed gaan
    layerUitzondering.Save(imgFile2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. Toevoegen van de bewerkbare eigenschap BaselineDirection/IsStandardVerticalRomanAlignmentEnabled aan de IText-interface**

{{< highlight csharp >}}
// De volgende code toont het vermogen om de nieuwe eigenschap IsStandardVerticalRomanAlignmentEnabled te bewerken.
// Dit heeft momenteel geen invloed op de rendering, maar stelt u alleen in staat de eigenschapwaarde te bewerken.

string src = "1346test.psd";
string output = "out_1346test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Correct lezen
    }
    else
    {
        throw new Exception("Onjuiste lezing van de eigenschapswaarde IsStandardVerticalRomanAlignmentEnabled");
    }

    textPortion.Style.IsStandardVerticalRomanAlignmentEnabled = false;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (!textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Correct lezen
    }
    else
    {
        throw new Exception("Onjuiste lezing van de eigenschapswaarde IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}}

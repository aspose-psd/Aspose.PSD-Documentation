---
title: Aspose.PSD pro .NET 23.1 - Poznámky k vydání
type: docs
weight: 120
url: /cs/net/aspose-psd-pro-net-23-1-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 23.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-401|Podpora vstkResource|Funkce|
|PSDNET-1346|Přidána editovatelná vlastnost BaselineDirection/IsStandardVerticalRomanAlignmentEnabled do rozhraní IText|Funkce|
|PSDNET-181|PSD není správně převeden na JPEG|Chyba|
|PSDNET-958|PSB na PDF selže u velkých souborů|Chyba|
|PSDNET-1171|Přidat zpracování ořezové masky k vrstvě úprav|Chyba|
|PSDNET-1252|Po změně velikosti celého obrázku a poté po změně velikosti konkrétní vrstvy Aspose.PSD vyvolává výjimku při ukládání vrstvy|Chyba|


## **Změny ve veřejném API**
# **Přidaná API:**
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


# **Odebraná API:**
- žádné


## **Příklady použití:**

**PSDNET-181. PSD není správně převeden na JPEG**

{{< highlight csharp >}}
string srcFile = "vrtulnik.psd";
string outputJpg = "vystup.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-401. Podpora vstkResource**

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

**PSDNET-958. PSB na PDF selže u velkých souborů**

{{< highlight csharp >}}
string inputPath = "SteveKohli-CarTOP.psb";
string outputPath ="vystup.pdf";

using (var image = Image.Load(inputPath))
{
    image.Save(outputPath, new PdfOptions());
}
{{< /highlight >}}

**PSDNET-1171. Přidat zpracování ořezové masky k vrstvě úprav**

{{< highlight csharp >}}
string srcFile = "vrtulnik_cast.psd";
string outputJpg = "vystup.jpg";

using (var psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.Save(outputJpg , new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1252. Po změně velikosti celého obrázku a poté po změně velikosti konkrétní vrstvy Aspose.PSD vyvolává výjimku při ukládání vrstvy**

{{< highlight csharp >}}
string sourceFile = "zdroj.psd";
string imgFile1 = "img1.png";
string imgFile2 = "img2.png";

var loadOptions = new PsdLoadOptions()
{
    ReadOnlyMode = false,
    LoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // Nejprve změníme celý obrázek
    image.Resize(110, 90);
    var layers = image.Layers;

    var layerOk = layers[0];
    layerOk.Resize(100, 80);

    var layerException = layers[1];
    layerException.Resize(100, 80);

    // Zde bude vše v pořádku
    layerOk.Save(imgFile1, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    // Nyní zde bude vše v pořádku
    layerException.Save(imgFile2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });                
}
{{< /highlight >}}

**PSDNET-1346. Přidat editovatelnou vlastnost BaselineDirection/IsStandardVerticalRomanAlignmentEnabled do rozhraní IText**

{{< highlight csharp >}}
// Následující kód demonstruje schopnost editovat novou vlastnost IsStandardVerticalRomanAlignmentEnabled.
// Toto v současné době neovlivní vykreslování, ale umožní vám pouze upravit hodnotu vlastnosti.

string src = "1346test.psd";
string output = "out_1346test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    var textPortion = textLayer.TextData.Items[0];
    if (textPortion.Style.IsStandardVerticalRomanAlignmentEnabled)
    {
        // Správné čtení
    }
    else
    {
        throw new Exception("Nesprávné čtení hodnoty vlastnosti IsStandardVerticalRomanAlignmentEnabled");
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
        // Správné čtení
    }
    else
    {
        throw new Exception("Nesprávné čtení hodnoty vlastnosti IsStandardVerticalRomanAlignmentEnabled");
    }
}
{{< /highlight >}}

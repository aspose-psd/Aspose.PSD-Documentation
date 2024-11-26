---
title: Aspose.PSD for .NET 23.9 - Uitgaveopmerkingen
type: docs
weight: 40
url: /nl/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Deze pagina bevat de uitgaveopmerkingen voor [Aspose.PSD for .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Sleutel** | **Samenvatting** | **Categorie** |
|:------------|:---------------------------------------|:--------|
| PSDNET-1638 | Implementeer het maken van een masker voor nieuwe aanpassingslagen | Functie |
| PSDNET-1654 | Voeg ondersteuning toe voor Blend Clipped Layers als Groepsmengoptie | Functie |
| PSDNET-1194 | PSD-bestand met 16-bits kleurenmodus past geen masker toe op aanpassingslagen | Fout    |
| PSDNET-1235 | Onjuiste weergave van haakjes in de tekstlaag | Fout    |
| PSDNET-1559 | Kan stijlen niet bijwerken in de tekstlagen | Fout    |
| PSDNET-1583 | Na het exporteren van een PSD-bestand met CMYK breken de kleuren in de geëxporteerde PSD | Fout    |
| PSDNET-1619 | Specifiek PSB-bestand geeft uitzondering "Het rechthoek heeft geen gemeenschappelijk verwerkingsgebied" | Fout    |
| PSDNET-1648 | Laden van afbeelding is mislukt. OverflowException: Rekenkundige bewerking resulteerde in een overloop | Fout    |


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-1638. Implementeer het maken van een masker voor nieuwe aanpassingslagen**

{{< highlight csharp >}}
string bronBestand = "zendeya_BW.psd";
string doelBestand = "zendeya_BW_out.psd";

met (var im = (PsdImage)Image.Load(bronBestand))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(doelBestand);
}

met (var im = (PsdImage)Image.Load(doelBestand))
{
    Laag laag = im.Layers[1];

    AssertAreEqual((ushort)5, laag.ChannelsCount);
    AssertAreEqual((short)-2, laag.ChannelInformation[4].ChannelID);
}

leeg AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    als (!object.Equals(verwacht, werkelijk))
    {
        gooi nieuwe Uitzondering(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Voeg ondersteuning toe voor Blend Clipped Layers als Groepsmengoptie**

{{< highlight csharp >}}
string bronBestand = "example_source.psd";
string outputPsd = "example_output.psd";
string outputPng = "example_output.png";

met (var afbeelding = (PsdImage)Image.Load(bronBestand))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, nieuwe PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. PSD-bestand met 16-bits kleurenmodus past geen masker toe op aanpassingslagen**

{{< highlight csharp >}}
string bronBestand = "bron.psd";
string outputPng = "huidige.png";

met (var afbeelding = (PsdImage)Image.Load(bronBestand))
{
    image.Save(outputPng, nieuwe PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Onjuiste weergave van haakjes in de tekstlaag**

{{< highlight csharp >}}
string bestand = "bestand1.psd";
string output = "uitvoer_1235.png";

met (var psdAfbeelding = (PsdImage)Image.Load(bestand))
{
    voor elk (var laag in psdAfbeelding.Layers)
    als (laag is TextLayer tekstLaag)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = nieuwe PsdOptions(psdAfbeelding);
    psdAfbeelding.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Kan stijlen niet bijwerken in de tekstlagen**

{{< highlight csharp >}}
string bronBestand = "Voorbeeld_FontSize.psd";
string uitvoerBestand = "uitvoer_Voorbeeld_FontSize.psd";

met (var psdAfbeelding = (PsdImage)Image.Load(bronBestand, nieuwe PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdAfbeelding.Layers[4];
    var l2 = (TextLayer)psdAfbeelding.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "tekst1", "tekst2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    voor elk (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "tekstlaag 1", "tekstlaag 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    voor elk (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdAfbeelding.Save(uitvoerBestand);
}
{{< /highlight >}}

**PSDNET-1583. Na het exporteren van een PSD-bestand met CMYK breken de kleuren in de geëxporteerde PSD**

{{< highlight csharp >}}
string bronBestand = "canyon.psd";
string outputBestandPng = "uitvoer_canyon.png";

met (var outputStream = nieuwe MemoryStream())
{
    met (var psdAfbeelding = (PsdImage)Image.Load(bronBestand))
    {
        psdAfbeelding.Save(outputStream);
    }

    outputStream.Position = 0;
    met (var psdAfbeelding = (PsdImage)Image.Load(outputStream))
    {
        psdAfbeelding.Save(outputBestandPng, nieuwe PngOptions());
    }
}
{{< /highlight >}}

**PSDNET-1619. Specifiek PSB-bestand geeft uitzondering "Het rechthoek heeft geen gemeenschappelijk verwerkingsgebied"**

{{< highlight csharp >}}
var invoer = "1619_src.psb";
var output = "1619_output.png";
met (PsdImage img = (PsdImage)Image.Load(input, nieuwe PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output, nieuwe PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Laden van afbeelding mislukt. OverflowException: Rekenkundige bewerking resulteerde in een overloop**

{{< highlight csharp >}}
string bronBestand = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

met (PsdImage im = (PsdImage)PsdImage.Load(bronBestand))
{
    Laag laag = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)laag.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

leeg AssertAreEqual(object verwacht, object werkelijk, string bericht = null)
{
    als (!object.Equals(verwacht, werkelijk))
    {
        gooi nieuwe Uitzondering(bericht ?? "Objecten zijn niet gelijk.");
    }
}
{{< /highlight >}}

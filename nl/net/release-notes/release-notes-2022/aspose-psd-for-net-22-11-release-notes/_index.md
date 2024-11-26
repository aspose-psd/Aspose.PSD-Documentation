---
title: Aspose.PSD voor .NET 22.11 - Release-opmerkingen
type: docs
weight: 20
url: /nl/net/aspose-psd-voor-net-22-11-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Deze release heeft een fout in het geval van 16-bits exports, dus we raden voorzichtigheid aan bij het gebruik van deze functie in deze release.
Update Aspose.PSD niet naar 22.9-22.11 als 16-bits beeldverwerking uw primaire functionaliteit is.

We werken aan oplossingen voor deze problemen.

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1320|Kan extreem grote PSB-bestanden niet exporteren|Uitbreiding|
|PSDNET-659|Maak het midden van de radiale gradiënt verplaatsbaar|Mogelijkheid|
|PSDNET-1330|Niet-ondersteunde compressiemethode ZipWithoutPrediction voor specifieke bestanden|Mogelijkheid|
|PSDNET-735|Na het toepassen van een transformatiemethode voor slechts een laag, heeft de opgeslagen laag een onjuiste grensdoos|Fout|
|PSDNET-1234|Uitzondering bij het laden van een PSD-afbeelding met patroon|Fout|
|PSDNET-1244|Beeldexport mislukt (IndexOutOfRangeException) bij het opslaan van een PSD-bestand met Chinese symbolen|Fout|
|PSDNET-1303|TimeLine ActiveFrame wordt onjuist toegepast|Fout|
|PSDNET-1307|Regressie 22.7: incorrecte weergave van tekst met Arabische tekens|Fout|
|PSDNET-1321|Vector Masker op de Groepslaag werkt onjuist. De uiteindelijke afbeelding heeft een zwart gat, maar zou dat niet moeten hebben|Fout|


## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDNET-659. Maak het midden van de radiale gradiënt verplaatsbaar**

{{< highlight csharp >}}
string bronBestand = "psdnet659.psd";
string uitvoerBestand = "output.png";

using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(bronBestand))
{
    FillLayer radialeLaag = (FillLayer)psdAfbeelding.Lagen[5];
    GradientFillSettings instellingen = (GradientFillSettings)radialeLaag.FillSettings;

    // Werk het offsetpunt bij
    instellingen.HorizontalOffset = 10;
    instellingen.VerticalOffset = -25;

    psdAfbeelding.Opslaan(uitvoerBestand, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Na het toepassen van een transformatiemethode voor slechts een laag, heeft de opgeslagen laag een onjuiste grensdoos**

{{< highlight csharp >}}
string bronBestandsNaam = @"TextLayer.psd";
string uitvoerBestand = "TextLayerResized_output.psd";

using (PsdImage afbeelding = (PsdImage)Afbeelding.Laden(bronBestandsNaam, new PsdLoadOptions()))
{
    TextLayer tekstLaag = (TextLayer)afbeelding.Lagen[1];

    // Het stelt de nieuwe grootte van de tekstlaag in
    const int NieuweBreedte = 250;
    const int NieuweHoogte = 250;

    // Het stelt het mechanisme in voor hoe de resize-functie de laag zal vergroten (standaardwaarde)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Nieuw mechanisme van vergroten voor tekstlaag hier gebruiken
    // Niet alleen de laag, maar ook de transformatiematrix van de tekstlaag zal veranderen
    tekstLaag.Resize(NieuweBreedte, NieuweHoogte, resizeType);

    afbeelding.Opslaan(uitvoerBestand, new PsdOptions(afbeelding));
}

using (PsdImage afbeelding = (PsdImage)Afbeelding.Laden(uitvoerBestand, new PsdLoadOptions()))
{
    TextLayer txtLaag = (TextLayer)afbeelding.Lagen[1];

    // Reden van delta is ander standaardlettertype
    if (txtLaag.TransformMatrix[4] >= 65 
        && txtLaag.TransformMatrix[4] <= 67
        && txtLaag.TransformMatrix[5] >= 234
        && txtLaag.TransformMatrix[5] <= 237)
    {
        // Alles is in orde
    }
    else
    {
        throw new Exception("Locatiepunt is verkeerd");
    }
}
{{< /highlight >}}

**PSDNET-1234. Uitzondering bij het laden van een PSD-afbeelding met patroon**

{{< highlight csharp >}}
string srcBestand = "test.psd";
string uitvoer = "output1234.png";

using (PsdImage psdAfbeelding = (PsdImage)PsdImage.Laden(srcBestand,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOpties = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdAfbeelding.Opslaan(uitvoer, pngOpties);
}
{{< /highlight >}}

**PSDNET-1244. Beeldexport mislukt (IndexOutOfRangeException) bij het opslaan van een PSD-bestand met Chinese symbolen**

{{< highlight csharp >}}
string bronBestand = "input.psd";
string outputPad = "output.psd";

var laadOpties = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var afbeelding = (PsdImage)Afbeelding.Laden(bronBestand, laadOpties))
{
    foreach (var laag in afbeelding.Lagen)
    {
        if (laag.Naam == "1")
        {
            var txtLaag = (TextLayer)laag;

            txtLaag.UpdateText("测试测试");
        }
    }

    // Hier mag geen uitzondering zijn.
    afbeelding.Opslaan(outputPad, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame wordt onjuist toegepast**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(src))
{
    TimeLine timeLine = TimeLine.InitialiseerVanuit(psdAfbeelding);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdAfbeelding);

    psdAfbeelding.Opslaan(output);
}
{{< /highlight >}}

**PSDNET-1307. Regressie 22.7: incorrecte weergave van tekst met Arabische tekens**

{{< highlight csharp >}}
string testLettertypeMap = "Lettertypen";
FontSettings.SetFontsFolder(testLettertypeMap);
FontSettings.UpdateFonts();

string sourceBestandsPad = "sarbarg.fin12.psd";
string outputPad = "result.tiff";

using (var psdAfbeelding = (PsdImage)Afbeelding.Laden(sourceBestandsPad))
{
    psdAfbeelding.Opslaan(outputPad, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Kan extreem grote PSB-bestanden niet exporteren**

{{< highlight csharp >}}
string bronBestand = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPad = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var afbeelding = (PsdImage)Afbeelding.Laden(bronBestand, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    afbeelding.Opslaan(psdExportPad, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Vector Masker op de Groepslaag werkt onjuist. De uiteindelijke afbeelding heeft een zwart gat, maar zou dat niet moeten hebben**

{{< highlight csharp >}}
string srcBestand = "demo.psd";
string uitvoer = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Laden(srcBestand))
{
    PngOptions pngOpties = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Opslaan(uitvoer, pngOpties);
}
{{< /highlight >}}

**PSDNET-1330. Niet-ondersteunde compressiemethode ZipWithoutPrediction voor specifieke bestanden**

{{< highlight csharp >}}
string bronBestand = "20221017_220706_0000.psd";
string uitvoerBestand = "20221017_220706_0000.jpg";

using (var afbeelding = (PsdImage)Afbeelding.Laden(bronBestand, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optiesBasis = new JpegOptions() { Quality = 80 };
    afbeelding.Opslaan(uitvoerBestand, optiesBasis);
}
{{< /highlight >}}

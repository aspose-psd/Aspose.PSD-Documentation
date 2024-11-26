---
title: Aspose.PSD voor .NET 22.12 - Release-opmerkingen
type: docs
weight: 10
url: /nl/net/aspose-psd-voor-net-22-12-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- In deze release is een regressie met 16-bits export opgelost.

{{% /alert %}}

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-1336|Voeg de bewerkbare TextOrientation-eigenschap toe aan de IText-interface|Functie|
|PSDNET-725|Het wijzigen van de specifieke PSD-bestand met een laagmasker produceert een incorrect masker|Fout|
|PSDNET-1277|Voeg de mogelijkheid toe om een masker voor 16 afbeeldingen op te slaan en te laden|Fout|
|PSDNET-1281|Onjuiste transparantie bij opslaan van een 16-bits afbeelding naar een 16- of 8-bits afbeelding|Fout|
|PSDNET-1375|Fix CMYK in 16-bits kleur|Fout|


## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Verwijderde API's:**
- Geen


## **Gebruiksvoorbeelden:**

**PSDNET-725. Het wijzigen van de specifieke PSD-bestand met een laagmasker produceert een incorrect masker**

{{< highlight csharp >}}
string sourceFile = "bron.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Het opent het bron PSD-bestand
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Het maakt de wijziging 
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Het opent een gewijzigd PSD-bestand
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Het converteert naar PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Voeg de mogelijkheid toe om een masker voor 16 afbeeldingen op te slaan en te laden**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Opties voor het opslaan van 16-bits kleur
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // PSD-bestand wordt opgeslagen met transparantie
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Onjuiste transparantie bij opslaan van een 16-bits afbeelding naar een 16- of 8-bits afbeelding**

{{< highlight csharp >}}
string sourceFile = @"Voorbeeld_16bit.psd";
string resavedFile = @"Hersave_16bit.psd";
string imageFile = @"TotaleAfbeelding_16bit.png";

// Het 16-bits kleuren PSD-bestand (met transparantie) wordt geopend en opgeslagen als 16-bits kleur
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Het opgeslagen 16-bits kleuren PSD-bestand wordt omgezet naar een png-bestand met transparantie
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Voeg de bewerkbare TextOrientation-eigenschap toe aan de IText-interface**

{{< highlight csharp >}}
// De volgende code toont de mogelijkheid om de nieuwe TextOrientation-eigenschap te bewerken.
// Dit heeft op dit moment geen invloed op de weergave, maar stelt je alleen in staat de eigenschapswaarde te bewerken.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Juiste lezing
    }
    else
    {
        throw new Exception("Onjuiste lezing van de TextOrientation-eigenschapswaarde");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Juiste lezing
    }
    else
    {
        throw new Exception("Onjuiste lezing van de TextOrientation-eigenschapswaarde");
    }
}
{{< /highlight >}}

**PSDNET-1375. Fix CMYK in 16-bits kleur**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Het instelt van de conversieopties
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Het converteert en slaat op
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Het opent het geconverteerde bestand en converteert naar PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

---
title: Aspose.PSD voor .NET 20.3 - Release-opmerkingen
type: docs
weight: 100
url: /nl/net/aspose-psd-voor-net-20-3-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-188|Ondersteuning van .Net Core|Functie|
|PSDNET-523|Converteer Adobe Illustrator-bestanden naar PDF's|Functie|
|PSDNET-212|Toevoegen van de mogelijkheid om verschillende stijlen te renderen in één tekstlaag|Functie|
|PSDNET-144|Ondersteuning van Zwart-wit Aanpassingslaag|Functie|
|PSDNET-233|Ondersteuning toevoegen van export AI-indeling (Versie 8) naar andere indelingen|Functie|
|PSDNET-540|Ondersteuning van PassThrough Blending Mode-verwerking (Alleen gebruikt voor Layer Group)|Functie|
|PSDNET-539|Uitzondering: Afbeeldingsladen mislukt bij laden van afbeelding met lege Unicode Alpha Namen Resource|Fout|
|PSDNET-541|Onjuiste uitvoer na wijzigen zichtbaarheid van een LayerGroup|Fout|
|PSDNET-516|Uitzondering bij laden PSD-afbeelding: Kleursectie (DropShadow Resource) moet 3 kleurcomponenten bevatten voor RGB of 4 kleurcomponenten voor CMYK|Fout|
|PSDNET-536|Uitzondering als geprobeerd wordt te tekenen op een nieuw gemaakte laag als de eenvoudige versie van Constructor wordt gebruikt|Fout|

## **Wijzigingen in de Openbare API**
# **Toegevoegde API's:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Onderstrepen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Doorhalen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePorties(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **Verwijderde API's:**
- Geen

## **Gebruik voorbeelden:**
**PSDNET-523. Converteer Adobe Illustrator-bestanden naar PDF's**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Toevoegen van de mogelijkheid om verschillende stijlen te renderen in één tekstlaag**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "kleine letters" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Onderstrepen = true; // bewerk tekststijl "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // bewerk tekststijl "2\r"

    newPortions[2].Style.FauxBold = true; // bewerk tekststijl "Vetgedrukt"

    newPortions[3].Style.FauxItalic = true; // bewerk tekststijl "Cursief\r"

    newPortions[3].Style.BaselineShift = -25; // bewerk tekststijl "Cursief\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // bewerk tekststijl "kleine letters"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Ondersteuning toevoegen van export AI-indeling (Versie 8) naar andere indelingen**

{{< highlight java >}}

 // Voorbeeld van exporteren van AI-bestand naar PSD- en PNG-indeling

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Ondersteuning van Passthrough Blending Mode-verwerking (Alleen gebruikt voor Layer Group).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Er is geen 23e laag.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "De 23e laag is geen laaggroep.");

    AssertIsTrue(layer.Name == "Aanpassingsgroep", "De naam van de 23e laag is niet 'Aanpassingsgroep'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.Passthrough, "Laag 'Aanpassingsgroep' moet 'passthrough' blendmodus hebben.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normaal;

    image.Save("Normaal" + outputFileName, new PsdOptions());

    image.Save("NormaalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Bijwerken van tekstlayer-tekst veroorzaakt een uitzondering**

{{< highlight java >}}

 // Bijwerken van tekstlayer-tekst veroorzaakt een uitzondering

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_aangepast.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Opslaan van PSD-afbeelding na RotateFlip-operatie produceert een beschadigd bestand dat niet geopend kan worden.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Zou moeten worden uitgevoerd zonder uitzonderingen

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Niets doen

}

{{< /highlight >}}

**PSDNET-539. Uitzondering: Afbeeldingsladen mislukt bij laden van afbeelding met lege Unicode Alpha Namen Resource**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Hier zouden geen uitzonderingen moeten optreden

{

    // niets doen

}

{{< /highlight >}}

**PSDNET-541. Onjuiste uitvoer na wijzigen zichtbaarheid van een LayerGroup**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// veranderingen maken in laagnamen en het opslaan

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Alles uitzetten binnen een groep

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Uitzondering bij laden van PSD-afbeelding: Kleursectie (DropShadow Resource) moet 3 kleurcomponenten bevatten voor RGB of 4 kleurcomponenten voor CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Laag.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Hier zouden geen uitzonderingen moeten optreden

{

    // niets doen

}

{{< /highlight >}}

**PSDNET-536. Uitzondering als geprobeerd wordt te tekenen op een nieuw gemaakte laag als de eenvoudige versie van Constructor wordt gebruikt**

{{< highlight java >}}}

 string outputFile = "output.psd";

int breedte = 100;

int hoogte = 100;

using (var image = new PsdImage(breedte, hoogte))

{

    var laag = new Laag();

    laag.Bottom = hoogte;

    laag.Right = breedte;

    image.AddLayer(laag);

    Grafisch grafisch = new Grafisch(laag);

    grafisch.Clear(Color.Yellow);

    // rechthoek tekenen met Pen-tool

    grafisch.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // nog een rechthoek tekenen met Solid Brush in Blauwe kleur

    grafisch.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}


---
title: Aspose.PSD voor Java 20.3 - Release-opmerkingen
type: docs
weight: 10
url: /nl/java/aspose-psd-voor-java-20-3-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat de release-opmerkingen voor [Aspose.PSD voor Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-20.2/) {{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDJAVA-133|Converteer Adobe Illustrator-bestanden naar PDF's|Functie|
|PSDJAVA-134|Voeg de mogelijkheid toe voor het renderen van verschillende stijlen in één tekstlaag|Functie|
|PSDJAVA-135|Ondersteuning van Zwart-wit Aanpassingslaag|Functie|
|PSDJAVA-137|Ondersteuning toegevoegd voor het exporteren van AI-indeling (Versie 8) naar andere formaten|Functie|
|PSDJAVA-138|Ondersteuning van PassThrough Blendingsmodus-verwerking (alleen gebruikt voor Layer Groep)|Functie|
|PSDJAVA-136|Uitzondering: Afbeeldingsladen mislukt bij het laden van afbeelding met lege Unicode Alpha Namen Resource|Fout|
|PSDJAVA-139|Onjuiste uitvoer na het wijzigen van zichtbaarheid van een Layer Group|Fout|
|PSDJAVA-140|Uitzondering bij het laden van PSD-afbeelding: Kleursectie (DropShadow Resource) moet 3 kleurcomponenten bevatten voor RGB of 4 kleurcomponenten voor CMYK|Fout|
|PSDJAVA-141|Uitzondering als wordt geprobeerd te tekenen op een nieuw gecreëerde laag als de eenvoudige versie van Constructor wordt gebruikt|Fout|
# **Openbare API-wijzigingen**
# **Toegevoegde API's:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **Verwijderde API's:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Gebruikvoorbeelden:**
**PSDJAVA-133. Converteer Adobe Illustrator-bestanden naar PDF's**

{{< highlight java >}}

 String inFile = "rect2_color.ai";

String outFile = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(inFile);

try

{

    aiImage.save(outFile, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Voeg de mogelijkheid toe voor het renderen van verschillende stijlen in één tekstlaag**

{{< highlight java >}}

 String inFilePath = "text212.psd";

String outFilePath = "Output_text212.psd";

PsdImage image = (PsdImage)Image.load(inFilePath);

try

{

    TextLayer textLayer = (TextLayer)image.getLayers()[1];

    IText textData = textLayer.getTextData();

    ITextStyle defaultStyle = textData.producePortion().getStyle();

    ITextParagraph defaultParagraph = textData.producePortion().getParagraph();

    defaultStyle.setFillColor(Color.getDimGray());

    defaultStyle.setFontSize(51);

    textData.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Vetgedrukt",  "Cursief\r",  "Kleineletters" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // bewerk tekststijl "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // bewerk tekststijl "2\r"

    newPortions[2].getStyle().setFauxBold(true); // bewerk tekststijl "Vetgedrukt"

    newPortions[3].getStyle().setFauxItalic(true); // bewerk tekststijl "Cursief\r"

    newPortions[3].getStyle().setBaselineShift(-25); // bewerk tekststijl "Cursief\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // bewerk tekststijl "Kleineletters"

    for (ITextPortion newPortion : newPortions)

    {

        textData.addPortion(newPortion);

    }

    textData.updateLayerData();

    image.save(outFilePath);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Ondersteuning van Zwart-wit Aanpassingslaag**

{{< highlight java >}}

 // Voorbeeld van ondersteuning van toevoegen van de zwart-wit aanpassingslaag tijdens runtime.

String inFileName = "Strepen.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("ZwartWitAanpassingslaag");

    newLayer.setReds(22);

    newLayer.setYellows(92);

    newLayer.setGreens(70);

    newLayer.setCyans(79);

    newLayer.setBlues(7);

    newLayer.setMagentas(28);

    image.save(outFileName, new PsdOptions());

}

finally

{

    image.dispose();

}

// Voorbeeld van de ondersteuning van de zwart-wit aanpassingslaag.

inFileName = "BlackWhiteAdjustmentLayerStrepenMasker.psd";

outFileName = "Output" + inFileName;

PsdImage image1 = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer blwhLayer = (BlackWhiteAdjustmentLayer)image1.getLayers()[1];

    blwhLayer.setReds(15);

    blwhLayer.setYellows(25);

    blwhLayer.setGreens(35);

    blwhLayer.setCyans(10);

    blwhLayer.setBlues(50);

    blwhLayer.setMagentas(105);

    blwhLayer.setUseTint(true);

    blwhLayer.setBwPresetKind(4);

    blwhLayer.setBlackAndWhitePresetFileName("bwPresetFileName");

    blwhLayer.setTintColorRed(60);

    blwhLayer.setTintColorGreen(80);

    blwhLayer.setTintColorBlue(200);

    image1.save(outFileName, new PsdOptions());

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Ondersteuning toegevoegd voor het exporteren van AI-indeling (Versie 8) naar andere formaten**

{{< highlight java >}}

 // Voorbeeld van het exporteren van een AI-bestand naar PSD- en PNG-indeling

String inFileName = "form_8.ai";

String outFileNamePrefix = "form_8_export";

AiImage image = (AiImage)Image.load(inFileName);

try

{

    image.save(outFileNamePrefix + ".psd", new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save(outFileNamePrefix + ".png", pngOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Ondersteuning van PassThrough Blendingsmodus-verwerking (alleen gebruikt voor Layer Groep)**

{{< highlight java >}}

 class LokaleScope

{

    void assertIsTrue(boolean voorwaarde, String bericht)

    {

        if (!voorwaarde)

        {

            throw new FormatException(bericht);

        }

    }

}

LokaleScope lokaleScope = new LokaleScope();

String inFileName = "Appel.psd";

String outFileName = "Output" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    lokaleScope.assertIsTrue(image.getLayers().length >= 23, "Er is geen 23e laag.");

    LayerGroup laag = (LayerGroup)image.getLayers()[23];

    lokaleScope.assertIsTrue(laag != null, "De 23e laag is geen laaggroep.");

    lokaleScope.assertIsTrue(laag.getName().equals("AanpassingsGroep"), "De 23e laag heeft niet de naam 'AanpassingsGroep'.");

    lokaleScope.assertIsTrue(laag.getBlendModeKey() == BlendMode.PassThrough, "Laag AanpassingsGroep moet 'pass through' blendingsmodus hebben.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("OutputAppel.png", pngOptions);

    laag.setBlendModeKey(BlendMode.Normal);

    image.save("Normaal" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormaleOutputAppel.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Uitzondering: Afbeeldingsladen mislukt bij het laden van afbeelding met lege Unicode Alpha Namen Resource**

{{< highlight java >}}

 String inFilePath = "appel.psd";

PsdImage psdImage = null;

try

{

    // Hier zouden geen uitzonderingen moeten voorkomen

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Onjuiste uitvoer na het wijzigen van zichtbaarheid van een Layer Group**

{{< highlight java >}}

 String inFileName = "input.psd";

String outFileName = "output.psd";

// Wijzigingen aanbrengen in laagnamen en opslaan

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer laag = image.getLayers()[i];

        // Alles binnen een groep uitschakelen

        if (laag instanceof LayerGroup)

        {

            laag.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Uitzondering bij het laden van PSD-afbeelding: Kleursectie (DropShadow Resource) moet 3 kleurcomponenten bevatten voor RGB of 4 kleurcomponenten voor CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Laag.psd";

PsdImage image = null;

try

{

    image = (PsdImage)PsdImage.load(inFilePath);

}

finally

{

    if (image != null) image.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Uitzondering als wordt geprobeerd te tekenen op een nieuw gecreëerde laag als de eenvoudige versie van Constructor wordt gebruikt**

{{< highlight java >}}

 String outputFile = "output.psd";

int breedte = 100;

int hoogte = 100;

PsdImage image = new PsdImage(breedte, hoogte);

try

{

    Layer laag = new Laag();

    laag.setOnderkant(hoogte);

    laag.setRechts(breedte);

    image.addLayer(laag);

    Graphics grafisch = new Graphics(laag);

    grafisch.klaar(Color.getGeel());

    // teken een rechthoek met pen tool

    grafisch.tekenRechthoek(new Pen(Color.getRood()), new Rechthoek(30, 10, 40, 80));

    // teken een andere rechthoek met Solid Brush in blauwe kleur

    grafisch.tekenRechthoek(new Pen(new SolideKwast(Color.getBlauw())), new Rechthoek(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}


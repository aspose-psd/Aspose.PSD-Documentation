---
title: Poznámky k vydání Aspose.PSD pro Java 20.3
type: docs
weight: 10
url: /cs/java/aspose-psd-pro-java-20-3-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/) {{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-133|Převod souborů Adobe Illustrator do PDF|Funkce|
|PSDJAVA-134|Přidání schopnosti vykreslit různé styly do jedné vrstvy textu|Funkce|
|PSDJAVA-135|Podpora vrstvy úpravy černobílé|Funkce|
|PSDJAVA-137|Přidání podpory exportu formátu AI (verze 8) do jiných formátů|Funkce|
|PSDJAVA-138|Podpora zpracování režimu mísení PassThrough (používáno pouze pro skupinu vrstev)|Funkce|
|PSDJAVA-136|Výjimka: Chyba při načítání obrázku s prázdným zdrojem Unicode Alpha Names|Chyba|
|PSDJAVA-139|Nesprávný výstup po změně viditelnosti skupiny vrstev|Chyba|
|PSDJAVA-140|Výjimka při načítání obrazu PSD: Barevná sekce (DropShadow Resource) musí obsahovat 3 barevné složky pro RGB nebo 4 barevné složky pro CMYK|Chyba|
|PSDJAVA-141|Výjimka při pokusu vykreslit na nově vytvořenou vrstvu, pokud je použita jednoduchá verze konstruktoru|Chyba|
# **Změny ve veřejném API**
# **Přidaná API:**
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
## **Odebraná API:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Příklady použití:**
**PSDJAVA-133. Převod souborů Adobe Illustrator do PDF**

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

**PSDJAVA-134. Přidání schopnosti vykreslit různé styly do jedné vrstvy textu**

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

    ITextPortion[] newPortions = textData.producePortions(new String[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Malápísmotext" }, defaultStyle, defaultParagraph);

    newPortions[0].getStyle().setUnderline(true); // Upravit styl textu "E=mc"

    newPortions[1].getStyle().setFontBaseline(FontBaseline.Superscript); // Upravit styl textu "2\r"

    newPortions[2].getStyle().setFauxBold(true); // Upravit styl textu "Bold"

    newPortions[3].getStyle().setFauxItalic(true); // Upravit styl textu "Italic\r"

    newPortions[3].getStyle().setBaselineShift(-25); // Upravit styl textu "Italic\r"

    newPortions[4].getStyle().setFontCaps(FontCaps.SmallCaps); // Upravit styl textu "Malápísmotext"

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

**PSDJAVA-135. Podpora vrstvy úpravy černobílé**

{{< highlight java >}}

 // Příklad podpory přidání vrstvy úpravy černobílé za běhu.

String inFileName = "Pruhy.psd";

String outFileName = "Výstup" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    BlackWhiteAdjustmentLayer newLayer = image.addBlackWhiteAdjustmentLayer();

    newLayer.setName("VrstvaČernobílýchÚprav");

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

// Příklad podpory vrstvy úpravy černobílé.

inFileName = "VrstvaČernobílýchÚpravPrustripeMask.psd";

outFileName = "Výstup" + inFileName;

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

    blwhLayer.setBlackAndWhitePresetFileName("BwPresetFileName");

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

**PSDJAVA-137. Přidání podpory exportu formátu AI (verze 8) do jiných formátů**

{{< highlight java >}}

 // Příklad exportu souboru AI do formátu PSD a PNG

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

**PSDJAVA-138. Podpora zpracování režimu mísení PassThrough (používáno pouze pro skupinu vrstev)**

{{< highlight java >}}

 class LocalScope

{

    void assertIsTrue(boolean condition, String message)

    {

        if (!condition)

        {

            throw new FormatException(message);

        }

    }

}

LocalScope localScope = new LocalScope();

String inFileName = "Jablko.psd";

String outFileName = "Výstup" + inFileName;

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    localScope.assertIsTrue(image.getLayers().length >= 23, "Neexistuje 23. vrstva.");

    LayerGroup layer = (LayerGroup)image.getLayers()[23];

    localScope.assertIsTrue(layer != null, "23. vrstva není skupina vrstev.");

    localScope.assertIsTrue(layer.getName().equals("SkupinaÚprav"), "Název 23. vrstvy není 'SkupinaÚprav'.");

    localScope.assertIsTrue(layer.getBlendModeKey() == BlendMode.PassThrough, "Vrstva skupiny Úprav by měla mít režim mísení 'Pass Through'.");

    image.save(outFileName, new PsdOptions());

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("VýstupJablko.png", pngOptions);

    layer.setBlendModeKey(BlendMode.Normal);

    image.save("Normální" + outFileName, new PsdOptions());

    PngOptions pngOptions1 = new PngOptions();

    pngOptions1.setColorType(PngColorType.TruecolorWithAlpha);

    image.save("NormálníVýstupJablko.png", pngOptions1);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Výjimka: Chyba při načítání obrázku s prázdným zdrojem Unicode Alpha Names**

{{< highlight java >}}

 String inFilePath = "jablko.psd";

PsdImage psdImage = null;

try

{

    // Zde bychom neměli dostat výjimky

    psdImage = (PsdImage)Image.load(inFilePath);

}

finally

{

    if (psdImage != null) psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Nesprávný výstup po změně viditelnosti skupiny vrstev**

{{< highlight java >}}

 String inFileName = "vstup.psd";

String outFileName = "výstup.psd";

// Upravit názvy vrstev a uložit

PsdImage image = (PsdImage)Image.load(inFileName);

try

{

    for (int i = 0; i < image.getLayers().length; i++)

    {

        Layer layer = image.getLayers()[i];

        // Vypnout vše uvnitř skupiny

        if (layer instanceof LayerGroup)

        {

            layer.setVisible(false);

        }

    }

    image.save(outFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Výjimka při načítání obrazu PSD: Barevná sekce (DropShadow Resource) musí obsahovat 3 barevné složky pro RGB nebo 4 barevné složky pro CMYK**

{{< highlight java >}}

 String inFilePath = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

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

**PSDJAVA-141. Výjimka pokud se pokusíte kreslit na nově vytvořenou vrstvu, pokud je použita jednoduchá verze konstruktoru**

{{< highlight java >}}

 String outputFile = "výstup.psd";

int width = 100;

int height = 100;

PsdImage image = new PsdImage(width, height);

try

{

    Layer layer = new Layer();

    layer.setBottom(height);

    layer.setRight(width);

    image.addLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.clear(Color.getYellow());

    // nakreslit obdélník s tužkou

    graphic.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // nakreslit další obdélník s plným štětce v modrozelené barvě

    graphic.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    image.save(outputFile);

}

finally

{

    image.dispose();

}

{{< /highlight >}}




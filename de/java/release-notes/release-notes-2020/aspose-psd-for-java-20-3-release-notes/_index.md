---
title: Aspose.PSD für Java 20.3 - Versionshinweise
type: docs
weight: 10
url: /de/java/aspose-psd-fuer-java-20-3-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 20.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-fuer-java-20.2/) {{% /alert %}} 

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-133|Adobe Illustrator-Dateien in PDFs konvertieren|Feature|
|PSDJAVA-134|Füge die Möglichkeit hinzu, verschiedene Stile in einem Textebene zu rendern|Feature|
|PSDJAVA-135|Unterstützung der Schwarz-Weiß-Anpassungsebene|Feature|
|PSDJAVA-137|Hinzufügen der Unterstützung für den Export des AI-Formats (Version 8) in andere Formate|Feature|
|PSDJAVA-138|Unterstützung der Verarbeitung des PassThrough-Mischmodus (nur für Ebenengruppe verwendet)|Feature|
|PSDJAVA-136|Ausnahme: Bild kann nicht geladen werden beim Laden eines Bildes mit leerem Unicode Alpha Names-Ressourcen|Fehler|
|PSDJAVA-139|Falsche Ausgabe nach Ändern der Sichtbarkeit einer Ebenengruppe|Fehler|
|PSDJAVA-140|Ausnahme beim Laden des PSD-Bildes: Farbschnitt (DropShadow-Ressource) muss 3 Farbkomponenten für RGB oder 4 Farbkomponenten für CMYK enthalten|Fehler|
|PSDJAVA-141|Ausnahme, wenn versucht wird, auf eine neu erstellte Ebene zu zeichnen, wenn die einfache Version des Konstruktors verwendet wird|Fehler|
# **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
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
## **Entfernte APIs:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.setVisibleInGroup(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(int)
# **Beispielanwendungen:**
**PSDJAVA-133. Adobe Illustrator-Dateien in PDFs konvertieren**

{{< highlight java >}}

 String Eingabedatei = "rect2_color.ai";

String Ausgabedatei = "rect2_color.ai_output.pdf";

AiImage aiImage = (AiImage)Image.load(Eingabedatei);

try

{

    aiImage.save(Ausgabedatei, new PdfOptions());

}

finally

{

    aiImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-134. Füge die Möglichkeit hinzu, verschiedene Stile in einer Textebene zu rendern**

{{< highlight java >}}

 String EingabeDateiPfad = "text212.psd";

String AusgabeDateiPfad = "Output_text212.psd";

PsdImage Bild = (PsdImage)Image.load(EingabeDateiPfad);

try

{

    Textebene textebene = (Textebene)Bild.getLayers()[1];

    IText textDaten = textebene.getTextDaten();

    ITextStyle standardStil = textDaten.producePortion().getStyle();

    ITextParagraph standardAbsatz = textDaten.producePortion().getParagraph();

    standardStil.setFillColor(Color.getDimGray());

    standardStil.setFontSize(51);

    textDaten.getItems()[1].getStyle().setStrikethrough(true);

    ITextPortion[] neuePortionen = textDaten.producePortions(new String[] { "E=mc",  "2\r",  "Fett",  "Kursiv\r",  "Kleinschreibungstext" }, standardStil, standardAbsatz);

    neuePortionen[0].getStyle().setUnderline(true); // Bearbeite den Textstil "E=mc"

    neuePortionen[1].getStyle().setFontBaseline(FontBaseline.Superscript); // Bearbeite den Textstil "2\r"

    neuePortionen[2].getStyle().setFauxBold(true); // Bearbeite den Textstil "Fett"

    neuePortionen[3].getStyle().setFauxItalic(true); // Bearbeite den Textstil "Kursiv\r"

    neuePortionen[3].getStyle().setBaselineShift(-25); // Bearbeite den Textstil "Kursiv\r"

    neuePortionen[4].getStyle().setFontCaps(FontCaps.SmallCaps); // Bearbeite den Textstil "Kleinschreibungstext"

    for (ITextPortion neuePortion : neuePortionen)

    {

        textDaten.addPortion(neuePortion);

    }

    textDaten.updateLayerData();

    Bild.save(AusgabeDateiPfad);

}

finally

{

    Bild.dispose();

}

{{< /highlight >}}

**PSDJAVA-135. Unterstützung der Schwarz-Weiß-Anpassungsebene**

{{< highlight java >}}

 // Beispiel für die Unterstützung beim Hinzufügen der Schwarz-Weiß-Anpassungsebene zur Laufzeit.

String EingabeDateiName = "Stripes.psd";

String AusgabeDateiName = "Output" + EingabeDateiName;

PsdImage Bild = (PsdImage)Image.load(EingabeDateiName);

try

{

    BlackWhiteAdjustmentLayer neueEbene = Bild.addBlackWhiteAdjustmentLayer();

    neueEbene.setName("BlackWhiteAdjustmentLayer");

    neueEbene.setReds(22);

    neueEbene.setYellows(92);

    neueEbene.setGreens(70);

    neueEbene.setCyans(79);

    neueEbene.setBlues(7);

    neueEbene.setMagentas(28);

    Bild.save(AusgabeDateiName, new PsdOptions());

}

finally

{

    Bild.dispose();

}

// Beispiel für die Unterstützung der Schwarz-Weiß-Anpassungsebene.

EingabeDateiName = "BlackWhiteAdjustmentLayerStripesMask.psd";

AusgabeDateiName = "Output" + EingabeDateiName;

PsdImage Bild1 = (PsdImage)Image.load(EingabeDateiName);

try

{

    BlackWhiteAdjustmentLayer blwhEbene = (BlackWhiteAdjustmentLayer)Bild1.getLayers()[1];

    blwhEbene.setReds(15);

    blwhEbene.setYellows(25);

    blwhEbene.setGreens(35);

    blwhEbene.setCyans(10);

    blwhEbene.setBlues(50);

    blwhEbene.setMagentas(105);

    blwhEbene.setUseTint(true);

    blwhEbene.setBwPresetKind(4);

    blwhEbene.setBlackAndWhitePresetFileName("bwPresetsDateiname");

    blwhEbene.setTintColorRed(60);

    blwhEbene.setTintColorGreen(80);

    blwhEbene.setTintColorBlue(200);

    Bild1.save(AusgabeDateiName, new PsdOptions());

}

finally

{

    Bild1.dispose();

}

{{< /highlight >}}

**PSDJAVA-137. Hinzufügen der Unterstützung für den Export des AI-Formats (Version 8) in andere Formate**

{{< highlight java >}}

 // Beispiel für den Export der AI-Datei in PSD- und PNG-Format

String EingabeDateiName = "form_8.ai";

String AusgabeDateiPrefix = "form_8_export";

AiImage Bild = (AiImage)Image.load(EingabeDateiName);

try

{

    Bild.save(AusgabeDateiPrefix + ".psd", new PsdOptions());

    PngOptions pngOptionen = new PngOptions();

    pngOptionen.setColorType(PngColorType.TruecolorWithAlpha);

    Bild.save(AusgabeDateiPrefix + ".png", pngOptionen);

}

finally

{

    Bild.dispose();

}

{{< /highlight >}}

**PSDJAVA-138. Unterstützung der Verarbeitung des PassThrough-Mischmodus (nur für Ebenengruppe verwendet).**

{{< highlight java >}}

 class LokalerBereich

{

    void istWahr(boolean bedingung, String nachricht)

    {

        if (!bedingung)

        {

            throw new FormatException(nachricht);

        }

    }

}

LokalerBereich lokalerBereich = new LokalerBereich();

String EingabeDateiName = "Apple.psd";

String AusgabeDateiName = "Output" + EingabeDateiName;

PsdImage Bild = (PsdImage)Image.load(EingabeDateiName);

try

{

    lokalerBereich.istWahr(Bild.getLayers().length >= 23, "Es gibt keine 23. Ebene.");

    LayerGroup ebene = (LayerGroup)Bild.getLayers()[23];

    lokalerBereich.istWahr(ebene != null, "Die 23. Ebene ist keine Ebenengruppe.");

    lokalerBereich.istWahr(ebene.getName().equals("AdjustmentGroup"), "Der Name der 23. Ebene ist nicht 'AdjustmentGroup'.");

    lokalerBereich.istWahr(ebene.getBlendModeKey() == BlendMode.PassThrough, "Ebenengruppen-Ebene sollte den 'PassThrough'-Mischmodus haben.");

    Bild.save(AusgabeDateiName, new PsdOptions());

    PngOptions pngOptionen = new PngOptions();

    pngOptionen.setColorType(PngColorType.TruecolorWithAlpha);

    Bild.save("OutputApple.png", pngOptionen);

    ebene.setBlendModeKey(BlendMode.Normal);

    Bild.save("Normal" + AusgabeDateiName, new PsdOptions());

    PngOptions pngOptionen1 = new PngOptions();

    pngOptionen1.setColorType(PngColorType.TruecolorWithAlpha);

    Bild.save("NormalOutputApple.png", pngOptionen1);

}

finally

{

    Bild.dispose();

}

{{< /highlight >}}

**PSDJAVA-136. Ausnahme: Bild kann nicht geladen werden beim Laden eines Bildes mit leerem Unicode Alpha Names-Ressourcen**

{{< highlight java >}}

 String EingabeDateiPfad = "apfel.psd";

PsdImage psdBild = null;

try

{

    // Hier sollten keine Ausnahmen auftreten

    psdBild = (PsdImage)Image.load(EingabeDateiPfad);

}

finally

{

    if (psdBild != null) psdBild.dispose();

}

{{< /highlight >}}

**PSDJAVA-139. Falsche Ausgabe nach Ändern der Sichtbarkeit einer Ebenengruppe**

{{< highlight java >}}

 String EingabeDateiName = "eingabe.psd";

String AusgabeDateiName = "ausgabe.psd";

// Änderungen an den Ebenennamen vornehmen und speichern

PsdImage Bild = (PsdImage)Image.load(EingabeDateiName);

try

{

    for (int i = 0; i < Bild.getLayers().length; i++)

    {

        Layer ebene = Bild.getLayers()[i];

        // Alles in einer Gruppe ausschalten

        if (ebene instanceof LayerGroup)

        {

            ebene.setVisible(false);

        }

    }

    Bild.save(AusgabeDateiName);

}

finally

{

    Bild.dispose();

}

{{< /highlight >}}

**PSDJAVA-140. Ausnahme beim Laden des PSD-Bildes: Farbschnitt (DropShadow-Ressource) muss 3 Farbkomponenten für RGB oder 4 Farbkomponenten für CMYK enthalten**

{{< highlight java >}}

 String EingabeDateiPfad = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

PsdImage Bild = null;

try

{

    Bild = (PsdImage)PsdImage.load(EingabeDateiPfad);

}

finally

{

    if (Bild != null) Bild.dispose();

}       

{{< /highlight >}}

**PSDJAVA-141. Ausnahme, wenn versucht wird, auf einer neu erstellten Ebene zu zeichnen, wenn die einfache Version des Konstruktors verwendet wird**

{{< highlight java >}}

 String AusgabeDatei = "ausgabe.psd";

int Breite = 100;

int Höhe = 100;

PsdImage Bild = new PsdImage(Breite, Höhe);

try

{

    Layer ebene = new Layer();

    ebene.setBottom(Höhe);

    ebene.setRight(Breite);

    Bild.addLayer(ebene);

    Graphics grafik = new Graphics(ebene);

    grafik.clear(Color.getYellow());

    // Zeichne ein Rechteck mit dem Stiftwerkzeug

    grafik.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

    // Zeichne ein weiteres Rechteck mit einer Volltonfarbenbürste in Blau

    grafik.drawRectangle(new Pen(new SolidBrush(Color.getBlue())), new Rectangle(10, 30, 80, 40));

    Bild.save(AusgabeDatei);

}

finally

{

    Bild.dispose();

}

{{< /highlight >}}
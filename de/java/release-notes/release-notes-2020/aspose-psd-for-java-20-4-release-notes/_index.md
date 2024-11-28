---
title: Aspose.PSD für Java 20.4 - Versionshinweise
type: docs
weight: 30
url: /de/java/aspose-psd-für-java-20-4-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-für-java-20.4/) {{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-156|Unterstützung der Ressource 'Vektor-Entstehungsdaten'|Feature|
|PSDJAVA-171|Unterstützung von lclrResource (Einstellung der Blattfarbe)|Feature|
|PSDJAVA-157|Unterstützung von Eigenschaften aus LengthRecord-Daten. (Pfadoperationen (Boolesche Operationen), Index der Form in der Ebene, Anzahl der Bezierknoten)|Feature|
|PSDJAVA-158|Unterstützung der Hintergrundfarbe der Ressource #1010 für Bildbereiche|Feature|
|PSDJAVA-161|Hinzufügen von Füllschichten während der Laufzeit|Feature|
|PSDJAVA-168|Unterstützung von Bildbereichsressource #1009 für Randinformationen.|Feature|
|PSDJAVA-169|Unterstützung von Ebenen in AI-Formatdateien|Feature|
|PSDJAVA-163|Unterstützung des Lesens und Bearbeitens des Überlagerungseffekts für Farbverläufe|Feature|
|PSDJAVA-164|Rendern des Überlagerungseffekts für Farbverläufe|Feature|
|PSDJAVA-149|Aspose.PSD für Java-Fehler beim Abrufen der textData.-Eigenschaft des Textebene|Bug|
|PSDJAVA-166|Korrektur des Speicherns einer PSD-Datei mit Graustufen-Farbmodus und 16 Bit pro Kanal im Graustufen-PSD-Format|Bug|
|PSDJAVA-167|Korrektur des Speicherns einer PSD-Datei mit Graustufen-Farbmodus und 16 Bit pro Kanal im PNG-Format|Bug|
|PSDJAVA-159|Die Änderungen der GradientOverlayEffect.BlendMode-Eigenschaft werden nicht in Photoshop angezeigt.|Bug|

# **Änderungen an der öffentlichen API**
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
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Verwendungsbeispiele:**

**PSDJAVA-156. Unterstützung der Ressource 'Vektor-Entstehungsdaten'**

{{< highlight java >}}

/*

Ein Beispiel zum Lesen und Ändern einer Ressource für Vektor-Entstehungsdaten.

*/

// Behalte die Methoden im lokalen Bereich für Einfachheit

class LokaleBereichserweiterung

{

    VogkResource findeErsteVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("VogkResource nicht gefunden.");

        }

        return vogkResource;

    }

}

LokaleBereichserweiterung $ = new LokaleBereichserweiterung();

String inPsdDateiPfad = "VektorOriginationDataResource.psd";

String outPsdDateiPfad = "out_VektorOriginationDataResource_.psd";

// Lade eine PSD-Datei, die eine vordefinierte VOGK-Ressource enthält

PsdImage psdImage = (PsdImage)Image.load(inPsdDateiPfad);

try

{

    // Finde die erste VogkResource in den Ressourcen der vordefinierten Ebene

    VogkResource vogkResource = $.findeErsteVogkResource(

            psdImage.getLayers()[1].getResources());

    // Überprüfe vordefinierte Ressourceneigenschaften

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource falsch gelesen.");

    }

    // Ändere einige VogkResource-Eigenschaften

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Speichere eine modifizierte Kopie der geladenen PSD-Datei am Pfad

    psdImage.save(outPsdDateiPfad);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Unterstützung von lclrResource (Einstellung der Blattfarbe)**

{{< highlight java >}}

/*

Ein Beispiel zur Verwendung von Layerebenenfarbe zur visuellen Hervorhebung von Ebenen. 

Zum Beispiel können Sie einige Ebenen in PSD aktualisieren und dann durch Farbe die Ebene hervorheben, die Sie beachten möchten.

*/

class LokaleBereichserweiterung

{

    void überprüfeSheetFarbenUndUmkehr(Short[] sheetColors, PsdImage psdImage)

    {

        int ebenenanzahl = psdImage.getLayers().length;

        for (int ebenenIndex = 0; ebenenIndex < ebenenanzahl; ebenenIndex++)

        {

            Layer ebene = psdImage.getLayers()[ebenenIndex];

            for (LayerResource ebeneRessource : ebene.getResources())

            {

                if (!(ebeneRessource instanceof LclrResource))

                {

                    continue;

                }

                // Die lclr-Ressource ist immer in der Ressourcenliste der psd-Datei vorhanden.

                LclrResource ressource = (LclrResource)ebeneRessource;

                if (ressource.getColor() != sheetColors[ebenenIndex])

                {

                    throw new Exception("Blattfarbe falsch gelesen");

                }

                // Umkehrung der Stylesheet-Farben. Festlegen der Farbmarkierung 

                ressource.setColor(sheetColors[ebenenanzahl - ebenenIndex - 1]);

                break;

            }

        }

    }

}

LokaleBereichserweiterung $ = new LokaleBereichserweiterung();

String inPsdDateiPfad = "AlleLclrResourceFarben.psd";

String outPsdDateiPfad = "AlleLclrResourceFarbenUmgekehrt.psd";

// In der Datei sind die Farben der Ebenenhervorhebung in dieser Reihenfolge 

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// Lade eine PSD-Datei, die eine vordefinierte LclrResource enthält

PsdImage psdImage = (PsdImage)Image.load(inPsdDateiPfad);

try

{

    $.überprüfeSheetColorsUndUmkehr(sheetColors, psdImage);

    psdImage.save(outPsdDateiPfad, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Lade eine gerade gespeicherte PSD-Datei

PsdImage psdImage1 = (PsdImage)Image.load(outPsdDateiPfad);

try

{

    // Umkehren der Farben

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.überprüfeSheetColorsUndUmkehr(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Unterstützung von Eigenschaften aus LengthRecord-Daten. (Pfadoperationen (Boolesche Operationen), Index der Form in der Ebene, Anzahl der Bézierknoten)**

{{< highlight java >}}

/*

Ein Beispiel zur Änderung von Pfadoperationen beim Arbeiten mit Formen. Das Programm liest

vordefinierte Vektorpfaddatensätze (LengthRecord) und ändert ihre Pfadoperationen, um dann das Modifizierte

Dokument als neue PSD-Datei zu speichern.

*/

String inPsdDateiPfad = "Pfadoperationsform.psd";

String outPsdDateiPfad = "out_" + inPsdDateiPfad;

// Lade eine PSD-Datei, die eine vordefinierte vsms-Ressource enthält

PsdImage psdImage = (PsdImage)Image.load(inPsdDateiPfad);

try

{

    // Suche die erste VsmsResource in den Ressourcen der vordefinierten Ebene

    VsmsResource ressource = null;

    for (LayerResource ebeneRessource : psdImage.getLayers()[1].getResources())

    {

        if (ebeneRessource instanceof VsmsResource)

        {

            ressource = (VsmsResource)ebeneRessource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)ressource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)ressource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)ressource.getPaths()[11];

    // Ändere die Art und Weise, wie Formen kombiniert werden

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Speichere eine modifizierte Kopie der geladenen PSD-Datei am Pfad

    psdImage.save(outPsdDateiPfad);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Unterstützung der Hintergrundfarbe der Ressource #1010 für Bildbereiche**

{{< highlight java >}}

/*

Ein Beispiel zum Lesen und Ändern einer Hintergrundfarben-Ressource.

*/

String inPsdDateiPfad = "Eingabe.psd";

String outPsdDateiPfad = "Ausgabe.psd";

// Lade eine PSD-Datei, die eine vordefinierte Hintergrundfarben-Ressource enthält

PsdImage psdImage = (PsdImage)Image.load(inPsdDateiPfad);

try

{

    BackgroundColorResource hintergrundfarbenRessource = null;

    for (ResourceBlock bildRessource : psdImage.getImageResources())

    {

        if (bildRessource instanceof BackgroundColorResource)

        {

            hintergrundfarbenRessource = (BackgroundColorResource)bildRessource;

            break;

        }

    }

    if (hintergrundfarbenRessource == null)

    {

        throw new Exception("Hintergrundfarben-Ressource nicht gefunden");

    }

    // Aktualisiere die Farbe der Hintergrundfarben-Ressource

    hintergrundfarbenRessource.setColor(Color.getDarkRed());

    // Speichere eine modifizierte Kopie der geladenen PSD-Datei am Pfad

    psdImage.save(outPsdDateiPfad);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Hinzufügen von Füllschichten während der Laufzeit**

{{< highlight java >}}

/*

Ein Beispiel zum Hinzufügen von Füllschichten verschiedener Typen zu einem Photoshop-Dokument.

*/

String outPsdDateiPfad = "Ausgabe.psd";

// Erstelle ein Photoshop-Dokument mit einer leeren Leinwand

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Füge Füllschichten verschiedener Typen zu PSD hinzu

    FillLayer farbFüllschicht = FillLayer.createInstance(FillType.Color);

    farbFüllschicht.setDisplayName("Farbfüllschicht");

    psdImage.addLayer(farbFüllschicht);

    FillLayer gradientFüllschicht = FillLayer.createInstance(FillType.Gradient);

    gradientFüllschicht.setDisplayName("Verlaufsfüllschicht");

    psdImage.addLayer(gradientFüllschicht);

    FillLayer musterFüllschicht = FillLayer.createInstance(FillType.Pattern);

    musterFüllschicht.setDisplayName("Mustergüllschicht");


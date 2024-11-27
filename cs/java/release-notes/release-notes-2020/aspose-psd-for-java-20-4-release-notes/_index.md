---
title: Aspose.PSD pro Java 20.4 - Poznámky k vydání
type: docs
weight: 30
url: /cs/java/aspose-psd-pro-java-20-4-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDJAVA-156|Podpora zdroje 'Vector Origination Data'|Funkce|
|PSDJAVA-171|Podpora lclrResource (Nastavení barvy listu)|Funkce|
|PSDJAVA-157|Podpora vlastností z dat délky záznamu (Operace na cestě (logické operace), index tvaru ve vrstvě, počet záznamů bezierových uzlů)|Funkce|
|PSDJAVA-158|Podpora zdroje sekce obrázku #1010 Barva pozadí|Funkce|
|PSDJAVA-161|Přidání plnících vrstev za běhu|Funkce|
|PSDJAVA-168|Podpora zdroje sekce obrázku #1009 Informace o ohraničení.|Funkce|
|PSDJAVA-169|Podpora vrstev ve formátech AI souborů|Funkce|
|PSDJAVA-163|Podpora čtení a úprav gradientního překryvu vrstvy efektů|Funkce|
|PSDJAVA-164|Vytvoření gradientního překryvu vrstvy efektů|Funkce|
|PSDJAVA-149|Chyba Aspose.PSD pro Java při získávání vlastnosti textData.items textové vrstvy|Chyba|
|PSDJAVA-166|Oprava ukládání obrazu PSD s režimem barvy Grayscale a 16 bitů na kanál do formátu PSD v režimu Grayscale|Chyba|
|PSDJAVA-167|Oprava ukládání obrazu PSD s režimem barvy Grayscale a 16 bitů na kanál do formátu PNG|Chyba|
|PSDJAVA-159|Změny vlastnosti GradientOverlayEffect.BlendMode se nezobrazí v Photoshopu.|Chyba|
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
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Příklady použití:**

**PSDJAVA-156. Podpora zdroje 'Vector Origination Data'**

{{< highlight java >}}

 /*

Příklad čtení a úpravy zdroje Vector Origination Data.

*/

// Udržujte metody v lokálním rozsahu pro jednoduchost

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

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

            throw new Exception("Zdroj VogkResource nebyl nalezen.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Načtení souboru PSD obsahujícího předdefinovaný zdroj VOGK

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Najděte první VogkResource v zdrojích předdefinované vrstvy

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Ověření vlastností předdefinovaného zdroje

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("Zdroj VogkResource byl špatně přečten.");

    }

    // Upravit některé vlastnosti zdroje Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Uložení upravené kopie načteného souboru PSD na cestu

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Podpora lclrResource (Nastavení barvy listu)**

{{< highlight java >}}

 /*

Příklad použití barvy listu vrstvy k vizuálnímu zvýraznění vrstev. Například můžete

aktualizovat některé vrstvy v PSD a poté zvýraznit barvou vrstvu, na kterou chcete upozornit.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // lcrl zdroj je vždy přítomen v seznamu zdrojů souboru PSD.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Barva listu byla špatně přečtena");

                }

                // Změna povahy barev listů. Nastavení barvy vrstvy.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Barvy vrstevních zvýraznění jsou v souboru v této pořadí

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

// Načtení souboru PSD obsahujícího předdefinovaný LclrResource

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Načtení právě uloženého souboru PSD

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Obrácení barev

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Podpora vlastností z dat délky záznamu. (Operace na cestě (logické operace), index tvaru ve vrstva, počet záznamů bezierových uzlů)**

{{< highlight java >}}

 /*

Příklad změny operačních cest při práci s tvary. Program čte

předdefinované záznamy vektorové cesty (LengthRecord) a mění jejich operační cesty, pak uloží

upravenou kopii dokumentu jako nový soubor PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Načtení souboru PSD obsahujícího předdefinovaný vsms zdroj

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Najděte první VsmsResource v zdrojích předdefinované vrstvy

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Změna způsobu, jakým jsou tvary kombinovány

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Uložení upravené kopie načteného souboru PSD na cestu

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Podpora zdroje sekce obrázku #1010 Barva pozadí**

{{< highlight java >}}

 /*

Příklad čtení a úpravy zdroje barvy pozadí.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Načtení souboru PSD obsahujícího předdefinovaný zdroj barvy pozadí

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Zdroj BackgroundColorResource nebyl nalezen");

    }

    // Aktualizace barvy zdroje barvy pozadí

    backgroundColorResource.setColor(Color.getDarkRed());

    // Uložení upravené kopie načteného souboru PSD na cestu

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Přidání plnících vrstev za běhu**

{{< highlight java >}}

 /*

Příklad přidání plnících vrstev různých typů do dokumentu Photoshopu.

*/

String outPsdFilePath = "output.psd";

// Vytvoření dokumentu Photoshopu s prázdným plátnem

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Přidání plnících vrstev různých typů do PSD

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Vrstva vyplnění barvou");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Vrstva vyplnění přechodem");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Vrstva vyplnění vzorem");

    patternFillLayer.setOpacity((byte)50);


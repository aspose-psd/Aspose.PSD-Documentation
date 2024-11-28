---
title: Aspose.PSD עבור Java 20.4 - הערות הגרסה
type: docs
weight: 30
url: /he/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} דף זה מכיל הערות הגרסה עבור [Aspose.PSD עבור Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDJAVA-156|תמיכה במשאב ממקור 'נתוני מוצא וקצבת' |תכונה|
|PSDJAVA-171|תמיכה ב-lclrResource (הגדרת צבע דף) |תכונה|
|PSDJAVA-157|תמיכה במאפיינים מנתון אורך (פעולות נתיב (פעולות בוליאניות), מיקום של הצורה בשכבה, ספירת רשומות קשר בזיג הבזיות)|תכונה|
|PSDJAVA-158|תמיכה במשאב מקטע תמונה #1010 צבע רקע|תכונה|
|PSDJAVA-161|הוספת שכבות מילוי בזמן ריצה|תכונה|
|PSDJAVA-168|תמיכה במשאב מקטע תמונה #1009 מידע גבול|תכונה|
|PSDJAVA-169|תמיכה בשכבות בקבצי עיצוב AI|תכונה|
|PSDJAVA-163|תמיכה בקריאה ועריכה של השפעת שכבת צנתות מעביף|תכונה|
|PSDJAVA-164|הצגת השפעת שכבת צנתות מעביף|תכונה|
|PSDJAVA-149|שגיאת Aspose.PSD עבור java כאשר מקבלים את מאפיין textData.items של שכבת טקסט|באג|
|PSDJAVA-166|תיקון לשמירת תמונת PSD עם צבע Grayscale ו-16 ביט לערוץ אל פורמט PSD בגוון Grayscale|באג|
|PSDJAVA-167|תיקון לשמירת תמונת PSD עם צבע Grayscale ו-16 ביט לערוץ אל פורמט PNG|באג|
|PSDJAVA-159|שינויים במאפיין BlendMode של GradientOverlayEffect לא מוצגים בפוטושופ|באג|
# **שינויים ב-API הפומבי**
# **API חדשים:**
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
## **APIs שהוסרו:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **דוגמאות שימוש:**

**PSDJAVA-156. תמיכה במשאב 'נתוני מוצא וקצבת'**

{{< highlight java >}}

 /*

דוגמא לקריאה ושינוי משאב נתוני מוצא וקצבת.

*/

// שמירה של הפעולות בסביבה המקומית לצורך פשטות

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

            throw new Exception("אין אפשרות למצוא את המוצא VogkResource.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// טעינת קובץ PSD הכולל מוצא VOGK מוגדר מראש

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // מציאת המוצא הראשון של VogkResource במשאבים של השכבה המוגדרת מראש

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // אימות מאפייני משאב מוגדרים מראש

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("המוצא VogkResource נקרא בצורה שגויה.");

    }

    // שינוי מספר מאפיינים של משאב מוצא

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // שמירת הודפסה מודיפיציה של קובץ PSD שנטען בנתיב

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. תמיכה ב-lclrResource (הגדרת צבע דף)**

{{< highlight java >}}

 /*

דוגמא לשימוש בצבעי גליון שכבה כדי להדגיש באופן חזותי שכבות. לדוגמה אפשר לעדכן

כמה שכבות ב-PSD ולאחר מכן להדגיש בצבע כאשר רוצים למשוך

תשומת לב אליהן.

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

                // המשאב lcrl המופיע תמיד ברשימת המשאבים לקובץ ה-PSD.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("צבע דף נקרא בצורה שגויה");

                }

                // הפוך לצבעי גליון.     הגהות של צבעי שכבה

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// בקובץ צבעי שכבות שמתוארים בסדר זה

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

// טעינת קובץ PSD הכולל משאב LclrResource מוגדר מראש

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

// טעינת קובץ PSD שמירה

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // הפך צבעים

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. תמיכה במאפיינים מנתון אורך (פעולות נתיב (פעולות בוליאניות), מיקום של הצורה באירוע, מספר רשומות ביזיר של הצורה)**

{{< highlight java >}}

 /*

דוגמא לשינויי פעולות הנתיבים בעת העבודה עם צורות. התוכנית קורא

רשומות נתונים וכאשר סיימה משנה את פעולות הנתיב ושומרת עותק מודיפיציה של המסמך כקובץ PSD חדש.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// טעינת קובץ PSD הכולל משאב vsms מוגדר מראש

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // מציאת המשאב VsmsResource הראשון במשאבים של השכבה המוגדרת מראש

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers
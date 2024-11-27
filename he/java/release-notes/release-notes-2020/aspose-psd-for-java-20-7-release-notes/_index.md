---
title: הודעות השחרור ל- Aspose.PSD עבור גרסת Java 20.7
type: docs
weight: 50
url: /he/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל את ההערות השחרור עבור [Aspose.PSD עבור Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDJAVA-231|תמיכה בהוספת אפקט Stroke בזמן ריצה|תכונה|
|PSDJAVA-249|תמיכה במשאבי lnk2 / lnk3 (משאבי שכבת Smart Object)|תכונה|
|PSDJAVA-247|שינוי בהודעת השגיאה בניסיון לפתוח פורמטים שאינם נתמכים כתמונה|שיפור|
|PSDJAVA-235|בעת שמירת קובץ PSD לאחר יצירת קבוצת שכבה חדשה, מתקבלת אזהרת Photoshop בפתיחת הקובץ.|באג|
|PSDJAVA-236|שגיאה במהלך שמירת LayerMask|באג|
|PSDJAVA-237|מסכת חיתוך לא מחולקת לתיקייה|באג|
|PSDJAVA-238|לא ניתן לפתוח קובץ עם Aspose.PSD עבור Java|באג|
|PSDJAVA-239|שגיאת ניסיון לשמור תמונה בהמרת PSD ל-PDF|באג|
|PSDJAVA-240|פעולת חיתוך משווקת מסלול החיתוך בתמונת PSD|באג|
|PSDJAVA-241|תקלת NullReference בניסיון לשמור קובץ PSD מסוים עם התופעה הספציפית|באג|
|PSDJAVA-243|Aspose.PSD מחזירה "נכון" על Image.CanLoad(pdfStream)|באג|
|PSDJAVA-244|בעיות בהצגת שכבות ב-PNG שנוצרו|באג|
|PSDJAVA-245|שגיאה בגישה אל TextData|באג|
|PSDJAVA-246|ImageSaveException במהלך שמירה של PSD|באג|
# **שינויים ב-API הציבורי**
# **API חדשות:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **API מוחלט:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
## **דוגמאות שימוש:**

**PSDJAVA-231. תמיכה בהוספת אפקט Stroke בזמן ריצה**
{{< highlight java >}}
//דוגמה זו מדגימה כיצד להוסיף אפקט stroke (גבול) לשכבות קיימות של קובץ PSD ב-Java.
//יש שלושה סוגי stroke: צבע, שטחי צבע ותבנית. כל סוג מאפשר שלושה דרכים (מיקומים) בהם הגבול נוצר: בתוך, במרכז ובחוץ.
//דוגמה זו מדגימה שימוש בכל אלו המקרים.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";
 
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;
 
// נוסיף צבע, במקום Inside
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 2. מוסיף צבע, במיקום בחוץ
    strokeEffect = psdImage.getLayers()[2].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Outside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 3. מוסיף צבע, במרכז
    strokeEffect = psdImage.getLayers()[3].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Center);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());
 
    // 4. מוסיף ריסוף מעלות, במיקום בפנים
    strokeEffect = psdImage.getLayers()[4].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(false);
    gradientFillSettings.setAngle(90);
 
    // 5. מוסיף ריסוף מעלות, במיקום מחוץ
    strokeEffect = psdImage.getLayers()[5].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Outside);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(90);
 
    // 6. מוסיף ריסוף מעלות, במרכז
    strokeEffect = psdImage.getLayers()[6].getBlendingOptions().addStroke(FillType.Gradient);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Center);
    gradientFillSettings = (IGradientFillSettings)strokeEffect.getFillSettings();
    gradientFillSettings.setAlignWithLayer(true);
    gradientFillSettings.setAngle(0);
 
    // 7. מוסיף ריסוף מעלות, במיקום בפנים
    strokeEffect = psdImage.getLayers()[7].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(5);
    strokeEffect.setPosition(StrokePosition.Inside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(200);
 
    // 8. מוסיף ריסוף מעלות, במיקום מחוץ
    strokeEffect = psdImage.getLayers()[8].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Outside);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(100);
 
    // 9. מוסיף ריסוף מעלות, במרכז
    strokeEffect = psdImage.getLayers()[9].getBlendingOptions().addStroke(FillType.Pattern);
    strokeEffect.setSize(10);
    strokeEffect.setPosition(StrokePosition.Center);
    patternFillSettings = (IPatternFillSettings)strokeEffect.getFillSettings();
    patternFillSettings.setScale(75);
 
    psdImage.save(dstPngPath, new PngOptions());
}
finally
{
    psdImage.dispose();
}
{{< /highlight >}}

**(המשך בתגובה)****PSDJAVA-249. תמיכה במשאבי lnk2 / lnk3 (משאבי שכבת Smart Object)**
{{< highlight java >}}
// דוגמה זו מדגימה כיצד לעבוד עם משאבי Smart Object (בגדול Lnk2Resource).
// התוכנית טוענת מסמכי פוטושופ מרובים וייצוא אובייקטי החכמים שלהם
// לפורמטי קובץ Raster. כמו כן, הקוד מדגים שימוש בשיטות הציבוריות של Lnk2Resource.

class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("Actual value %s are not equal to expected %s.", actual, expected));
        }
    }
 
    // שומר את הנתונים של Smart Object לקובץ PSD
    void saveSmartObjectData(String filePath, byte[] data)
    {
        FileStreamContainer container = FileStreamContainer.createFileStream(filePath, false);
        try
        {
            container.write(data);
        }
        finally
        {
            container.dispose();
        }
    }
 
    // טוען את נתוני ה-Smart Object החדשים מקובץ
    byte[] loadNewData(String filePath)
    {
        FileStreamContainer container = FileStreamContainer.openFileStream(filePath);
        try
        {
            return container.toBytes();
        }
        finally
        {
            container.dispose();
        }
    }
 
    // מקבל ומגדיר מאפיינים של Lnk2 / Lnk3 Resource ומקורות המידע שלו מ-LiFD בתמונת PSD
    void exampleOfLnk2ResourceSupport(
            String fileName,
            int dataSourceCount,
            int length,
            int newLength,
            Object[] dataSourceExpectedValues)
    {
        String srcPsdPath = fileName;
        String dstPsdPath = "out_" + fileName;
 
        PsdImage image = (PsdImage)Image.load(srcPsdPath);
        try
        {
            // מחפש Lnk2Resource 
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;
 
                    // בודק את המאפיינים של Lnk2Resource
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);
 
                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // מוודא ומשנה את המאפיינים של LiFdDataSource
                        LiFdDataSource lifdSource = lnk2Resource.get_Item(i);
                        Object[] expected = (Object[])dataSourceExpectedValues[i];
                        assertAreEqual(LinkDataSourceType.liFD, lifdSource.getType());
                        assertAreEqual(expected[0], lifdSource.getUniqueId().toString());
                        assertAreEqual(expected[1], lifdSource.getOriginalFileName());
                        assertAreEqual(expected[2], lifdSource.getFileType().trim());
                        assertAreEqual(expected[3], lifdSource.getFileCreator().trim());
                        assertAreEqual(expected[4], lifdSource.getData().length);
                        assertAreEqual(expected[5], lifdSource.getAssetModTime());
                        assertAreEqual(expected[6], lifdSource.getChildDocId());
                        assertAreEqual(expected[7], lifdSource.getVersion());
                        assertAreEqual(expected[8], lifdSource.hasFileOpenDescriptor());
                        assertAreEqual(expected[9], lifdSource.getLength());
 
                        if (lifdSource.hasFileOpenDescriptor())
                        {
                            assertAreEqual(-1, lifdSource.getCompId());
                            assertAreEqual(-1, lifdSource.getOriginalCompId());
                            lifdSource.setCompId(Integer.MAX_VALUE);
                        }
 
                        saveSmartObjectData(
                                fileName + "_" + lifdSource.getOriginalFileName(),
                                lifdSource.getData());
                        lifdSource.setData(loadNewData("new_" + lifdSource.getOriginalFileName()));
                        assertAreEqual(expected[10], lifdSource.getLength());
 
                        lifdSource.setChildDocId(UUID.randomUUID().toString());
                        lifdSource.setAssetModTime(Double.MAX_VALUE);
                        lifdSource.setFileType("test");
                        lifdSource.setFileCreator("me");
                    }
 
                    assertAreEqual(newLength, lnk2Resource.getLength());
                    break;
                }
            }
 
            // בודק שנמצא Lnk2Resource
            assertAreEqual(true, lnk2Resource != null);
 
            // יוצר עותק דמי של PSD
            if (image.getBitsPerChannel() < 32) // 32 ביט לערוץ אין תמיכה בשמירה עדיין
            {
                image.save(dstPsdPath, new PsdOptions(image));
            }
        }
        finally
        {
            image.dispose();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();
 

Object[] Lnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "00af34a0-a90b-674d-a821-73ee508c5479",
                                "rgb8_2x2.png",
                                "png",
                                "",
                                0x53,
                                0d,
                                "",
                                7,
                                true,
                                0x124L,
                                0x74cL
                        }
        };
 
Object[] LayeredLnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "69ac1c0d-1b74-fd49-9c7e-34a7aa6299ef",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
                new Object[]
                        {
                                "5a7d1965-0eae-b24e-a82f-98c7646424c2",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694L,
                                0x10dd4L
                        },
        };
 
Object[] LayeredLnk3ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "2fd7ba52-0221-de4c-bdc4-1210580c6caa",
                                "panama-papers.jpg",
                                "JPEG",
                                "",
                                0xF56B,
                                0d,
                                "xmp.did:BDE940CBF51B11E59D759CDA690663E3",
                                7,
                                true,
                                0xF694l,
                                0x10dd4L
                        },
                new Object[]
                        {
                                "372d52eb-5825-8743-81a7-b6f32d51323d",
                                "huset.jpg",
                                "JPEG",
                                "",
                                0x9d46,
                                0d,
                                "xmp.did:0F94B342065B11E395B1FD506DED6B07",
                                7,
                                true,
                                0x9E60L,
                                0xc60cL
                        },
        };
 
// דוגמה זו מדגימה כיצד לקבל ולקבע מאפיינים של Lnk2 Resource ושל LiFD שלו ל-8 ביט בערוצים
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
 
// דוגמה זו מדגימה כיצד לקבל ולקבע מאפיינים של Lnk3 Resource ושל LiFD שלו ל-32 ביט בערוצים
$.exampleOfLnk2ResourceSupport("Layered PSD file smart objects.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk3ResourceSupportCases);
 
// דוגמה זו מדגימה כיצד לקבל ולקבע מאפיינים של Lnk2 Resource ושל LiFD שלו ל-16 ביט בערוצים
$.exampleOfLnk2ResourceSupport("LayeredSmartObjects16bit.psd", 2, 0x19504, 0x0001d3e0, LayeredLnk2ResourceSupportCases);
{{< /highlight >}}

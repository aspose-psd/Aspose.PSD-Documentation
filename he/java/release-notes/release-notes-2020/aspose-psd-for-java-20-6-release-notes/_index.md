---
title: Aspose.PSD עבור Java 20.6 - הערות גרסה
type: docs
weight: 50
url: /he/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} דף זה מכיל את הערות הגרסה עבור [Aspose.PSD עבור Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDJAVA-216|תמיכה ב-LnkEResource (משאב של שכבת Smart Object)|תכונה|
|PSDJAVA-219|תמיכה ב-britResource (משאב של שכבת בהירות/ניגודיות)|תכונה|
|PSDJAVA-222|העברת הגדרת DefaultReplacementFont לתוך מחלקת ImageOptionsBase|שדרוג|
|PSDJAVA-217|שינוי גודל קבצי PSD פועל בלא נכון אם יש מסכה בשכבת ההתאמה שיש לה גבולות ריקים|באג|
|PSDJAVA-218|עדכון שכבת PSD עם מצב RGB של 16 ביט לערוך שכבות רק בתצוגה מקדימה|באג|
|PSDJAVA-220|שינויים במסיכות השכבת PSD מתוותרים בשמירה|באג|
|PSDJAVA-221|סדר שכבה שגוי לאחר הוספת קבוצת שכבות לקבוצת שכבות ריקה|באג|
|PSDJAVA-223|חריגה בעת טעינת קובץ PSD מסוים עם משאב LnkE מרוכז ומאפיין adobeStockLicenseState|באג|
|PSDJAVA-224|שמירת קובץ AI כמבנה Jpeg2000 לא עובדה|באג|
|PSDJAVA-225|קבוצת שכבות עם מצב מעבר לא מתוקן אינה מופיעה|באג|
|PSDJAVA-226|חריגת NullReference בעת ניסיון להמיר קובץ Psd ספציפי לתמונה|באג|
|PSDJAVA-227|חריגה Overflow בעת ניסיון לפתוח קובץ Psd ספציפי|באג|

# **שינויים ציבוריים ב-API**
# **APIs שנוספו:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource

## **APIs שהוסרו:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)

# **דוגמאות שימוש:**

**PSDJAVA-216: תמיכה ב-LnkEResource (משאב של שכבת Smart Object)**

{{< highlight java >}}

 // דוגמא שממחישה קישור בין סוגי נכסים שונים (תמונות raster, ספריות CC) ל-PSD.

// גם API של LnkeResource נחשב.

// מחלקה ששומרת פעולות בנוסף

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport פועל בדרך שגויה.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // הדוגמה מדגימה איך לקבל ולהגדיר מאפיינים של ה-LnkE של Photoshop Psd

    // Resource המכיל מידע על קובץ חיצוני שקושר.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,				      

...

{{< /highlight >}}

**PSDJAVA-219: תמיכה ב-britResource (משאב של שכבת בהירות/ניגודיות)**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-217: שינוי גודל קבצי PSD פועל בלא נכון אם יש מסכה בשכבת ההתאמה שיש לה גבולות ריקים**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-218: שכבת Psd עם מצב RGB של 16 ביט לערך שכבות רק בתצוגה מקדימה**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-220: שינויים במסיכות שכבת PSD מתוותרים בשמירה**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-221: סדר שכבה שגוי לאחר הוספת קבוצת שכבות לקבוצת שכבות ריקה**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-223: חריגה בעת טעינת קובץ PSD מסוים עם השאמת LnkE מרוכז ומאפיין adobeStockLicenseState**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-224: שמירת קובץ AI כמבנה Jpeg2000 לא עובדה**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-225: קבוצת שכבות עם מצב מעבר לא מוצגת**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-226: חריגת NullReference בעת ניסיון להמיר קובץ Psd ספציפי לתמונה**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-227: חריגה Overflow בעת ניסיון לפתוח קובץ Psd ספציפי**

{{< highlight java >}}

...

{{< /highlight >}}

**PSDJAVA-222: העברת הגדרת DefaultReplacementFont לתוך מחלקת ImageOptionsBase**

{{< highlight java >}}

...

{{< /highlight >}}**PSDJAVA-222: העברת הגדרת DefaultReplacementFont לתוך מחלקת ImageOptionsBase**

{{< highlight java >}}

...

{{< /highlight >}}
---
title: Aspose.PSD עבור .NET 24.6 - הודעות לשחרור
type: docs
weight: 70
url: /he/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הודעות לשחרור עבור [Aspose.PSD עבור .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Key**     | **Summary**                                                                         | **Category** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | ליישום תמיכה בשכבת מפת הצבעים                                                                        | תכונה       |
| PSDNET-1670 | [פורמט AI] הוספת תמיכה בנתוני מטא XPacket לפורמט AI                                                | תכונה       |
| PSDNET-1831 | ליישום סוגי גלילה שוחקת, דחיף, וסיבוב                                                   | תכונה       |
| PSDNET-1653 | מצבי Rgb ו-Lab לא יכולים להכיל פחות מ-3 ערוצים ויותר מ-4 ערוצים בקובץ עם שכבות ArtBoard                              | באגים       |
| PSDNET-1775 | גבול האזור של העיבוד מעלה חייב להיות חיובי. (פרמטר 'אזור לעיבוד') בעיבוד של קובץ ספציפי                  | באגים       |
| PSDNET-2052 | ההרחבה מעבר לתמונת התשריט מיוחסת לאחר השמירה. נתונים אבודים אך התצוגה נראית נכון                       | באגים       |

## **שינויים ציבוריים ב- API**
# **API חדשים:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **API שהוסרו:**
- אין

## **דוגמאות שימוש:**

**PSDNET-1450. ליישום תמיכה בשכבת מפת הצבעים**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // הוספת שכבת כיוון מטרה.
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// בדיקת השינויים שהתקבלו
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("מותאם אישית", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "האובייקטים אינם שווים.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [פורמט AI] הוספת תמיכה בנתוני מטא XPacket לפורמט AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("האובייקטים אינם שווים.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("אובייקט נבדק הוא null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "אדובי אילוסטרייטור CC 22.1 (חלון)";
string expectedNPages = "1";
string expectedUnit = "פיקסלים";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // נתוני ה-Metadata Xmp נוספו.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // כעת אנחנו יכולים לגשת לחבילות ה-Xmp של קבצי AI.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // ויש לנו גישה לתוכן של חבילות אלו.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}

**PSDNET-1831. ליישום סוגי גלילה שוחקת, דחיף, וסיבוב**

{{< highlight csharp >}}
string[] files = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string prefix in files)
{
    string sourceFile = Path.Combine(baseFolder, prefix + ".psd");
    string outputFile = Path.Combine(outputFolder, prefix + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(outputFile, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. מצבי Rgb ו-Lab לא יכולים להכיל פחות מ-3 ערוצים ויותר מ-4 ערוצים בקובץ עם שכבות ArtBoard**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Rgb5Channels.psb");
string outputFile = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(sourceFile))
{
    // כאן לא צריך להיות חריגה
    image.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1775. גבול האזור של העיבוד מעלה חייב להיות חיובי. (פרמטר 'אזור לעיבוד') בעיבוד של קובץ ספציפי**

{{< highlight csharp >}}
string sourceFile = @"BANNERS_2_Intel-Gamer_psak.psd";
string outputFile = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(sourceFile, psdLoadOptions))
{
    image.Save(outputFile);
    // לא צריך להיות חריגה
}
{{< /highlight >}}

**PSDNET-2052. ההרחבה מעבר לתמונת התשריט מיוחסת לאחר השמירה. נתונים אבודים אך התצוגה נראית נכון**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "bigfile.psd");

string outputFile = Path.Combine(outputFolder, "bigfile_output.psd");
string outputPicture = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    // לא צריך להיות שגיאה כאן
    psdImage.Save(outputFile, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(outputFile, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // לא צריך להיות שגיאה כאן
    psdImage.Save(outputPicture, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

---
title: Aspose.PSD עבור .NET 21.12 - רשימות הוצאה לאור
type: docs
weight: 10
url: /he/net/aspose-psd-for-net-21-12-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל רשימות הוצאה לאור עבור [Aspose.PSD עבור .NET 21.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-997|הוספת אפשרות להגבלת גופנים באופן תכנתי|תכונה|
|PSDNET-785|Aspose.PSD 20.10: כשל בטעינת PSD|באג|
|PSDNET-812|חריגת ImageLoad בעת טעינת PSD|באג|
|PSDNET-870|חריגת ImageLoad בטעינת שכבת PSD עם CompressionMethod שאינו נתמך|באג|
|PSDNET-918|Aspose.PSD 21.6: שיטת דחיסה אינה נתמכת עבור קובץ PSD|באג|
|PSDNET-984|שמירה שגויה של נתיב וקטור עם מסיכה|באג|
|PSDNET-1001|גופן שגוי ב-TextPortion בקובץ מסוים|באג|
|PSDNET-1031|חריגת "שיטת דחיסה אינה נתמכת" בטעינת תמונה|באג|
|PSDNET-1033|מיקום מחוץ לטווח בשמירה בקובץ מסוים|באג|
|PSDNET-1036|הוספת תמיכה ב-PathStructure כדי למנוע שגיאת טעינת קובץ|באג|

## **שינויים ב-API הציבורי**
# **APIs הנוספים:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Prefix
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.Length
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.PathStructure.StructureKey
- M:Aspose.PSD.FontSettings.SetAllowedFonts(System.String[])
- M:Aspose.PSD.FontSettings.IsFontAllowed(System.String)
- M:Aspose.PSD.FontSettings.GetReplacementFont(System.String)
- M:Aspose.PSD.FontSettings.GetFontReplacements(System.String)
- M:Aspose.PSD.FontSettings.SetFontReplacements(System.String,System.String[])
- M:Aspose.PSD.FontSettings.ClearFontReplacements

# **APIs המוסרים:**
- אף אחד

## **דוגמאות שימוש:**

**PSDNET-785. Aspose.PSD 20.10: כשל בטעינת PSD**

{{< highlight csharp >}}
            string src = "ShimadzuLetterhead100.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src, new PsdLoadOptions() { ReadOnlyMode = true }))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-812. חריגת ImageLoad בעת טעינת PSD**

{{< highlight csharp >}}
            string src = "5-MX10600_Amazon_DEVICES_2_1000x1000.psd";
            string output = "output.psd";
            using (var img = (PsdImage)Image.Load(src))
            {
                img.Save(output);
            }
{{< /highlight >}}

**PSDNET-870. חריגת ImageLoad בטעינת שכבת PSD עם CompressionMethod שאינו נתמך**

{{< highlight csharp >}}
            string srcFile = "sourceFile.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-918. Aspose.PSD 21.6: שיטת דחיסה אינה נתמכת עבור קובץ PSD**

{{< highlight csharp >}}
            string srcFile = "Fb-blue-jury (1).psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-984. שמירה שגויה של נתיב וקטור עם מסיכה**

{{< highlight csharp >}}
            string srcFile = "PsdConvertToPngExample.psd";
            string outputFilePng = "output.png";

            using (var psdImage = (PsdImage)Image.Load(srcFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                psdImage.Save(
                    outputFilePng,
                    new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha, Progressive = true, CompressionLevel = 9 });
            }
{{< /highlight >}}

**PSDNET-997. הוספת אפשרות להגבלת גופנים באופן תכנתי**

{{< highlight csharp >}}
            string srcFile = "fonts_com_updated.psd";
            string output = "etalon_fonts_com_updated.psd.png";

            try
            {
                var fontList = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                FontSettings.SetAllowedFonts(fontList);

                var myriadReplacement = new string[] { "Courier New", "Webdings", "Bookman Old Style" };
                var calibriReplacement = new string[] { "Webdings", "Courier New", "Bookman Old Style" };
                var arialReplacement = new string[] { "Bookman Old Style", "Courier New", "Webdings" };
                var timesReplacement = new string[] { "Arial", "NotExistedFont", "Courier New" };

                FontSettings.SetFontReplacements("MyriadPro-Regular", myriadReplacement);
                FontSettings.SetFontReplacements("Calibri", calibriReplacement);
                FontSettings.SetFontReplacements("Arial", arialReplacement);
                FontSettings.SetFontReplacements("Times New Roman", timesReplacement);

                using (PsdImage image = (PsdImage)Image.Load(srcFile))
                {
                    image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            } 
            finally
            {
                FontSettings.SetAllowedFonts(null);
                FontSettings.ClearFontReplacements();
            }
{{< /highlight >}}

**PSDNET-1001. גופן שגוי ב-TextPortion בקובץ מסוים**

{{< highlight csharp >}}
            string srcFile = "fonts_com.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                var tl = (TextLayer)image.Layers[1];
                var fontName = tl.TextData.Items[0].Style.FontName;
                if (fontName != "MyriadPro-Regular")
                {
                    throw new Exception("גופן שגוי");
                }

                // אמורים לקבל Myriad Pro, אך אנו רואים AdobeInvisFont
                image.Save(output, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-1031. חריגת "שיטת דחיסה אינה נתמכת" בטעינת תמונה**

{{< highlight csharp >}}
            string srcFile = "shirt-error.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

**PSDNET-1033. מיקום מחוץ לטווח בשמירה בקובץ מסוים**

{{< highlight csharp >}}
            string srcFile = "237708.psd";
            string output = "output.png";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1036. הוספת תמיכה ב-PathStructure כדי למנוע שגיאת טעינת קובץ**

{{< highlight csharp >}}
            string srcFile = "shirt-color.psd";
            string output = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output);
            }
{{< /highlight >}}

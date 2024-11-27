---
title: Aspose.PSD עבור .NET 23.2 - הערות לגרסה
type: docs
weight: 110
url: /he/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות לגרסה של [Aspose.PSD עבור .NET 23.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1359|רענון של עיצוב טקסט לשיפור פריסה, הצגה, ותמיכה|משפר|
|PSDNET-1270|הוספת אפשרות לעיבוד אפקט מאופק|תכונה|
|PSDNET-1391|הוספת תמיכה במצבי נתיב מתחת למטה ומלמעלה למלמעלה מהגדרות הפסקה|תכונה|
|PSDNET-912|שינוי פונט וצבע עבור TextLayer PSD|באג|
|PSDNET-1022|יצוא שגוי של טקסט במבחן TextUpdateTests, הטקסט חסר|באג|
|PSDNET-1221|טקסט קטן נוסף חסר לאחר שינוי גודל של תמונת PSD גדולה יותר|באג|
|PSDNET-1301|‏Aspose.Psd עבור .NET textLayer.UpdateText() מדפיס '-' (מקפים) כקו תחתון בצורה אקראית עבור סט נתונים שונים|באג|
|PSDNET-1379|הגדרות רזולוציה לא נכנסות לתוקפה בייצוא מ-PSD ל-PDF|באג|

## **שינויים ב-API הציבורי**

### **APIs שהוספו:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop

### **APIs שהוסרו:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual

## **דוגמאות לשימוש:**

**PSDNET-912. שינוי פונט וצבע עבור TextLayer PSD**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

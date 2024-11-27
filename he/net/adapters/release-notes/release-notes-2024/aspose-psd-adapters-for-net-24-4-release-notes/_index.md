---
title: האדפטרים של Aspose.PSD עבור .NET 24.4 - הערות לשחרור
type: תיעוד
weight: 100
url: /he/net/adapters/aspose-psd-adapters-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}
עמוד זה מכיל את ההערות האחרונות ל-[Aspose.PSD אדפטרים עבור .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)
{{% /alert %}}

| **Key**     | **Summary**                                                          | **Category** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | פרסום ראשי של Aspose.PSD.Adapters.Imaging ל-Nuget                 | שדרוג      |


## **שינויים ב-API הציבוריים**
# **APIs מוסיפים:**
- אין

# **APIs שהוסרו:**
- אין

## **דוגמאות שימוש:**

אנא בדקו את [עמוד התיעוד של Aspose.PSD.Adapters](/he/psd/net/adapters)

**PSDNET-1985. דוגמא מלאה ביותר לשימוש ב- Aspose.PSD.Adapters**

{{< highlight csharp >}}
// הוספת אפשרות אדפטרים בתצורת האיתחול שלך
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// אפשר גם יצרת Exporters
Aspose.PSD.Adapters.Imaging.EnableExporters();

// כדי לעבוד עם אדפטרים, נדרשות רשיונות עבור Aspose.PSD ועבור adaptee
// הנה דוגמה לאיך להחיל רשיון של Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// כאן דוגמה לאיך להחיל רשיון של Adaptee עבור Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// כעת תוכלו להפעיל קוד בכלים או ספריית PSD או Imaging

// לאחר מכן, כל אלו קבצים יכולים להיפתח על ידי Aspose.PSD בלי שום קוד נוסף, רק עם
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // לאחר ביצוע קוד זה, תקבלו את קובץ ה-PSD שנוצר מ-WEBP ותוכלו להחיל כל עיבודים בAspose.PSD כולל טשטוש והתאמת העקבות
}

// בנוסף, תוכלו ליצור תמונות של adaptee שיוצאות לתבנית PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // השתמש ב-API של Aspose.Imaging כדי לערוך קובץ WEBP עם יכולות ספציפיות ל-Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // אז פשוט השתמש בשיטת ToPsdImage() וערוך את הקובץ כמו PSD עם יכולות דומות לפוטושופ כולל שכבות, מסננים חכמים ואובייקטים חכמים.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("טקסט מסוים", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // שמור את קובץ ה-PSD הסופי באמצעות Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// אם אין צורך להשתמש במאגרי נתונים או במייצאים שמסופקים על ידי האדפטרים, אפשר להשבית אותם
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
{{< /highlight >}}

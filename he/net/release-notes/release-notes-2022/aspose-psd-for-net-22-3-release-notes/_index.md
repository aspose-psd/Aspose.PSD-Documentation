---
title: Aspose.PSD עבור .NET 22.3 - הערות גרסה
type: מסמכים
weight: 100
url: /he/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות לגרסה עבור [Aspose.PSD עבור .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-210|הוספת שדה IsOpen לקבוצת שכבות|תכונה|
|PSDNET-643|תמונת PSD עם מסכות שכבת רסטר משליכה מסכות בעת השמירה לתמונת PSD 16 ביטים|תקלה|
|PSDNET-899|מצב ערבוב Dissolve לא מתקם בתיקייה עם מסכה|תקלה|
|PSDNET-1047|קובץ ספציפי לא ניתן לפתיחה בפוטושופ לאחר השמירה ב-Aspose.PSD 21.11|תקלה|
|PSDNET-1068|הצגה שגויה של השכבה עם מצב ערבוב Linear Dodge (Add)|תקלה|
|PSDNET-1069|שכבת מילוי ארעית זורקת חריגה בעת עדכון אחרי הטעינה|תקלה|


## **שינויים ב- API הציבוריים**
# **APIs שהתווספו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **APIs שהוסרו:**
- אין


## **Usage examples:**

**PSDNET-210. הוספת שיחות IsOpen לקבוצת שכבות**

{{< highlight csharp >}}
// דוגמא לקריאה וכתיבה בשדה IsOpen בזמן ריצה. 
string sourceFileName = "LayerGroupOpenClose.psd";
string outputFileName = "Output" + sourceFileName;

using (var image = (PsdImage)Image.Load(sourceFileName))
{
    foreach (var layer in image.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    image.Save(outputFileName);
}
{{< /highlight >}}

**PSDNET-643. תמונת PSD עם מסכות שכבת רסטר משליכה מסכות בעת השמירה לתמונת PSD 16 ביטים**

{{< highlight csharp >}}
            string sourceFilePath = "OneRegularAndOneRegularWithMask.psd";
            string outputFilePath = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFilePath, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. מצב ערבוב Dissolve לא מתקם בתיקייה עם מסכה**

{{< highlight csharp >}}
            string sourceFile = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. קובץ מסוים לא ניתן לפתיחה בפוטושופ לאחר השמירה ב-Aspose.PSD 21.11**

{{< highlight csharp >}}
            string sourceFile = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(sourceFile))
            {
                image.Save(outputPsd);
            }

            // נדרש לפתוח באופן ידני את קובץ ה-PSD המצורף באמצעות פוטושופ.

            using (PsdImage image = (PsdImage) Image.Load(outputPsd))
            {
                // אין חריגה.
            }
{{< /highlight >}}

**PSDNET-1068. הצגה שגויה של השכבה עם מצב ערבוב Linear Dodge (Add)**

{{< highlight csharp >}}
            string sourceFile = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(sourceFile))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. שכבת מילוי ארעית זורקת חריגה בעת עדכון אחרי הטעינה**

{{< highlight csharp >}}
            string sourceFile = "AllTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(sourceFile))
            {
                var fillLayer = (FillLayer)image.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}

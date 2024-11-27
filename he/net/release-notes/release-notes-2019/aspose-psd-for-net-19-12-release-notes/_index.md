```toml
---
title: "הערות שחרור Aspose.PSD עבור .NET 19.12"
type: "docs"
weight: 10
url: "/he/net/aspose-psd-for-net-19-12-release-notes/"
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לגרסה של [Aspose.PSD עבור .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDNET-11|[תמיכה בשכבת קישור](/he/psd/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|תכונה|
|PSDNET-131|[תמיכה ב-SoCoResource](/he/psd/net/support-of-socoresource/)|תכונה|
|PSDNET-115|שורות פיסוק מתווספות לשורות פיסוק קיימות אם שכבת טקסט מתעדכנת עם מחרוזת|באג|
|PSDNET-157|שמירת PSB כ-PNG קופאת|באג|
|PSDNET-250|חריגה בטעינה של קובץ PSD CMYK ללא שכבות עם דחיסת RLE|באג|
|PSDNET-161|חריגה בעדכון שכבות טקסט|באג|
|PSDNET-222|הקטנת כמה קבצי PSD עם מסכות שכבה עובדת באופן שגוי|באג|
|PSDNET-244|שמירת PSD עם תרבות CultureInfo.CurrentCulture מביאה לחריגות בטעינה|באג|

## **שינויים ב- API הציבוריים**
# **APIs שנוספו:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **APIs שהוסרו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **דוגמאות שימוש:**
**PSDNET-11. תמיכה בשכבת קישור**

{{< highlight java >}}

           באמצעות (PsdImage)Image.Load("example.psd")

            {

                Layer[] שכבות = psd.Layers;

                // לקשר את כל השכבות בקבוצה אחת

                קבוצת קישור של שכבות קצרות = psd.LinkedLayersManager.LinkLayers(שכבות);

                // לקבל id עבור שכבה אחת

                בקידום קישורות = psd.LinkedLayersManager.GetLinkGroupId(שכבות[0]);

                אם (קבוצת שכבות != id של קישור)

                {

                    לזרוק חריגה("הקבוצות של שכבות וקידום הקישור אינם שווים.");

                }

                // לקבל את כל השכבות המקושרות לפי id של קישור.

                Layer[] שכבות מקושרות = psd.LinkedLayersManager.GetLayersByLinkGroupId(בקידום קישורות);

                // להפריד כל שכבה מהקבוצה

                כל שכבה שמקושרת בשכבה מקושרת

                {

                    psd.LinkedLayersManager.UnlinkLayer(שכבה מקושרת);

                }

                // לאחזר NULL עבור id קישור שאין לו שכבות בקבוצה.

                שכבות מקושרות = psd.LinkedLayersManager.GetLayersByLinkGroupId(בקידום קישורות);

                אם (שכבות מקושרות != null)

                {

                    לזרוק חריגה("השדה של השכבות המקושרות אינו NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. תמיכה ב-SoCoResource**

{{< highlight java >}}

      // תמיכה ב-SoCoResource

    string שם_קובץ_מקור = "ColorFillLayer.psd";

    string נתיב_יצוא = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(שם_קובץ_מקור);

    using (im)

    {

        עבור (var שכבה in im.Layers)

        {

            אם (שכבה היא FillLayer)

            {

                var שכבת_מילוי = (FillLayer)שכבה;

                עבור (var משאב בשכבת_מילוי.Resources)

                {

                    אם (משאב הוא SoCoResource)

                    {

                        var משאב_SoCo = (SoCoResource)משאב;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), משאב_SoCo.Color);

                        משא
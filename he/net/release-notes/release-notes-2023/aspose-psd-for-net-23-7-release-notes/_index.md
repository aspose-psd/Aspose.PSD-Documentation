---
title: Aspose.PSD עבור .NET 23.7 - הערות לגרסה
type: docs
weight: 60
url: /he/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות לגרסה עבור [Aspose.PSD עבור .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח** | **סיכום**                                                                                             | **קטגוריה** |
|:----------|:-------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-802 | הוספת אפשרות ליצוא כל שכבת קובץ PSD לקובץ Gif מונפשים                                           | תכונה      |
| PSDNET-1441 | הקצאת מאפיין המילוי של שכבת צורה ממשאב vscg                                                    | תכונה      |
| PSDNET-1534 | הוספת סוגים חדשים של דיפור (עגול וקשת)                                                           | תכונה      |
| PSDNET-1543 | שינוי היישום ששומר את קובץ ה-PSD ל-Aspose.PSD אם נקבע המאפיין UpdateMetadata ל-true    | תכונה      |
| PSDNET-1567 | הגדלת אזור החישוב של קובץ השרבור                                                             | תכונה      |
| PSDNET-1471 | שכבת התאום שחורה ולבנה מעבדת שקיניות חצי שקופה באופן שגוי                                      | באג       |
| PSDNET-1505 | החלפת תוכן SmartObject (כאשר האפשרות AllowWarpRepaint פעילה) נכשלת לאחר 2 דקות של חישוב | באג       |
| PSDNET-1585 | הוספת אפשרות לקבל את המיקום האמיתי של LayerGroup משמאל ומלמעלה                               | באג       |
| PSDNET-1589 | שינוי של שכבת הגודל עובד לא נכון כאשר לקובץ PSD יש משאב VogkResource עם מבנים בנקודות      | באג       |
| PSDNET-1608 | TextBound אינה עובדת כפי שצפוי                                                                     | באג       |
| PSDNET-1612 | הוספת שכבה שנוצרה עם בנאי מוגדר כברירת מחדל לתמונת PSD לא מוסיפה משאבים ברירת מחדל לזה | באג       |
| PSDNET-1623 | `Timeline.LoopesCount` מתעלם בשמירה על Gif מונפש                                               | באג       |


## **שינויים ב-API הציבוריים**
# **APIs שנוספו:**
- P:Aspose.PSD.ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **APIs שהוסרו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **דוגמאות שימוש:**

**PSDNET-802. הוספת אפשרות ליצוא כל שכבת קובץ PSD לקובץ Gif מונפש**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

...
{{< /highlight >}}


**PSDNET-1441. הקצאת מאפיין המילוי של שכבת צורה ממשאב vscg**

{{< highlight csharp >}}
string srcFile = "ShapeInternalSolid.psd";
string outFile = "ShapeInternalSolid.psd.out.psd";

...
{{< /highlight >}}


(המשך בתיקיית המקור)
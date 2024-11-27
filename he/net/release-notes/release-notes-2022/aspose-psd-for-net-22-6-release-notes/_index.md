---
title: Aspose.PSD עבור .NET 22.6 - רשימות שחרור
type: docs
weight: 70
url: /he/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל רשומות שחרור עבור [Aspose.PSD עבור .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-940|יצירת API לקבלת גיבוב ייחודי עבור שכבות דומות בקבצים שונים|שיפור|
|PSDNET-678|תצוגה שגויה של שכבת מילוי עם תבנית במקרה בו יש תבניות יותר מאחת וסדר השכבות השתנה|באג|
|PSDNET-1125|חריגה בטעינת קובץ PSD מסוים עם מצב צבע CMYK|באג|


## **שינויים ב-API הציבורי**

# **APIם שהתווספו:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **APIם שהוסרו:**
- אף אחד


## **דוגמאות שימוש:**

**PSDNET-678. תצוגה שגויה של שכבת מילוי עם תבנית במקרה בו יש תבניות יותר מאחת וסדר השכבות השתנה**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. יצירת API לקבלת גיבוב ייחודי עבור שכבות דומות בקבצים שונים**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // הקוד המתורגם נמצא כאן
}
{{< /highlight >}}

**PSDNET-1125. חריגה בטעינת קובץ PSD מסוים עם מצב צבע CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}
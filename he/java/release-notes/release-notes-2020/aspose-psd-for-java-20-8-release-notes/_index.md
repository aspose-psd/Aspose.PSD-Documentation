---
title: הערות שחרור Aspose.PSD עבור Java 20.8
type: מסמכים
weight: 50
url: /he/java/aspose-psd-for-java-20-8-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל את הערות השחרור עבור [Aspose.PSD עבור Java 20.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.8/) {{% /alert %}}

|**Key**|**Summary**|**Category**|
| :- | :- | :- |
|PSDJAVA-264|תמיכה ב-SoLdResource (משאבי פלטפורמה של נתוני שכבת נתונים לאובייקט חכם)|תכונה|
|PSDJAVA-263|תמיכה ב-PlLdResource (משאב של שכבת מיקום עבור שכבת אובייקט חכם)|תכונה|
|PSDJAVA-262|הוספת תמיכה במבני מערך אובייקט ומערך יחידות: חתימות ObAr / UnFl|תכונה|
|PSDJAVA-265|קו תחתון וקו חוצה אבדו לאחר מיקוד בטקסט בקובץ שנשמר עם Aspose.|באג|
|PSDJAVA-257|תיקון שמירת תמונת PSD מודיפיצירה עם מצב צבע CMYK 16 ביט לערוץ|באג|
|PSDJAVA-268|רגרסיה: Aspose.PSD 20.7.0 מפרקת גדלים של גופני טקסט עבור קבצים ישנים|באג|

# **שינויים ב-API הציבורי**
# **APIs שנוספו:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.ImageStack
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Raster
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Unknown
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.PlacedLayerType.Vector
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.AntiAliasPolicyKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.SoLdResource.TypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ObjectArrayStructure.StructureKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.UnitArrayStructure.StructureKey
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ClassID.#ctor(byte[],boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getAntiAliasPolicy
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource....
(המשך בקישור)
```
...getPlacedLayerType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getRight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTop
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTotalPages
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getTransformMatrix
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVOrder
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getValue
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPointUnit
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.getVerticalMeshPoints
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.isCustom
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setAntiAliasPolicy(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource.setBottom(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.smartobjectresources.IPlacedLayerResource....
(המשך בקישור)

**דוגמאות שימוש:**

**PSDJAVA-264. תמיכה ב-SoLdResource (משאבי שכבת נתונים של אובייקט חכם)**
{{< highlight java >}}
// This example shows how to get or set the smart object layer data properties of the PSD file.
(הכולל בקובץ)
{{< /highlight >}}

**PSDJAVA-263. תמיכה ב-PlLdResource (משאב של שכבת מיקום עבור שכבת אובייקט חכם)**
{{< highlight java >}}
// This example shows how to get or set the Placed layer resource properties of the PSD file.
(הכולל בקובץ)
{{< /highlight >}}

**PSDJAVA-262. הוספת תמיכה במבני מערך אובייקט ומערך יחידות: חתימות ObAr / UnFl**
{{< highlight java >}}
// This example proves that ObjectArrayStructure and UnitArrayStructure are supported by...
(הכולל בקובץ)
{{< /highlight >}}

**PSDJAVA-265. קו תחתון וקו חוצה אבדו לאחר מיקוד בטקסט בקובץ שנשמר עם Aspose.PSD**
{{< highlight java >}}
// This example proves that underline and strikethrough formatting does not disappear on...
(הכולל בקובץ)
{{< /highlight >}}

**PSDJAVA-257. תיקון שמירת תמונת PSD מודיפיצירה עם מצב צבע CMYK 16 ביט לערוץ**
{{< highlight java >}}
// This example proves that there is no error on saving a 16-bit PSD image in the CMYK...
(הכולל בקובץ)
{{< /highlight >}}

**PSDJAVA-268. רגרסיה: Aspose.PSD 20.7.0 מפרקת גדלים של גופני טקסט עבור קבצים ישנים**
{{< highlight java >}}
// This example reproduces the bug that breaks font sizes for older PSD files.
(הכולל בקובץ)
{{< /highlight >}}
```
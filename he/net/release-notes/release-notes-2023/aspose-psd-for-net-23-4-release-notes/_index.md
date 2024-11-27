---
title: Aspose.PSD עבור .NET 23.4 - הערות לשחרור
type: docs
weight: 90
url: /he/net/aspose-psd-for-net-23-4-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל הערות לשחרור עבור [Aspose.PSD עבור .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1409|עיצוב של מחלקת RawColor עבור ה-API הציבורי לשימוש ב-PSD API במקום מבנה Color לסייע בממשק|שיפור|
|PSDNET-1332|שילוב שכבת כוונת מפה התאפיון ממצב ניסיון לקוד Aspose.PSD הראשי|תכונה|
|PSDNET-1448|עריכת טקסט באמצעות חלקי טקסט אינה שומרת את התוצאה הנכונה|באג|
|PSDNET-1449|ההתחלה והסיום של הסגנונות או הפסקות מופיעים במקום שגוי בעריכת שכבת טקסט על ידי ITextPortion|באג|
|PSDNET-1509|העברת העיצוב בעת עריכה בפוטושופ|באג|

## **שינויים ב-API הציבורי**
# **API-ות שנוספו:**
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P:Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor


# **API-ות שהוסרו:**
- אין


## **דוגמאות לשימוש:**

**PSDNET-1332. שילוב שכבת כוונת מפת מעבה ממצב ניסיון לקוד Aspose.PSD הראשי**

{{< highlight csharp >}}
...
{{< /highlight >}}


**PSDNET-1409. עיצוב מחלקת RawColor עבור ה-API הציבורי לשימוש ב-PSD API במקום מבנה Color מיושן**

{{< highlight csharp >}}
...
{{< /highlight >}}


**PSDNET-1448. עריכת טקסט באמצעות חלקי טקסט אינה שומרת את התוצאה הנכונה**

{{< highlight csharp >}}
...
{{< /highlight >}}


**PSDNET-1449. ההתחלה והסיום של הסגנונות או הפסקות מופיעים במקום שגוי בעריכת שכבת טקסט על ידי ITextPortion**

{{< highlight csharp >}}
...
{{< /highlight >}}


**PSDNET-1509. העברת העיצוב בעת עריכה בפוטושופ**

{{< highlight csharp >}}
...
{{< /highlight >}}
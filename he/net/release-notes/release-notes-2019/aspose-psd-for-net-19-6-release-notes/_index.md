---
title: Aspose.PSD עבור .NET 19.6 - הערות גרסה
type: docs
weight: 70
url: /he/net/aspose-psd-for-net-19-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לגרסה של [Aspose.PSD עבור .NET 19.6](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

| **מפתח** | **סיכום** | **קטגוריה** |
| :- | :- | :- |
|PSDNET-127|יכולת להמיר קובץ PSD ל־PSB ולהיפך|תכונה|
|PSDNET-154|העברת מקורות Aspose.Imaging 19.5 ל־Aspose.PSD|שיפור|
|PSDNET-155|ניקוי API ציבורי הקשור ל־Aspose.PSD|שיפור|
|PSDNET-159|הסרת השדה IsLicensed|שיפור|
|PSDNET-102|המרת PSB ל־JPG מתקעת|באג|
|PSDNET-150|מיקום שכבת טקסט שהתווספה חדש נזוז בעת עריכה בפוטושופ|באג|

## **שינויים ב- API הציבורי**

# **APIs שנוספו:**
- T:Aspose.PSD.FileFormats.Psd.FileFormatVersion
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psd
- F:Aspose.PSD.FileFormats.Psd.FileFormatVersion.Psb
- P:Aspose.PSD.ImageOptions.PsdOptions.FileFormatVersion
- F:Aspose.PSD.FileFormat.Cdr
- F:Aspose.PSD.FileFormat.Cmx
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResource.PsbResourceSignature
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LayerLockType.LockAll
- P:Aspose.PSD.Image.BufferSizeHint
- P:Aspose.PSD.ImageOptions.JpegOptions.ResolutionUnit
- P:Aspose.PSD.ImageOptions.VectorRasterizationOptions.TextRenderingHint
- M:Aspose.PSD.ImageOptions.VectorRasterizationOptions.CopyTo(Aspose.PSD.ImageOptions.VectorRasterizationOptions)
- P:Aspose.PSD.LoadOptions.BufferSizeHint
- T:Aspose.PSD.MemoryManagement.Configuration
- P:Aspose.PSD.MemoryManagement.Configuration.BufferSizeHint
- T:Aspose.PSD.ResolutionUnit
- F:Aspose.PSD.ResolutionUnit.None
- F:Aspose.PSD.ResolutionUnit.Inch
- F:Aspose.PSD.ResolutionUnit.Cm
# **APIs שהוסרו:**
- M:Aspose.PSD.Blend.op_Equality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.Blend.op_Inequality(Aspose.PSD.Blend,Aspose.PSD.Blend)
- M:Aspose.PSD.ColorBlend.op_Equality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth
- ...

## **דוגמאות שימוש:**
**PSDNET-127. יכולת להמיר קובץ PSD ל־PSB ולהיפך**

{{< highlight java >}}

 // יכולת להמיר קובץ PSD ל־PSB ולהיפך

            string sourceFilePathPsb = "2layers.psb";

            string outputFilePathPsd = "ConvertFromPsb.psd";

            using (Image img = Image.Load(sourceFilePathPsb))

...

{{< /highlight >}}

**PSDNET-102. המרת PSB ל־JPG מתקעת**

{{< highlight java >}}

  // המרת PSB ל־JPG מתקעת

            string[] sourceFileNames = new string[] { 

...

{{< /highlight >}}

**PSDNET-150: מיקום שכבת טקסט שהתווספה חדש נזוז בעת עריכה בפוטושופ**

{{< highlight java >}}

             // מיקום שכבת טקסט שהתווספה חדש נזוז בעת עריכה בפוטושופ

    string sourceFileName = "OneLayer.psd";

...

{{< /highlight >}}# **PSDNET-155: ניקוי API ציבורי הקשור ל־Aspose.PSD**

{{< highlight java >}}

 // ניקוי API ציבורי הקשור ל־Aspose.PSD

}}

{{< /highlight >}}

**PSDNET-159: הסרת השדה IsLicensed**

{{< highlight java >}}

 // הסרת השדה IsLicensed         

    string sourceFilePathPsd = "2layers.psd";

    string outputFilePathPsb = "ConvertFromPsd.psb";

...

{{< /highlight >}}

**שינויים ב- API הציבורי**

# **APIs שנוספו:**
- T:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Units
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Reserved
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Recording
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Rendering
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Size1
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Size2
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.ColorEncoding
- P:Aspose.PSD.FileFormats.Bmp.Os22XBitmapHeader.Identifier

# **APIs שהוסרו:**
- M:Aspose.PSD.ColorBlend.op_Inequality(Aspose.PSD.ColorBlend,Aspose.PSD.ColorBlend)
- T:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader
- M:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.#ctor
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.HeaderSize
- P:Aspose.PSD.FileFormats.Bmp.BitmapCoreHeader.BitmapWidth

---

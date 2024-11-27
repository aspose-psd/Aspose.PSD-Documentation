---
title: Aspose.PSD CLI גירוש ל .NET 24.6 - רשומות לגרסה
type: docs
weight: 90
url: /he/psd/net/cli/crop/aspose-psd-crop-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל רשומות לגרסה של [Aspose.PSD CLI גירוש ל.NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **מפתח**   | **סיכום**                                                                                   | **קטגוריה** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | גירוש ראשון של יישומי Aspose.PSD CLI: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor |  שדרוג      |


## **דוגמאות שימוש:**

**PSDNET-2110. גירוש ראשון של אפליקציית גירוש Aspose.PSD CLI**

**שימוש משורת הפקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מקוד הפקודה:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.CommandLineOptions.CropOptions
{
    InputPath = "photo1.jpg",
    CropType = CropType.Rect,
    Left = 10,
    Top = 35,
    Width = 250,
    Height = 300,
    OutputPath = "cropped_photo.png",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Crop.Apply(options);
{{< /highlight >}}

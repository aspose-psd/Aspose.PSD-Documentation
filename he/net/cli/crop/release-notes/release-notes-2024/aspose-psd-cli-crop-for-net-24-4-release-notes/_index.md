---
title: התעולה Aspose.PSD CLI ל-Crop עבור .NET 24.4 - הערות גרסה
type: docs
weight: 90
url: /he/net/cli/crop/aspose-psd-cli-crop-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לגרסה של [Aspose.PSD CLI ל-Crop עבור .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Crop/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                        | **קטגוריה** |
|:------------|:---------------------------------------------------|:-------------|
| PSDNET-2025 | גרסת התחלה של אפליקציית Aspose.PSD CLI ל-Crop |  שיפור |


## **דוגמאות שימוש:**

**PSDNET-2023. גרסת התחלה של אפליקציית Aspose.PSD CLI ל-Crop**

**שימוש משורת הפקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Crop --input photo1.jpg --output cropped_photo.png --format png --left 10 --top 35 --width 250 --height 300 --cropType rect --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מקוד:**

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

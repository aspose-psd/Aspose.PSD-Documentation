---
title: Aspose.PSD CLI שינוי גודל עבור .NET 24.4 - הודעות שחרור
type: docs
weight: 90
url: /he/net/cli/resize/release-notes/aspose-psd-cli-resize-for-net-24-4-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההודעות השחרור עבור [Aspose.PSD CLI שינוי גודל עבור .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                              | **קטגוריה**|
|:------------|:-----------------------------------------------------|:-------------|
| PSDNET-2026 | שחרור ראשוני של אפליקציית Aspose.PSD CLI לשינוי גודל | שיפור |

## **דוגמאות שימוש:**

**PSDNET-2026. שחרור ראשוני של אפליקציית Aspose.PSD CLI לשינוי גודל**

**שימוש משורת פקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מתוך קוד:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ResizeOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "resized.png",
    Scale = 200,
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Resize.Apply(options);

{{< /highlight >}}

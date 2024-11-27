---
title: Aspose.PSD CLI Convert for .NET 24.4 - הודעות לשחרור
type: docs
weight: 90
url: /he/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הודעות לשחרור עבור [Aspose.PSD CLI Convert for .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **מפתח**   | **סיכום**                                              | **קטגוריה** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | הפצת גרסה ראשונית של אפליקציית המרת Aspose.PSD CLI | שיפור       |


## **דוגמאות לשימוש:**

**PSDNET-2023. הפצת גרסה ראשונית של אפליקציית המרת Aspose.PSD CLI**

**שימוש משורת פקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מקוד משורת הפקודה:**

{{< highlight csharp >}}
var options = new Aspose.PSD.CLI.Convert.CommandLineOptions.ConversionOptions
{
    InputFiles = new List<string> { "photo_1.jpg", "photo_2.jpg", "photo_3.jpg", "photo_4.jpg", "photo_5.jpg", "photo_6.jpg" },
    OutputPath = "result.zip",
    OutputFormat = "png"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Convert.Apply(options);
{{< /highlight >}}

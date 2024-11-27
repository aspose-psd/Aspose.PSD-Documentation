---
title: הפצת Aspose.PSD CLI עבור .NET 24.6 - יומן שחרורים
type: מסמכים
weight: 90
url: /he/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל יומן שחרורים עבור [Aspose.PSD CLI Export עבור .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                                                 | **קטגוריה** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | שחרור ראשוני של אפליקציות Aspose.PSD CLI: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor |  שדרוג |


## **דוגמאות שימוש:**

**PSDNET-2110. שחרור ראשון של אפליקציית Aspose.PSD CLI Export**

**שימוש משורת פקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --קלט photo1.jpg --פלט exported.png --פורמט png --שםשכבה Layer1 --רישיון Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מקוד:**

{{< highlight csharp >}}

var options = new Aspose.PSD.CLI.CommandLineOptions.ExportOptions
{
    PathToInputImage = "photo1.jpg",
    PathToOutputImage = "exported.png",
    OutputFormat = "png",
    LayerName = "Layer1"
};


if (isLicensed)
{
    options.LicensePath = "Aspose.PSD.Product.Family.lic";
}

Aspose.PSD.CLI.Export.Apply(options);

{{< /highlight >}}

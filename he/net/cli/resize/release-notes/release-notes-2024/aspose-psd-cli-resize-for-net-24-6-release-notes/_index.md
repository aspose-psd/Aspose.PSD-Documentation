---
title: Aspose.PSD CLI הקטנה עבור .NET 24.6 - הודעות גירסה
type: docs
weight: 90
url: /he/net/cli/resize/aspose-psd-resize-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הודעות גירסה עבור [Aspose.PSD CLI הקטנה עבור .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Resize/)

{{% /alert %}}

| **מפתח**   | **סיכום**                                                                                    | **קטגוריה** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | הגרסה הראשונית של Aspose.PSD CLI Apps: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor |  שיפור     |


## **דוגמאות שימוש:**

**PSDNET-2110. הוצאה אתחולית של אפליקציית הקטנת Aspose.PSD CLI**

**שימוש משורת פקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Resize --input photo1.jpg --output resized.png --width 200 --height 340 --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מקוד:**

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

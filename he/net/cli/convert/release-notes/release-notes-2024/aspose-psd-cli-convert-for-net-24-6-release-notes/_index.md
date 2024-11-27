---
title: הופעל.PSD CLI המר עבור .NET 24.6 - הערות לגרסה
type: מסמכים
weight: 90
url: /he/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות לגרסה של [Aspose.PSD CLI המר עבור .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                                                                   | **קטגוריה** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | הופעל ראשוני של שימושים עבור Aspose.PSD: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor | שדרוג       |


## **דוגמאות שימוש:**

**PSDNET-2110. הופעל ראשוני של שימושים עבור Aspose.PSD CLI: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor**

**שימוש מהשורת פקודה:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**שימוש מתוך קוד מצורף:**

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

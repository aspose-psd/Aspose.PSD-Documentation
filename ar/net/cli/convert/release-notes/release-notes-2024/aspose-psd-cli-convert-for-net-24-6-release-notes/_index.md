---
title: ملاحظات الإصدار Aspose.PSD CLI Convert for .NET 24.6
type: docs
weight: 90
url: /ar/net/cli/convert/aspose-psd-cli-convert-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

تحتوي هذه الصفحة على ملاحظات الإصدار لـ [Aspose.PSD CLI Convert for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **المفتاح**     | **الملخص**                                                                                 | **الفئة** |
|:------------|:--------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2110 | الإصدار الأولي لتطبيقات Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor |  تحسين |


## **أمثلة الاستخدام:**

**PSDNET-2110. الإصدار الأولي لتطبيقات Aspose.PSD CLI: Aspose.PSD.CLI.Export و Aspose.PSD.CLI.NLP.Editor**

**الاستخدام عبر سطر الأوامر:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**الاستخدام عبر الكود البرمجي:**

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
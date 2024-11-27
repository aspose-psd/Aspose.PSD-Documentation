---
title: تطبيق Aspose.PSD CLI Convert لـ .NET 24.4 - ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/cli/conversion/aspose-psd-conversion-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [تطبيق Aspose.PSD CLI Convert لـ .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.CLI.Convert/)

{{% /alert %}}

| **المفتاح**     | **الملخص**                                              | **الفئة** |
|:------------|:---------------------------------------------------------|:-------------|
| PSDNET-2023 | الإصدار الأولي لتطبيق Aspose.PSD CLI Convert | تحسين |


## **أمثلة الاستخدام:**

**PSDNET-2023. الإصدار الأولي لتطبيق Aspose.PSD CLI Convert**

**الاستخدام من سطر الأوامر:**

{{< highlight bash >}}
Aspose.PSD.CLI.Convert --input photo_1.jpg --output result.zip --format png --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**الاستخدام من رمز الأمر:**

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
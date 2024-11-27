---
title: تصدير Aspose.PSD CLI لـ .NET 24.6 - ملاحظات الإصدار
type: docs
weight: 90
url: /ar/net/cli/export/aspose-psd-export-cli-app-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

هذه الصفحة تحتوي على ملاحظات الإصدار لـ [Aspose.PSD CLI التصدير لـ .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.Export/)

{{% /alert %}}


| **المفتاح** | **الملخص**                                                                           | **الفئة**   |
|:------------|:--------------------------------------------------------------------------------------|:------------|
| PSDNET-2110 | الإصدار الأولي من تطبيقات Aspose.PSD CLI: Aspose.PSD.CLI.Export وAspose.PSD.CLI.NLP.Editor | تعزيز |


## **أمثلة الاستخدام:**

**PSDNET-2110. الإصدار الأولي من تطبيق تصدير Aspose.PSD CLI**

**الاستخدام من سطر الأوامر:**

{{< highlight bash >}}
Aspose.PSD.CLI.Export --input photo1.jpg --output exported.png --format png --layerName Layer1 --license Aspose.PSD.Product.Family.lic
{{< /highlight >}}

**الاستخدام من الكود:**

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